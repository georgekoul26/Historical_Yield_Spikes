# Impacts of Bond Yields on Sector Pricing

## By: Apexa, David, and George

#
The idea for this project came from the current market conditions, in which the 10 year US Treasury Yield has risen very quickly in the past month.  We decided to try and find other historical instances of spikes in the 10yr yield to learn how different sectors were impacted in the short term.  We used APIs to pull data for the bonds and used sector ETFs to represent the different sectors.  This data was then fed through a function which isolated 90 day periods of time after the 10 day rolling momentum off the bond yields eclipsed the level reached in early March of this year. We found 6 such spikes.  This data for each spike was combined together and grouped by sector and by spike.  These new dataframes were exported using pickle files, a technique not covered in class.  The pickle files were imported to another document where the visualizations were created. 

![avg_returns](avg_returns.png)

The above visualization(sector returns) shows the average cumulative returns for each sector in the 90 days after the yield spike.  We can see that all sectors drop in the first month after the yield spike.  Our theory is that this has to do with uncertainty related to inflation fears and monetary policy concerns.

![equalized_avg_returns](equalized_avg_returns.png)

We decided that the best way to see which sectors performed best was to equalize for changes in the SP500.  This was done by subtracting the percent change of the SP500 from the percent change of each sector.  This data was then put into the above plot.  We can see that the financial, consumer discretionary, and industrial sectors perform the best.  The financial sector performing the best makes sense because banks are required to hold a large number of bonds and they are now able to buy them cheaper.  The worst performing sectors were utilities, consumer staples, and healthcare.  One intersting finding is, historically, the consumer discretionary sector performed better than the consumer staples sector.  This is the opposite of what we would have predicted.  