# Meteorite Project
Goal:

The goal of my project is to build an accurate simulation of meteorites falling to Earth. The purpose of this is to predict when the next dangerous to catastrophic meteorite will fall to Earth. If we know the approximate year that it will drop, we will have a better chance of locating it and completing a mission similar to DART to divert the meteor.

Data description and summary of EDA:

The dataset comes from NASA. I have modified it so that it is now a list of every meteorite that has hit the Earth and been recorded since 1974. Some significant columns are year, the year the meteorite fell, and mass, the weight of the meteorite in lbs. The EDA showed it is difficult to find any trends in when meteorites fall and how much they weigh. The amount of meteorites that fall a year is depicted below. It shows spikes and dips in the amount of meteorites that fall a year and they seem to happen at random. Further analysis found that although the distribution of meteorite masses is heavily right skewed, the distribution of the log of meteorite masses is about normal.

Methods:

The first method that I tried used the average drop rate of the meteorites recorded in the original dataset, which included data from the year 600- 2013. This value was used as a baseline to simulate how many meteorites would drop a year. The masses of those meteorites were chosen from a list of possible meteorite sizes and the drop rate of each of those sizes. The results were not accurate.

My next method used a subset of the data that started in 1974 instead of the year 600. This is because meteorite recording wasn’t as frequent until around this year, so using data from before this time

skewed my results. The simulation was not a very good predictor of count or mass because it lacked variation.

My next method used the same 1974 dataset, but instead of using the average drop rate in the simulation, I have switched to using a random number generator that picks from a normal distribution that is centered around the mean meteorite drop rate per year and uses the standard deviation of meteorite drop rates per year. The results yielded much more variation than the previous simulations that more accurately depict the actual meteorite drop rates. A solution is still needed for variation in mass.

My final method used the same method to predict count, but used the mean and standard deviation of the distribution of log meteorite masses to choose a random gaussian number that represents a predicted log(mass). This number was then converted into a regular mass.

Results:

My simulation created a table of the top 10 most massive meteorites that will fall in the next 100 years. These results suggest that the most catastrophic meteorite will be in the year 2042 and it will weigh over 24 million pounds.
