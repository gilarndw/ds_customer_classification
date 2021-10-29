# Data Science Customer Clustering: Overview
* Uaed unsupervised machine learning to create cluster
* Engineered some features and data preparation
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

## Profiling The Cluster
I made the following plots for profiling:

### Plot based on Income

![image](https://user-images.githubusercontent.com/60825743/137197924-a5b828e1-43f1-4887-b7c4-403e432ad3ec.png)

### Plot based on Total Spent

![image](https://user-images.githubusercontent.com/60825743/137198453-fd8f40f6-15f8-44f9-ab7a-01639a9e0c3e.png)

### Plot based on Marital Status

![image](https://user-images.githubusercontent.com/60825743/137198622-da43e4d9-4603-429c-a862-7a48afaa6415.png)

### Plot based on Family Size

![image](https://user-images.githubusercontent.com/60825743/137198638-88abfc20-799b-4d38-ad6a-84719fd080d6.png)

### Plot based on Parenthood

![image](https://user-images.githubusercontent.com/60825743/137198651-e7372506-6d97-4eca-928c-6a57533149c8.png)

### Plot based on Education

![image](https://user-images.githubusercontent.com/60825743/137198665-4e182973-cb9d-4d42-a367-12b177484cca.png)

### Plot based on Age

![image](https://user-images.githubusercontent.com/60825743/137198704-bc01388e-d2d0-483a-b673-c4c05a7f2fc2.png)

## Conclusion

1. Cluster 0:
* majority between age 40 - 55 relatively younger
* most of them graduated
* majority not a parent and don't have kids
* majority spend over 1500 USD with income between 60k - 100k

2. Cluster 1:
* majority on their 50's relatively older
* most of them graduated
* majority a parent with family size of 3
* majority spend over 500 to 1000 with income between 45k - 55k

3. Cluster 2:
* they are the youngest, with average age between early 30's - late 40's
* most of them graduated
* majority a parent with maximum family size of 4
* have the lowest spending, in just below 500 with income below 50k
