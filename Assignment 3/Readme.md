Instructions

2 datasets for Homework3:

DataSet1 = closes_Quandl_Rolling_EDs.csv

DataSet2 = imm_Quandl_Rolling_EDs.csv

 

Goal: Create a new dataset (DataSet3) with constant-maturity Eurodollar series, interpolated from DataSet1.

DataSet1 contains 20 rolling Eurodollar series (20 quarterly contracts)

Constant maturities: 3m, 6m, 9m..... 4.75y forwards

DataSet2 contains 40 columns of IMM dates for each historical date in DataSet1

Use interpolation (linear or higher-order) for your work, building an interpolant  for every day in the sample.  Please use data from 2005-on, as it's better quality.  Note that a front contract stops trading on Monday before IMM date.

Compare volatility curves (volatility as a function of futures expiry term) generated from DataSet1 and DataSet3, analyze results.

Save DataSet3, as we will use it in future work with Eurodollar estimations.

Note:

If you have a Quandl account, you can access rolling Eurodollars and create your own dataset:

import quandl

token = "xxxxxxxxxx"

n = range(1,21)

nms = ["CHRIS/CME_ED"+str(i) for i in n]

dfs = [quandl.get(nm, authtoken=token) for nm in nms]