Here is the data set I used:
 https://www.kaggle.com/datasets/bahramjannesarr/goodreads-book-datasets-10m?resource=download&select=book400k-500k.csv

I sampled it down to 50k using the following Python code:
import pandas as pd
df = pd.read_csv("book400k-500k.csv")
df = df.sample(n=50000, random_state=42)
df.to_csv("book_sample.csv", index=False)