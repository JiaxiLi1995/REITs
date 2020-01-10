Sector
================
Jiaxi Li

In this file, I will analysis the sector level betas and compare the REITs ones against other sectors. The data here are from Ken French Data Library 49 industry portfolios since 1993.

Load Data
=========

Load FF5.csv and 49\_Industry\_Portfolios.csv

Merge Data, Clean Data, and Regression
======================================

I will merge the data and convert the simple return to log return. Since the graph does not work well, I made it, saved it and then loaded it.

![Here is the coefficient for different sectors](Sectors.png)

Here, I would present the risk premiums distribution for each sector. ![](Sector_files/figure-markdown_github/unnamed-chunk-5-1.png)![](Sector_files/figure-markdown_github/unnamed-chunk-5-2.png)

Plot the time series plot for the betas
=======================================

Using 5 year windows for a time series beta plot ![](Sector_files/figure-markdown_github/unnamed-chunk-6-1.png)

Full Sample Second-Pass Fama Macbeth
====================================

![](Sector_files/figure-markdown_github/unnamed-chunk-7-1.png)![](Sector_files/figure-markdown_github/unnamed-chunk-7-2.png)

With the Cook's Distance estimation, REITs does not seem to pull the factor premium estimation of the second pass Fama Macbeth.

Rolling-Window Second-Pass Fama Macbeth
=======================================

Here, I would apply the 5-year rolling window to estimate the betas and use them to calculate the lambdas for the following month.

![](Sector_files/figure-markdown_github/unnamed-chunk-8-1.png)![](Sector_files/figure-markdown_github/unnamed-chunk-8-2.png)

Even with Rolling Windows, the Cook's Distance estimation shows that REITs does not seem to pull the factor premium estimation of the second pass Fama Macbeth.
