## Stock prices and volatility

[Note: I don't code in R very often, so I apologize in advance for any potential bad practices. Any form of feedback or contribution will be greatly appreciated!]

High volatility in stock prices typically means bad news for investors. In this simple project, I study the close prices and volatility values for a selection of stocks from different industries in order to check for patterns and potential correlations. In particular, I am most interested in studying the relationship between periods of high volatility and their impact on stock prices and monthly returns (i.e. growth) for the given stocks. The simulations include the computation of average close prices by month, which are adjusted for splits; computation of volatility and returns by month, autocorrelation plots for each variable, and cross-correlation between prices and volatility. The autocorrelation function for stock prices shows considerable persistence in the price from one month to the next, but it shows no significant cross-correlation against volatility. The relationship between prices and volatility tends to be negative, but not significant. The exception to this is American Airlines and Delta Airlines, which show a considerable negative correlation against historical volatility. This is a small but interesting result and could lead to further research to determine what other variables are similar between these two stocks which may be causing this apparent correlation.

The data has been extracted and filtered from [Kaggle](https://www.kaggle.com/dgawlik/nyse/data). I selected some S&P 500 companies in three moderately stable industries with moderate growth rates: cable/satellite service companies, restaurants and airlines.

Using this data, I computed monthly averages, monthly returns and volatility for each stock with the help of R and its date handling functionalities. I also used the time series class and its features to find possible correlations.

Computing volatility from the given data involves several steps for which I created a set of functions. I chose to find volatility for every one-month period, but it could be computed for smaller or larger periods as well. Results are in the results folder of this repo.