# Airbnb-Open-Data-analysisn-Python-
Project Report
Title: Airbnb Data Analysis
Introduction
This report provides an analysis of Airbnb listings using data on prices, room types, neighbourhoods, and reviews. The aim is to understand the distribution of listing prices by neighbourhood, the count of listings by room type, and various other factors that influence the Airbnb rental market.

1. Distribution of Listing Prices by Neighbourhood
Objective: To visualize how rental prices are distributed across different neighbourhoods.

python
Copy code
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(14, 8))
sns.boxplot(x='price', y='neighbourhood', data=df, palette='Set2')
plt.title('Distribution of Listing Prices by Neighbourhood')
plt.xlabel('Price ($)')
plt.ylabel('Neighbourhood')
plt.show()
Findings: This boxplot shows the price distribution for each neighbourhood, indicating variations and outliers.

2. Count of Listings by Room Type
Objective: To determine the distribution of listings across different room types.

python
Copy code
plt.figure(figsize=(12, 6))
sns.countplot(y='room_type', data=df, palette='Set2')
plt.title('Count of Listings by Room Type')
plt.xlabel('Count')
plt.ylabel('Room Type')
plt.show()
Findings: The countplot reveals which room types are most common, providing insight into market trends.

3. Average Price by Neighbourhood Group
Objective: To analyze how the average price varies across different neighbourhood groups.

python
Copy code
plt.figure(figsize=(12, 8))
sns.barplot(x='neighbourhood_group', y='price', data=df, estimator='mean', palette='viridis')
plt.title('Average Price by Neighbourhood Group')
plt.xlabel('Neighbourhood Group')
plt.ylabel('Average Price ($)')
plt.show()
Findings: This barplot shows the average price of listings in different neighbourhood groups, highlighting price disparities.

4. Room Type Analysis
Objective: To understand the distribution of different room types.

python
Copy code
plt.figure(figsize=(12, 6))
sns.countplot(y='room_type', data=df, palette='Set2')
plt.title('Distribution of Room Types')
plt.xlabel('Count')
plt.ylabel('Room Type')
plt.show()
Findings: The countplot shows the frequency of each room type, which can inform about market preferences.

5. Average Price by Room Type
Objective: To compare average prices for different room types.

python
Copy code
plt.figure(figsize=(12, 8))
sns.boxplot(x='price', y='room_type', data=df, palette='coolwarm')
plt.title('Average Price by Room Type')
plt.xlabel('Price ($)')
plt.ylabel('Room Type')
plt.show()
Findings: This boxplot illustrates how prices vary among different room types, indicating price ranges and medians.

6. Number of Reviews by Room Type
Objective: To analyze how the number of reviews varies with room types.

python
Copy code
plt.figure(figsize=(12, 8))
sns.boxplot(x='room_type', y='number_of_reviews', data=df, palette='pastel')
plt.title('Number of Reviews by Room Type')
plt.xlabel('Room Type')
plt.ylabel('Number of Reviews')
plt.show()
Findings: This boxplot shows the distribution of reviews across room types, providing insights into guest activity and feedback.

7. Number of Reviews vs. Price
Objective: To explore the relationship between the number of reviews and listing prices.

python
Copy code
plt.figure(figsize=(12, 6))
sns.scatterplot(x='number_of_reviews', y='price', data=df, alpha=0.5, color='blue')
plt.title('Number of Reviews vs. Price')
plt.xlabel('Number of Reviews')
plt.ylabel('Price ($)')
plt.show()
Findings: This scatterplot examines how the number of reviews correlates with prices, which might indicate how popular or expensive listings are.

