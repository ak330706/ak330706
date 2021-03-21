
import datetime
import random
import time

from flask import Flask, jsonify, render_template

dt = str(datetime.datetime.now())  //to convert into string to remoe the character//
dt = dt[09:19]

app = Flask(__name__) /// to run flaask file

buy = 100
buy_volume = 100
sell = 2000
sell_volume = 500

info = {
                "time": dt,
                "buy": buy,
                "buy_volume": buy_volume,
                "sell": sell,
                "sell_volume": sell_volume
            }

@app.route('/update_stocks', methods=['POST'])
def update_stocks():

    buy = 1000
    buy_volume = 100
    sell = 1000
    sell_volume = 100

    dt = str(datetime.datetime.now())
    dt = dt[:19]

    buy = buy + random.randint(-6, 8)
    buy_volume = buy_volume + random.randint(-50, 50)
    sell = sell + random.randint(-6, 8)
    sell_volume = sell_volume + random.randint(-50, 50)

    info = {
        "time": dt,
        "buy": buy,
        "buy_volume": buy_volume,
        "sell": sell,
        "sell_volume": sell_volume
    }
    return jsonify(info)



@app.route('/')
def orderpage():
    return render_template('home.html')

app.run()
