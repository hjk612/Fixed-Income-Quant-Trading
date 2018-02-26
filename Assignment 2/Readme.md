Build a Jupyter Notebook to do the following: 

- Use the same dataset as HW1( 'CMT-all.xlsx'), and extract [3m, 2y,5y,7y,10y,30y] columns (all 
  the estimation work will be done only on this sub-set of columns)
- Definitions: 
  - Sample1: 2013-2014 history (2 years), 
  - Sample2: 2015-2016 history (2 years).  
  - FLY: 2y-5y+10y
  - Weighted FLY: (2y)*w1-5y+(10y)*w2, w1,w2 are the weights 
  - PCA FLY is the Weighted FLY with weights chosen to make the Weighted FLY PCA1,2-neutral
  - COINT FLY is the Weighted FLY with weights chosen to make the Weighted FLY into the best   
    cointegrated vector
  - NOTE: PCA/Cointegration models will only be estimated in Sample1
- Perform PCA decomposition using Sample1, 5 pts
- Compute Half-Life or Augmented Dickey-Fuller (ADF) test statistic for:
  - FLY in Sample1, 5 pts
  - PCA FLY in Sample1, 5 pts 
  - repeat 1 & 2 in Sample2 (5 pts each, note that weights of the PCA FLY were determined in  
    Sample1)
- Perform Cointegration analysis either by Box-Tiao or Chou-Ng in Sample1, 20 pts.  
 Alternatively, compute a COINT FLY from a level regression, 5 pts
- Compute Half-Life or Augmented Dickey-Fuller (ADF) test statistic for:
  - COINT FLY in Sample1, 5pts
  - COINT FLY in Sample2 (note, that weights of the COINT FLY were chosen using Sample1), 5pts
- Summarize results of 2-4, 5pts
- If you are using pca & cca routines from sklearn (or other packages), pls add methodology 
 description in the comments (-10pts, if no satisfactory comments)
- Submit a Jupyter notebook & html->pdf view of the notebook, using the same naming convention   
  as HW1