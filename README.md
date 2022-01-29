# fintech_challenge_5
This project includes a financial planner for emergencies, which allows members to use tools to visualize their current savings. Members can also utilize the emergency planner to determine if they have enough money in their emergency fund. This project also includes a second financial planner that specializes in retirement. This planner will forcast your retirement portfolio for the next 30 years. Then the program will create a more volatile 10 year retirement portfolio and allow you to compare the two portfolio's data together.

---
## Technologies
This program is run in Jupyter Notebook and uses the python coding language.

Here is the list of required libraries:
- os
- requests
- json
- pandas
- dotenv
- alpaca_trade_api
- MCForecastTools
- matplotlib

![](/screen_caps/import_1.png)
 
---
## Installation Guide
This program requires a .env file that contains both an Alpaca API key and a secret key in order to import the necessary data. Besides the .env file and installing the required libraries on your local machine, you are ready to go!

---
## Usage
In the first step we set the amount of BTC and ETH owned in the portfolio.

![](screen_caps/step_1.png)

Next we find the current value of each cryptocurrency by selecting it through their individual response dataset from the API call.

![](screen_caps/step_2.png)

We then use the current price data with the total amount of BTC and ETH in the portfolio to determine the total value of cryptocurrency in the portfolio.

![](screen_caps/step_3.png)

The program now allows the input of the total SPY and AGG shares held in the portfolio.

![](screen_caps/step_4.png)

For the next step we have the option to set the start and end date to any timeframe you choose to focus on. 

![](screen_caps/step_5.png)

We utilize Alpaca to turn the API data into a dataframe which displays the open, high, low, close, and volume of both AGG and SPY over the specified start and end date.

![](screen_caps/step_6.png)

The program now uses the total amount of stocks and bonds held in the portfolio with the current value of AGG and SPY to determine the total current value of stocks and bonds held in the portfolio.

![](screen_caps/step_7.png)

Next the total current value of the portfolio is determined by adding the total current value of stocks and bonds with the total current value of cryptocurrency held in the portfolio.

![](screen_caps/step_8.png)

We then use a pie chart to visualize the portfolio weight for crypto vs. stocks/bonds.

![](screen_caps/step_9.png)

Now we have the option to set the emergency fund value appropriately, by default it is set to 3 * monthly income.

![](screen_caps/step_10.png)

The program now uses the total portfolio value and the emergency fund value to determine if you have reached your emergency fund goal.

![](screen_caps/step_11.png)

Here is an opportunity to set the start and end dates for the historical closing prices data that we will be using to create our 30 and 10 year Monte Carlo simulations.

![](screen_caps/step_12.png)

After the 500 Monte Carlo simulations run the program then visualizes the 30 year simulation data as a line plot.

![](screen_caps/step_13.png)

Now the program uses the exact same data but visualizes it as a histogram in order to display the distribution.

![](screen_caps/step_14.png)

The program now provides a summary of the 30 year Monte Carlo simulation data.

![](screen_caps/step_15.png)

Here the program utilizes the summary to multiply the 95% upper and lower CI by the total value of stocks/bonds in the portfolio to display the 30 year retirement investment potential for the stock/bond portion of the portfolio.

![](screen_caps/step_16.png)

Once again the program visualizes another simulation but this simulation only evaluates the investment over 10 years rather than the 30 years we had just previously seen.

![](screen_caps/step_17.png)

The program now visualizes the 10 year Monte Carlo simulation as a histogram.

![](screen_caps/step_18.png)

Here the summary of the 10 year Monte Carlo simulation is printed.

![](screen_caps/step_19.png)

Once again the program utilizes the summary to multiply the 95% upper and lower CI by the total value of stocks/bonds in the portfolio to display the 10 year retirement investment potential for the stock/bond portion of the portfolio.

![](screen_caps/step_20.png)


---
## Contributors
Kevin Gross

---
## License
MIT license
