# [PYTHON] RFM Analysis
## I. Introduction
### 1. About RFM Analysis
### Why RFM?
- RFM is a marketing analysis technique that stands for Recency, Frequency, and Monetary Value.
  - **Recency**: measures how recently a customer has made a purchase.
  - **Frequency**: measures how often a customer has made purchases.
  - **Monetary Value**: measures the total amount of money a customer has spent on purchases.
- RFM is used to identify and categorize customers based on their purchasing behavior and how recently and frequently they have made purchases, as well as the monetary value of those purchases.
### How?
- In RFM analysis, customers are scored based on three factors (Recency - how recently, Frequency - how often, Monetary - how much), then labeled based on the combination of RFM scores
### This is a transnational data set which contains all the transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail. The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers.
- **InvoiceNo**: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'C', it indicates a cancellation. 
- **StockCode**: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.
- **Description**: Product (item) name. Nominal.
- **Quantity**: The quantities of each product (item) per transaction. Numeric.	
- **InvoiceDate**: Invoice Date and time. Numeric, the day and time when each transaction was generated.
- **UnitPrice**: Unit price. Numeric, Product price per unit in sterling.
- **CustomerID**: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.
- **Country**: Country name. Nominal, the name of the country where each customer resides.
### Reference
- [RFM Analysis For Successful Customer Segmentation](https://www.putler.com/rfm-analysis)

### 2. Business Questions
- The Marketing Department needs to classify the segments of each customer to deploy each marketing program suitable for each customer group.
- The Marketing Director also proposed a plan to use the RFM model in Python to segment customers, and then launch marketing campaigns to thank customers for supporting the company over the past time. As well as exploit potential customers to become loyal customers.
- Suggestions to the Marketing and Sales team with the company's retail model, which of the three indicators R, F, and M should be most interested in?
## II. Data Visualization with Python
- **Distribution of 'Recency', 'Frequency', 'Monetary'**
![image](https://github.com/KayzDo/RFM-Analysis/assets/141127437/1b327cf2-d6af-466c-a3ad-7b545a4cc1e1)

- **Seaborn Countplot of customer segmentation**
![download](https://github.com/KayzDo/RFM-Analysis/assets/141127437/660f90b3-699b-4dc9-8884-36b66f173d98)

- **Bar plot: Total Sales by Segmentation**
![image](https://github.com/KayzDo/RFM-Analysis/assets/141127437/d65909ff-0d40-4d4e-8dc7-086893400844)

- **Build a treemap of customer segmentation**
![image](https://github.com/KayzDo/RFM-Analysis/assets/141127437/ddfd4245-7906-456a-b595-003e9fb54f91)

- **Build a treemap of sales by customer segmentation**
![image](https://github.com/KayzDo/RFM-Analysis/assets/141127437/70c018fe-8f3f-4058-a080-9639366dc372)
## III. Insights
- 1.The most important index of the 3 indicators that the SuperStore company needs to pay attention to is F, then R: because the rate of customers buying once and twice is very high. Very few customers make long-term purchases like 8-9 times or more.
     -> That shows that the customer retention rate at the company is still low.
     
- 2.About Customer Segmentation: The company is mainly "New Customers" >"Hibernating customers">"Lost customers".
    -> This again shows that we need to pay attention to the index F.
  
- 3.Revenue and profit from "New Customers" is the highest.

- 4.The revenue in the East region is the lowest compared to the other 3 regions.

- 5.California, Texas, Illinois vs Florida are the states with the most orders.

- 6.The company's main customers are Consumers accounting for 52%, Corporate: 30% and finally Home Office.

- 7.The categories with the most orders are "Office Supplies" up to 60%, then "Furniture".

- 8.The main subcategory are: Paper(14%), Binders(15%), Art(9%), Phones and Storage (8%).
## IV. Definition and recommended action for each customer segment:

| Segment | Characteristics | Recommendation |
| :-: | :-: | :-: |
| Champions | Bought recently, buy often and spend the most! | Reward them. Can be early adopters for new products. Will promote your brand. |
| Loyal | Spend good money with us often. Responsive to promotions. | Upsell higher value products. Ask for reviews. Engage them. |
| Potential Loyalist | Recent customers, but spent a good amount and bought more than once. | Offer membership / loyalty program, recommend other products. |
| New customers | Bought most recently, but not often. | Provide on-boarding support, give them early success, start building relationship. |
| Promising | Recent shoppers, but haven’t spent much. | Create brand awareness, offer free trials |
| Need attention | Above average recency, frequency and monetary values. May not have bought very recently though. | Make limited time offers, Recommend based on past purchases. Reactivate them. |
| About to sleep | Below average recency, frequency and monetary values. Will lose them if not reactivated. | Share valuable resources, recommend popular products / renewals at discount, reconnect with them. |
| At risk | Spent big money and purchased often. But long time ago. Need to bring them back! | Send personalized emails to reconnect, offer renewals, provide helpful resources. |
| Cannot lose them | Made biggest purchases, and often. But haven’t returned for a long time. | Win them back via renewals or newer products, don’t lose them to competition, talk to them. |
| Hibernating customers | Last purchase was long back, low spenders and low number of orders. | Offer other relevant products and special discounts. Recreate brand value. |
| Lost customers | Lowest recency, frequency and monetary scores. | Revive interest with reach out campaign, ignore otherwise. |
