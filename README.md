# Dispersion-Analysis
Analyzing the difference in volatility between an ETF and the underlying holdings.
Inspired by aspects of CBOE's new dispersion index (DSPX) and Longbow's (https://app.mylongbow.com/dashboard) IV Discount metric.

Scrapes an ETFs holdings from Zachs and finds the nearest option expiration to chosen timeframe.
Option data is pulled based on the expiration for all underlying positions and the ETF.

For each strike within the chosen expiry, the difference in option premium between the call & put is calculated. The strike with the lowest difference is chosen.
  If the strike price is greater than the stock price - the call is chosen.
  If the strick price is lower than the stock price - the put is chosen.

"Realized Volatilty" is calculated using price history over the same timeframe as option expiry.

The option data, along with basic info ie. Market Cap & Sector is aggregated into a dataframe.

"IV Discount" and "IV Discount" to ETF are both calculated.

