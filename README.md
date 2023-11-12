# Github Intro Guide
This is a task for you to get farmilar with Github. You will be asked to replicate a simple code. 


## My RD graph (Bangkok)
![](output/figure/rating_rd_4_Bangkok.png)
### explanation on graph
The fitted line sharply decrease when listings is near rating at 4. 
It differ from the reference figure as the change is positive, showing opposite result. 
### code editing explanation
As the downloaded data ends with .csv instead of .csv.gz, I change the reading function as below
```
for filename in os.listdir(directory):
    if filename.endswith('.csv'):
        file_path = os.path.join(directory, filename)

        with open(file_path, 'rt', encoding='utf-8') as f:
            df = pd.read_csv(f)
###         as the downloaded data is not end with csv.gz, using open is accessable
            
            dataframes.append(df)
```