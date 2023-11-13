# Github Intro Guide

This is the complected task of replication. 

## Getting Started

1.Ensure that [git lfs](https://git-lfs.github.com) and Python 3.10 are installed. I use MacOS system and Github online. So, it is recommended to use [Homebrew](https://brew.sh) to install git lfs. 

2. Open a shell to the location where you wish to store the repo. You should avoid storing the repo in a synced directory (i.e., do not store it in a Dropbox, Box, or iCloud folder. Note that on many Macs, the Desktop and Documents folder is synced with iCloud.). Once you have navigated to the location where you wish to store the repo, clone the repository, and navigate to its root.

```bash
git lfs clone https://github.com/sz549/Github_Intro_Guide.git
cd Github_Intro_Guide
git lfs install
```
3. I use Visual Studio Code to edit Python codes, so I choose to refer to public online resource like [Zhihu](https://zhuanlan.zhihu.com/p/624521466). It shows the details on how to link VSC to Github and how to push. 


## Rating RD Design Replication Exercise 



We want to do this RD exercise using the Airbnb public data. The goal is to see whether there is a 
clear jump on sales, as approximated by new reviews, near rating at 4 for listings. The guidance is as below: 

1. Go to [Airbnb public data](http://insideairbnb.com/get-the-data/) and download the Bangkok's listings.csv.gz. However, downloaded file is .csv format. Repeat 3 times to ensure they are quarterly data for the last 12 months. Save the data into the path 'data/raw/Bangkok'. The goal is to construct a panel data with 4 screenshots. 

![](NewYork_screenshot.png)

2. Run the code below for data cleaning. 

```bash
python code/data_cleaning.py
```
3. Run the code below to get the RD graph. 

```bash
python code/rating_rd.py
```

## My RD graph (NewYork)![](output/figure/rating_rd_4.png)

I analysis the data for New York. However, the result shows a negetive effect of rating on sales (rd_estimate = -1.545 <0). The reasons for this result may be some confounding problems or the estimate of sales. I also tried Boston and Amsterdam. The data for Boston is more dense clsoe to the threshold. And there are few data near the threshold for Amsterdam. 
