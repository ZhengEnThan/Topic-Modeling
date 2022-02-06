# Topic Modeling Using LSA and LDA

<br>
The t-SNE clusters of the 10 topics recognized by the LSA technique. We can see that this technique does not categorize the passages into topics very well.
<p align="center">
<img width="715" alt="Screenshot 2022-02-06 at 4 35 09 PM" src="https://user-images.githubusercontent.com/46462603/152706423-373ce6a3-365f-461b-aca0-3e34b47b0c10.png">
</p>

<br>
The t-SNE clusters of the 10 topics recognized by the LDA technique. The passages are categorized into 10 topics more evenly.
<p align="center">
<img width="706" alt="Screenshot 2022-02-06 at 4 35 24 PM" src="https://user-images.githubusercontent.com/46462603/152706553-38ce9ced-408f-44d2-b16a-d09034c48e2a.png">
</p>

<br>
The interactive display showing the 10 topics and the most frequently occurred words. 
<p align="center">
<img width="1221" alt="Screenshot 2022-02-06 at 4 35 44 PM" src="https://user-images.githubusercontent.com/46462603/152706655-1122f117-a43c-4f56-be52-30a388804fcc.png">
</p>

<br>
If you hover over a topic (a circle with a number in it on the left side of the display), the bar charts on the right will be updated, showing the most frequently occurred words in the chosen topic in red.
<p align="center">
<img width="1223" alt="Screenshot 2022-02-06 at 4 43 20 PM" src="https://user-images.githubusercontent.com/46462603/152706662-20f137e8-936f-4028-9214-d81d8f76d9f6.png">
</p>

## Goal
- To implement topic modeling to categorize the passages in the RACE dataset into 10 topics and determine the most frequently used words in each topic.
- To compare the performances of LSA and LDA in topic modeling. 

## Dataset
The RACE dataset is a large-scale reading comprehension dataset with more than 28,000 passages and nearly 100,000 questions. The dataset is collected from English examinations in China, which are designed for middle school and high school students. The dataset can be downloaded from <a href="https://www.cs.cmu.edu/~glai1/data/race/" target="_blank">here</a>.

## Code, files, or folders needed to run the program
- <a href="https://github.com/ZhengEnThan/Topic-Modeling/blob/main/Topic_Modeling_with_LSA_and_LDA.ipynb" target="_blank">Topic_Modeling_with_LSA_and_LDA.ipynb</a>
- documents.csv, which is the RACE dataset that can be downloaded from <a href="https://www.cs.cmu.edu/~glai1/data/race/" target="_blank">here</a>

## How to use the program
Simply run the program cell by cell to import the library, load the data, process and inspect the data, and then apply topic modeling using LSA as well as LDA on the data. 

There are comments in each code cell that tell you what the code cell does and the code cells are also grouped under different markdowns that specify what the code cells do.

If you want to use another dataset, edit the code cell directly below the markdown "Getting the data".

```python
documents = pd.read_csv("documents.csv")
print("There are ", len(documents), " documents in total.\n")
print("The first 5 rows of the dataset are:\n")
print(documents.head())
```

Change "documents.csv" in the code cell above to the file name of your dataset. Make sure that your dataset is such that there is only 1 column where each entry is a passage. If your dataset is not in the csv format, you would have to change the function pd.read_csv() as well. 
