# **Market Basket Analysis: Understanding Customer Purchase Behavior**

## **Introduction**
In today’s competitive retail landscape, **understanding customer buying patterns is crucial** for boosting sales and enhancing the shopping experience. Using **Market Basket Analysis**, a type of **prescriptive modeling**, I built and deployed my **first Python-based model** to identify frequently bought product combinations—providing insights that help **optimize store layouts, improve promotions, and drive cross-selling**, ultimately increasing **revenue and customer satisfaction**.


## **Why This Market Basket Analysis Project Matters**

**1. Reveals Customer Buying Habits**: 

- It identifies what products customers naturally pair together, giving insight into their true purchasing behavior. 

**2. Drives Cross-Selling Opportunities**: 

- Knowing common product combos helps recommend related items, tagged "Customers also bought..." feature. 

**3. Improves Store Layout & Product Placement**: 

- Place commonly bought-together items near each other (physically or digitally), making purchases more seamless and increasing cart size. 

**4. Powers Targeted Promotions & Bundling**: 

- Businesses can create bundles or run combo discounts to increase sales without guesswork.

**5. Boosts Revenue & Average Order Value (AOV)**: 

- When customers are nudged to buy one more complementary product, revenue climbs without adding new customers. 

**6. Informs Strategic Decision-Making**: 

- Insights from product-pair frequency help marketing, inventory, and pricing teams make smarter, faster decisions. 

**7. Great Entry into Prescriptive Analytics**: 

- This project isn’t just about what has happened, but what should be done next—making it a powerful leap into action-oriented data science. 



## **Files**
-	 [Dataset](https://github.com/olumidebalogun1/Prescriptive-Model-1/blob/main/1.%20Monthly%20Sales%20Dataset.ipynb): The dataset used for this analysis is fictional (synthetically generated) but designed to reflect realistic sales data.

-	[Load and Clean_data](https://github.com/olumidebalogun1/Prescriptive-Model-1/blob/main/2.%20Load%20and%20Clean.ipynb): This is the code I used to extract and clean the data before loading it into the model.

- [Code](https://github.com/olumidebalogun1/Prescriptive-Model-1/blob/main/3.%20Prescriptive%20Model%201%20-%20Market%20Basket%20Analysis.ipynb): The full code covers everything from loading and cleaning the dataset to training the model.



## **I. Key Business Question**

### **What products are frequently bought together**?

## **II. Project Overview**

### **1. Business Challenge**:
The company lacks insights into customer purchasing patterns, specifically which products are frequently purchased together. This makes it difficult to design effective cross-selling strategies, optimize product placements, and increase average order value.

### **2. Project Goal**:
To uncover frequently co-purchased products (pairs and triplets) by analyzing historical transaction data. These insights can inform marketing promotions, in-store layouts, recommendation systems, and bundling strategies.

## **III. Approach**:

**1. Data Cleaning**: 

- Clean and standardize the dataset to remove errors, ensure consistency, and establish a reliable foundation for accurate analysis.

**2. Feature Expansion**:

- Enrich the dataset by adding supplementary columns that provide additional context and enhance the depth of analysis.

**3. Data Preparation**:

- Filter transactions with duplicate Order IDs to focus only on multi-item orders.

**4. Grouping**:

- Aggregate products by Order ID into comma-separated lists.

**5. Combination Analysis**: 

- Use the itertools.combinations and collections.Counter to identify the most common: **Pairs (2-item combinations)** and **Triplets (3-item combinations)**

**6. Output**: 

- Rank the top 20 product pairs and top 10 product triplets based on frequency of occurrence.

**7. Actionable Insights**: 

- Use the results to guide product bundling, personalized recommendations, or promotional campaigns.



## **Market Basket Analysis – Top 20 Product Pairs Most Frequently Purchased Together**
![Market Basket Analysis (Customer Purchase Behavior)](https://github.com/user-attachments/assets/ef8b7847-d60a-4d02-a101-9c7ed2132785)



## **Market Basket Analysis – Top 10 Sets of Three Products Most Commonly Purchased Together**
![Market Basket Analysis 2](https://github.com/user-attachments/assets/ba01104b-d480-4e30-9315-58c355a70841)




## **Key Trends and Insights**

### **1. Accessory & Device Complementarity**

-	Charging cables (USB-C, Lightning) are frequently purchased with their corresponding smartphones:

-	Google Phone and USB-C Charging Cable


-	iPhone and Lightning Charging Cable


This indicates customers often buy chargers when purchasing new phones—either for convenience, compatibility, or replacement.

### **2. Smartphone & Headphones Pairings**

-	iPhones are frequently bought with: Galaxy Buds Headphones or Apple Airpods Headphones.

-	Google Phones and Samsung Phones are also often purchased with Galaxy Buds or Bose SoundSport Headphones.

-	Suggests a strong demand for audio accessories along with smartphones, regardless of brand alignment.

### **3. Redundancy in Pairings**

-	Some pairs appear in both orders, e.g.:

-	('USB-C Charging Cable', 'Google Phone') and ('Google Phone', 'USB-C Charging Cable')

This redundancy reflects Python's combinations() creating unordered tuples. They’re logically the same pair.

## **Strategic Recommendations**

### **1. Bundle Products for Sales Promotions**: 

Offer predefined bundles:

-	iPhone + Lightning Charging Cable + Airpods

-	Google Phone + USB-C Charging Cable + Galaxy Buds

-	These bundles reflect natural purchasing behavior and can increase Average Order Value (AOV).


### **2. Cross-Selling Opportunities**:

Customers who bought this phone also bought this charger/headphone. Especially for high-frequency combos like:

-	Google Phone and USB-C Charging Cable

-	iPhone, Lightning Cable,  and Airpods



### **3. Inventory & Supply Chain Optimization**:

Ensure higher stock levels for frequently co-purchased accessories. Example, for every 100 Google Phones, forecast 90+ USB-C cable sales.


### **4. Product Placement Optimization (In-Store or Online)**:

Place frequently bought-together items close to each other in:

-	Physical stores (e.g., accessories shelf near phone section)

-	Online layout (carousel of “Frequently Bought Together”)

