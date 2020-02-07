ECC
================
Jiaxi Li

In this file, I will calculate the equity cost of capital. For each 5-year window, I would use the 49 industry portfolios to calculate the risk premiums (from Sector.Rmd), and use asset level data to calculate the individual betas. Then use their product as the equity cost of capital.

Load Data
=========

Load FF5.csv and 49\_Industry\_Portfolios.csv

Examine whether lambda is stationary using time-series plot
===========================================================

![](ECC_files/figure-markdown_github/unnamed-chunk-3-1.png) It seems that the lambdas are really stationary. Therefore, I will use current lamdas, lambdas for the year, as well as historical average lambdas for equity cost of capital estimation.

5-year Rolling Betas
====================

I will calculate the 5-year Rolling Betas for individual REIT.

Different Lambdas
=================

The next step would be calculate the lambdas. I would have three type of lambdas, current month lambda as CurMoLam, current year lambda as CurYrLam, historical average lambda as HistAvgLam.

Check the number of assets in our sample each month and at the end of each year.
================================================================================

![](ECC_files/figure-markdown_github/unnamed-chunk-6-1.png)![](ECC_files/figure-markdown_github/unnamed-chunk-6-2.png)![](ECC_files/figure-markdown_github/unnamed-chunk-6-3.png)![](ECC_files/figure-markdown_github/unnamed-chunk-6-4.png)

Use the Current Month Lambda for Equity Cost of Capita
======================================================

The first way is just use the current month estimated lambda for ECC estimation.

![](ECC_files/figure-markdown_github/unnamed-chunk-7-1.png)

Based on the graph, it seems that the the spread of Risk Premiums (Almost Equity Cost of Capital) are quite similar across the years. (A former test will be conducted later.) In 2008, however, the spread becomes really large suddenly.

Here is the Risk Premiums for desired REITs with different Property Types:

![Here is the Risk Premiums for desired REITs with different Property Types:](CurMoProperty.png)

Here is the Risk Premiums for desired REITs with different Property Subtypes:

![Here is the Risk Premiums for desired REITs with different Property Subtypes:](CurMoSubproperty.png)

Use the Current Year Lambda for Equity Cost of Capita
=====================================================

The first way is just use the current year estimated lambda for ECC estimation.

![](ECC_files/figure-markdown_github/unnamed-chunk-10-1.png)

Based on the graph, it seems that the the spread of Risk Premiums (Almost Equity Cost of Capital) are quite similar across the years. (A former test will be conducted later.) In 2008, however, the spread becomes really large suddenly.

Here is the Risk Premiums for desired REITs with different Property Types:

![Here is the Risk Premiums for desired REITs with different Property Types:](CurYrProperty.png)

Here is the Risk Premiums for desired REITs with different Property Subtypes:

![Here is the Risk Premiums for desired REITs with different Property Subtypes:](CurYrSubproperty.png)

Use the Historical Average Lambda for Equity Cost of Capita
===========================================================

The first way is just use the historical average lambda for ECC estimation.

![](ECC_files/figure-markdown_github/unnamed-chunk-13-1.png)

Based on the graph, it seems that the the spread of Risk Premiums (Almost Equity Cost of Capital) are quite similar across the years. (A former test will be conducted later.) In 2008, however, the spread becomes really large suddenly.

Here is the Risk Premiums for desired REITs with different Property Types:

![Here is the Risk Premiums for desired REITs with different Property Types:](HistAvgProperty.png)

Here is the Risk Premiums for desired REITs with different Property Subtypes:

![Here is the Risk Premiums for desired REITs with different Property Subtypes:](HistAvgSubproperty.png)
