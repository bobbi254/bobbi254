import alpaca_trade_api as tradeapi

# Replace these with your own API keys
API_KEY = 'YOUR_API_KEY'
API_SECRET = 'YOUR_API_SECRET'
BASE_URL = 'https://paper-api.alpaca.markets'  # Use the paper trading (simulated) environment for testing

# Create an Alpaca API connection
api = tradeapi.REST(API_KEY, API_SECRET, BASE_URL, api_version='v2')

# Define the stock you want to retrieve data for
symbol = 'AAPL'

# Get the latest price data for the stock
latest_price = api.get_latest_trade(symbol=symbol)

# Print the latest price
print(f'Latest price for {symbol}: ${latest_price.price}')
