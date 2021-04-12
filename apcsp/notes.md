Meeting ID: 968 2612 4262
Passcode: 083094

# repo token
a8d550aad48e79d21b29b0fc9549d4b432873b1c
----


# generate key pairs
openssl genrsa -des3 -out private.pem 4096
openssl rsa -in private.pem -pubout -out public.pem
# sign
openssl dgst -sign private.pem -out test.c.sign test.c
# verify
openssl dgst -verify public.pem -signature test.c.sign test.c

## 8th

Post calculation example


Physics

## 7th
* Intro to flask
    * application.py
    * pages, inserting values (random)
    * request parameters (name)
    * templates

# 8th
* Arduino cont'd
    * 7 segment - explain bitmasks, use
    * Homework assignment


---

* Discussion, questions
* Code example
* Questions:

* Should cryptocurrency be regulated by the government? Which government?
* Cryptocurrency proponents say the energy costs are justified by the benefits in economic freedom. Do you agree or disagree?

---


"♥", "♣", "♠", "♦"
card = {"rank": 5, "suit": "♣"}
deck = [{"rank": 5}, "suit": 0}, {"rank": 11, "suit": 3}]

class Card:
    pass

c = Card()
c.rank = "King"
c.suit = "Hearts"


## APCSP
peer-grade
next unit after web
daily vids?

-----------------------------

# INTERVENTIONS

#7
Min
Russel-isaacs

xx Kashani - mom replied
x Casillas
xx Ramirez - spoke 3/9 4pm, come for more help (recent death in family)
x Yawakim
Lee, Edward
x Story - dad, encourage ofc hrs
x Vaysberg
xx Gracie - almost 3 weeks - mom & dad, depression, will try


Parent conf
----------
xMejia
    mom
xChrisman
    dad
xAltamirano - after 4pm
    mom


-------
from flask import Flask, session, render_template, redirect, request

app = Flask(__name__)
app.secret_key = "foo"

@app.route("/")
def index():
    if "username" in session:
        return render_template("index.html", name=session["username"])
    else:
        return "not logged in"

@app.route("/login", methods=["GET", "POST"])
def login():
    if request.method == "POST":
        session["username"] = request.form["username"]
        return redirect("/")
    return render_template("login.html")

@app.route("/logout")
def logout():
    session.pop("username")
    return redirect("/login")