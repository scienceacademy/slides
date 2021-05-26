Meeting ID: 968 2612 4262
Passcode: 083094


Aaron late work
David ha msg
Devine worksheets
Vargas msg
Gupta/Schweiger crypto
Jayden lee - readability/verify/pkwd
nassar/sherman excuse decrypt
grigorian pkws
ariana html
herbst arduino
andy lee homepage

8/7 rsa worksheet resubs
8 fix old grades
7 verify worksheet



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
- Ishkanyan (sent)
x Choi - msg
x Nassar - msg
x Paek - msg
x Russel-I - msg
x Halko - msg
- Lane
x Lee, Jinkyu - msg
- Shannon
- Story
x Wong - msg

#8
- Akchyan
- Faubert
- Herbst
- Simonyan
- Baker
- Carone
- Vuletic
- Wiatrak


x Gutierrez
x Hong, Celine
x Kim, Justin
x Lee, Lauren
x Rhee


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
            any suit not match [0]
        is straight?
            sort ranks , if [0] + 4 == [4], straight
                        if [0] == 1, [1] == 10

also great (quick) for comparing hands

----
Archbishop Elder Drift
Harpsichord Debt Rifle

```python
# pip install pycryptodome
from Crypto.PublicKey import RSA
key_pair = RSA.generate(1024) # minimum size
# show p, q
# show n (m), n == p*q
# show d
# show e, why is e 65537 (small enough to be efficient, big enough to be secure)
# fermat prime (2**2**n +1)
print(key_pair.public_key().export_key().decode()) #pub
print(key_pair.export_key().decode()) #priv
#key size
### same process with 2048-bit key
file = open("public.key", "w")
file.write(key_pair.public_key().export_key().decode())
file.close()
file = open("private.key", "w")
file.write(key_pair.export_key().decode())
file.close()
```
# PKCS1_OAEP
Pub key cipher standard - optimal asymmetric encryption padding
add randomness, prevents partial decrypting


----------------------------------------------------------
*I - LEDs
N - 3d prints?
N - pens/rulers/drafting
------------------------------------------
*O - orrery - add motor
*V - motors?
A - tools (more)
---------------------------------
T - circuit boards
I - Lego? 3Dp Rocket? LED Matrix?
*O - infinity mirror
*N - motors

 ---- epoch clock
 ---- binary/hex counter
 ---- Wrap w/wire

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


----
spreadsheets
cybersecurity
    user data
        PII
        cookies
        search/browser history
        geolocation
    attacks
        phishing
        rogue ap
        malware (virus, trojan)
    protocols
    authentication
        passwords
        mfa
encryption

*rainbow
*particle
*baseline
radial
*harmonic

    vignere example - w/one of the keywords?
Vignere key

Send a clue to each encrypted with their private key.
----
#4 transposition leads to next link (8th word)
/rebellion

#5 Find the hidden url in the html source
    links to /wobniar

#6 /wobniar
decrypt AES128 with key: baselineharmonic
found with ottendorf (giancoli)
  301:39:2:1
    110:5:8:3
    803:16:1:8
    232:8:4:4
    760:1:6:8
    81:20:13:2
    791:4:12:1
    511:22:14:6

campbell
        1070:12:1:2
        259:6:5:8
        74:3:6:3
        673:16:2:3
        436:2:5:4
        1108:5:1:5
        387:21:8:6
        915:17:3:1

# 7 /tolkien
keywords encrypted to each person (6 total)
overrun
massive
economic
radiate
approach
dungeon

#8
vignere with keylength 44
order of words?
braille?
hover images (css style)
steganography
    image, message
    clue to online tool: https://stylesuxx.github.io/steganography/

- each word a clue page

# OVERRUN
* main:
    message encrypted with rsa. Give E, but you must find p&q to get D
    p: 419
    q: 307

* result:

* source


# MASSIVE
* main:
    Steganography - image with encoded text

* result:

* source:

# ECONOMIC
* main:

* result:

* source:

# RADIATE
* main:

* result:

* source:

# APPROACH
* main:

* result:

* source:

# DUNGEON
* main:

* result:

* source:

#################### FINAL GOAL
