Options Data Preprocessing Tool
​This script is designed to take raw stock options data  and turn it into a clean dataset ready for machine learning. 
Instead of dealing with messy raw files, this pipeline handles the cleaning, adds technical indicators, and splits the data into sets for training and testing.
​What this script does
​Filters Data: It looks for specific symbols (like NIFTY or BANKNIFTY) and removes any rows that aren't options (CE/PE).
​Cleans Up: It fixes date formats, removes negative prices, and makes sure the column names are consistent.
​Trims Outliers: It removes extreme "junk" values (the top and bottom 1%) so they don't confuse your model.
​Builds Features: It calculates useful trading stats, including:
​RSI (Relative Strength Index)
​Moving Averages (3-day and 5-day)
​Moneyness and Days to Expiry
​OI Trend (Open Interest changes)
​Sets a Target: It creates a "target_direction" column which tells you if the price went up or down the following day.
​Time-Based Split: It splits the data into Train, Validation, and Test sets chronologically. This is important because you can't use future data to predict the past.
