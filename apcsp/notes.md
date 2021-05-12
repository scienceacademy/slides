Meeting ID: 968 2612 4262
Passcode: 083094




# 8th

---

* Discussion, questions
* Code example
* Questions:

* Should cryptocurrency be regulated by the government? Which government?
* Cryptocurrency proponents say the energy costs are justified by the benefits in economic freedom. Do you agree or disagree?

---


-----------------------------

# INTERVENTIONS

#7
- Kim, Terrius, p/s
- Colligan, Apollo, s
- Lee, Jayden, s
- Russel-Isaacs, p
- Story, p/s
- Casillas
- Vaysberg
- Paek

#8

Parent conf
----------
xMejia
    mom
xChrisman
    dad
xAltamirano - after 4pm
    mom


-------
Classroom

- sort through student projects
- organize workbench
- greenscreen
    - lights
    - camera
- posters/deco



---
array of ranks [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
count ranks in hand
how many non-zero values?
    2:
        is either 4? 4 of a kind
        else full house
    3:
        a 3? 3 of a kind
        else 2 pair
    4:
        pair
    5:
        is flush?
        is straight?

also great (quick) for comparing hands

-----
pip install pycryptodome
#### CREATE KEYS (EXAMPLE) #####################
```python
from Crypto.PublicKey import RSA

key_pair = RSA.generate(2048)
# priv = key_pair.export_key()
# pub = key_pair.publickey().export_key()

print("p =", key_pair.p)
print("q =", key_pair.q)
print("-"*10)
print("m =", key_pair.n)
print("-"*10)
print("d =", key_pair.d)
print("-"*10)
print("e =", key_pair.e)
```

#### ENCRYPT ####################################
```python
from Crypto.PublicKey import RSA
from Crypto.Cipher import PKCS1_OAEP
import base64

keyfile = input("Public key: ")

with open(keyfile, "r") as f:
    data = f.read()
pub = RSA.import_key(data)

cleartext = input("Message: ").encode()
cipher = PKCS1_OAEP.new(pub)
ciphertext = cipher.encrypt(cleartext)
print("Ciphertext:")
print(base64.b64encode(ciphertext).decode())
```

#### DECRYPT ###################################
```python
from Crypto.PublicKey import RSA
from Crypto.Cipher import PKCS1_OAEP
import base64

with open("private.key", "r") as file:
    data = file.read()
priv = RSA.import_key(data)

ciphertext = input("Message: ").encode()
ciphertext = base64.b64decode(ciphertext)
cipher = PKCS1_OAEP.new(priv)
cleartext = cipher.decrypt(ciphertext)
print("Cleartext:")
print(cleartext.decode())
```

#### SIGN ###########################
```python
from Crypto.PublicKey import RSA
from Crypto.Signature import pss
from Crypto.Hash import SHA256
import base64

def sign():
    with open("private.key", "r") as file:
        data = file.read()
    private_key = RSA.import_key(data)
    msg = input("Message: ").encode()
    hashed = SHA256.new(msg)
    signature = pss.new(private_key).sign(hashed)
    with open("output.txt", "w") as output:
        output.write(msg.decode())
        output.write("\n--\n")
        output.write(base64.b64encode(signature).decode())
    # print(base64.b64encode(signature).decode())

def verify():
    keyfile = input("Public key file: ")
    with open(keyfile, "r") as f:
        data = f.read()
    public_key = RSA.import_key(data)
    msg = input("Message: ").encode()
    signature = input("Signature: ").encode()
    signature = base64.b64decode(signature)
    hashed = SHA256.new(msg)
    try:
        pss.new(public_key).verify(hashed, signature)
        print("Verified")
    except:
        print("Verification failed")

choice = input("(S)ign or (V)erify: ").lower()
if choice == "s":
    sign()
elif choice == "v":
    verify()
```
