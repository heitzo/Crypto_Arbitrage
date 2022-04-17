## Crypto_Arbitrage
# Financial analysis to determine if any arbitrage opportunities exist for Bitcoin.

Welcome! For this project, you'll take on the role of an analyst at a high-tech investment firm. The vice president (VP) of your department is considering arbitrage opportunities in Bitcoin and other cryptocurrencies. As Bitcoin trades on markets across the globe, can you capitalize on simultaneous price dislocations in those markets by using the powers of Pandas?

For this assignment, you’ll sort through historical trade data for Bitcoin on two exchanges: Bitstamp and Coinbase. Your task is to apply the three phases of financial analysis to determine if any arbitrage opportunities exist for Bitcoin.

This project has 3 phases:

1. Collect the data.

2. Prepare the data.

3. Analyze the data.

# Phase 1: Collect the data

1. Using the Pandas read_csv function and the Path module, import the data from the csv file, and create a DataFrame. Set the DatetimeIndex as the Timestamp column, and be sure to parse and format the dates.

2. Use the head (and/or the tail) function to confirm that Pandas properly imported the data.

3. Repeat Steps 1 and 2 for any other csv files you want to import.

## Phase 2: Prepare Data

1. For the DataFrame you created, replace or drop all NaN, or missing, values.

2. Use the str.replace function to remove the dollar signs from the values in the Close column.

3. Convert the data type of the Close column to a float.

4. Review the data for duplicated values, and drop them if necessary.

5. Repeat Steps 1–4 for the any other dataframes you have created DataFrame.

## Phase 3: Analyze the data

1. Choose the columns of data on which to focus your analysis. Use loc or iloc to select the following columns of data for both the bitstamp and coinbase DataFrames: 'Timestamp' (index) and 'Close'

2. Get the summary statistics using the .describe() method. Using the loc and plot functions, plot the price action of the assets on each exchange for different dates and times. In another plot, overlay the visualizations that you created for teh dataframes. Be sure to adjust the legend and title for this new visualization. Did the degree of spread change as time progressed?

3. Focus your analysis on specific dates. Select three dates to evaluate for arbitrage profitability. Choose one date that’s early in the dataset, one from the middle of the dataset, and one from the later part of the time period. For each of the three dates, generate the summary statistics and then create a box plot. This big-picture view is meant to help you gain a better understanding of the data before you perform your arbitrage calculations. As you compare the data, what conclusions can you draw?

4. Calculate the arbitrage profits: 
    1. For each of the three dates, measure the arbitrage spread between the two exchanges by subtracting the lower-priced exchange from the higher-priced one. Then use a conditional statement to generate the summary statistics for each arbitrage_spread DataFrame, where the spread is greater than zero.
    2. For each of the three dates, calculate the spread returns. To do so, divide the instances that have a positive arbitrage spread (that is, a spread greater than zero) by the price of Bitcoin from the exchange you’re buying on (that is, the lower-priced exchange). Review the resulting DataFrame.
    3. For each of the three dates, narrow down your trading opportunities even further. To do so, determine the number of times your trades with positive returns exceed the 1% minimum threshold that you need to cover your costs.
    4. Generate the summary statistics of your spread returns that are greater than 1%. How do the average returns compare among the three dates?
    5. For each of the three dates, calculate the potential profit, in dollars, per trade. To do so, multiply the spread returns that were greater than 1% by the cost of what was purchased. Make sure to drop any missing values from the resulting DataFrame.
    6. Generate the summary statistics, and plot the results for each of the three DataFrames.
    7. Calculate the potential arbitrage profits that you can make on each day. To do so, sum the elements in the profit_per_trade DataFrame.
    8. Using the cumsum function, plot the cumulative sum of each of the three DataFrames. Can you identify any patterns or trends in the profits across the three time periods?

## Learning Objectives:
Pandas is a powerful addition to your fintech toolbox. You can now:
1. Collect data by importing CSV files into Pandas DataFrames.
2. Prepare and clean data for analysis by using Pandas functions.
3. Generate summary statistics for a DataFrame.
4. Create and customize plots from a DataFrame.
5. Select specific data for a close analysis.
6. Explain the role of time in financial analysis.
7. Perform a time series analysis.
