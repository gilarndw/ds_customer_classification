# Data Science Customer Classification: Overview
* Explored the data to classify the costumer's background and help the business to understand more about the customer
* Engineered some features for classification
* Customer segmentation based on their background

## Tools and Resourced used
* **Python**: Version 3.7
* **Notebook**: Google Colab
* **Libraries**: pandas, numpy, matplotlib, seaborn, sklearn
* **Datasets**: https://www.kaggle.com/imakash3011/customer-personality-analysis

## Data Preparation
### Attributes

People

* ID: Customer's unique identifier
* Year_Birth: Customer's birth year
* Education: Customer's education level
* Marital_Status: Customer's marital status
* Income: Customer's yearly household income
* Kidhome: Number of children in customer's household
* Teenhome: Number of teenagers in customer's household
* Dt_Customer: Date of customer's enrollment with the company
* Recency: Number of days since customer's last purchase
* Complain: 1 if customer complained in the last 2 years, 0 otherwise

Products

* MntWines: Amount spent on wine in last 2 years
* MntFruits: Amount spent on fruits in last 2 years
* MntMeatProducts: Amount spent on meat in last 2 years
* MntFishProducts: Amount spent on fish in last 2 years
* MntSweetProducts: Amount spent on sweets in last 2 years
* MntGoldProds: Amount spent on gold in last 2 years

Promotion

* NumDealsPurchases: Number of purchases made with a discount
* AcceptedCmp1: 1 if customer accepted the offer in the 1st campaign, 0 otherwise
* AcceptedCmp2: 1 if customer accepted the offer in the 2nd campaign, 0 otherwise
* AcceptedCmp3: 1 if customer accepted the offer in the 3rd campaign, 0 otherwise
* AcceptedCmp4: 1 if customer accepted the offer in the 4th campaign, 0 otherwise
* AcceptedCmp5: 1 if customer accepted the offer in the 5th campaign, 0 otherwise
* Response: 1 if customer accepted the offer in the last campaign, 0 otherwise

Place

* NumWebPurchases: Number of purchases made through the company’s web site
* NumCatalogPurchases: Number of purchases made using a catalogue
* NumStorePurchases: Number of purchases made directly in stores
* NumWebVisitsMonth: Number of visits to company’s web site in the last month

## Data Cleaning
Cleaned the data and added some variables. I made the following changes and modified some of the following features:
* Cleared the Null values from our datasets
* Created Age column and calculate the customer's age
* Calculated total amount of children
* Divide Marital status into 2 categories
* Calculate total family size
* Summed the total money spent
* Divide education level into 3 categories
* Added parenthood column
* Renamed some columns, so it's easier to read
* Deleted some columns that I don't need
* Visually checked the data plot
* Cleared some outliers as seen from data plot

## Data Preprocessing and Clustering
I preprocessed the data to make it more usable for clustering. Here are the following changes I made:
* Converted text data into numeric data with LabelEncoder
* Scaled the data with StandardScaler
* Used K-Means for clustering
* Determined how many centroids with elbow method
* Created clusters column
* Plotted the distribution of clusters
### Clustering
The elbow to help decide how many cluster

![elbow plot](https://user-images.githubusercontent.com/60825743/137193314-d2292592-917e-4cd5-9c98-df503118becf.png)

In this case, I used k=3 because the elbow clear at 3 as I seen

This following image shows the distribution of the cluster:

![cluster distribution](https://user-images.githubusercontent.com/60825743/137194476-2f2b9c7a-8abb-4825-85a7-b0dd25586fa4.png)


.....Under Development

