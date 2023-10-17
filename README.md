# Dispersion-Analysis
Analyzing the difference in volatility between an ETF and the underlying holdings.
Inspired CBOE's new dispersion index (DSPX) and Longbow's (https://app.mylongbow.com/dashboard) IV Discount metric.

Scrapes an ETFs holdings from Zachs and finds the nearest option expiration to chosen timeframe.
Option data is pulled based on the expiration for all underlying positions and the ETF.

Within the chosen expiry, the strike with the lowest difference between call & put premium is chosen.
  If the strike price is greater than the stock price - the call is chosen.
  If the strike price is lower than the stock price - the put is chosen.

"Realized Volatilty" is found using annualized standard deviation of the % change in the stocks price over the same timeframe as option expiry.

The option data, along with Market Cap & Sector is aggregated into a dataframe where "IV Discount" and "IV Discount to ETF" are both calculated.
