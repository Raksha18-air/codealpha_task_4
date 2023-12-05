# codealpha_task_4
#codealphatask_4
import ccxt
import time
exchange=ccxt.binance({
    'apiKey':'YOUR_API_KEY',
    'secret':'YOUR_SECRET_KEY',
})
def place_buy_order(symbol,amount,price):
    try:
        order=exchange.create_limit_buy_order(symbol,amount,price)
        print("Buy OrderPlaced:",order)
        return order['id']
    except Exception as e:
        print("Failed to place buy order",e)
        return None
def place_sell_order(symbol,amount,price):
    try:
        order=exchamge.create_limit_sell_order(synbol,amount,price)
        print("Sell order placed",order)
        return order['id']
    except Exception as e:
        print("Failed to place sell order",e)
        return None
if __name__=="__main__"|
    symbol='BTC/USDT'
    buy_price=50000
    sel_price=55000
    quantity=0.001
    buy_order_id=place_buy_order(symbol,quantity,buy_price)
    time.sleep(10)
    sell_order_id=place_sell_order(symbol,amount,sell_price)
