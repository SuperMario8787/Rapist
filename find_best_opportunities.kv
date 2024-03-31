import requests
from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.boxlayout import BoxLayout

class CryptoInvestmentApp(App):

    def build(self):
        # Fetch data from the CoinCap API
        api_key = '3cd0b6b8-5ccf-41bf-b3da-5ea0eb77608a'  # Your API key here
        url = 'https://api.coincap.io/v2/assets'
        headers = {'Authorization': 'Bearer ' + api_key}
        response = requests.get(url, headers=headers)

        # Analyze data to determine the best investments
        if response.status_code == 200:
            data = response.json()['data']
            best_investments = self.analyze_data(data)
        else:
            best_investments = ["Failed to fetch data"]
        
        # Create and return the UI
        layout = BoxLayout(orientation='vertical')
        for crypto in best_investments:
            label = Label(text=crypto, halign='center', valign='middle')
            layout.add_widget(label)
        return layout

    def analyze_data(self, data):
        if not data:
            return ["No data available"]

        # Initialize variables to track the best investments
        best_investments = []
        max_market_cap = 1000000000  # Maximum market cap requirement

        # Analyze data to find the best investment opportunities
        for asset in data:
            if 'marketCapUsd' in asset and float(asset['marketCapUsd']) < max_market_cap:
                name = asset['name']
                symbol = asset['symbol']
                price_usd = float(asset['priceUsd'])
                volume_usd_24h = float(asset['volumeUsd24Hr'])
                change_24h = float(asset['changePercent24Hr'])

                # Consider additional factors for analysis
                # Example: Price volatility, project fundamentals, community sentiment, etc.
                # For demonstration purposes, we'll use simple indicators based on available data

                # Example indicator: High trading volume
                if volume_usd_24h > 1000000:  # Adjust threshold as needed
                    best_investments.append(f"{name} ({symbol}): High trading volume")

                # Example indicator: Significant price change in the last 24 hours
                if abs(change_24h) > 5:  # Adjust threshold as needed
                    if change_24h > 0:
                        trend = "increased"
                    else:
                        trend = "decreased"
                    best_investments.append(f"{name} ({symbol}): Price has {trend} significantly")

            if len(best_investments) >= 20:  # Collecting 20 best investments
                break

        if not best_investments:
            return ["No suitable investments found"]

        return best_investments

if __name__ == '__main__':
    CryptoInvestmentApp().run()
