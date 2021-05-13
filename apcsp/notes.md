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
# 8th
failed:
    jkim0205.key

# 7th
No key:
    abao
failed:
    emorrow
    jhalko
    rlee0096
    mpae


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

----

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


----------------------------------------------------------
*I - LEDs
N - 3d prints?
N - pens/rulers/drafting
*O - orrery - add motor
*V - motors?
A - tools (more)
T - circuit boards
I - Lego? 3Dp Rocket? LED Matrix?
*O - infinity mirror
*N - motors

2x4s for mounting
    - sections (2-3?)
Wall anchors
Power supply/wiring
    - 5v power bus

-------
Classroom

- sort through student projects
- organize workbench
- greenscreen
    - lights
    - camera
- posters/deco
- Wall lego plates + bin

Projects
- LED grid
- kame robot
- Innovation sign


Donations list:
----------------
Electronics - printers, dvd/cd players
Lego (esp. Technics)
Tools



