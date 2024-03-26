# Coffee Sales Analysis

## Introductions
- Coffee makes the world go around. It is one of my guilty pleasures to have a nice cup of coffee in the morning and enjoy its taste, aroma, and caffeine that will keep me going throughout the day.

- I always had a deep interest in different types of coffee and the market that supplies it, so I decided to explore Coffee Sales to see what insights I could find.


## Coffee Sales Dashboard

![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/76f975dd-8223-43f0-9c44-70821de69fc3)

## Project Overview
- This project aims to find trends and interesting statistics on Coffee supply throughout many Countries. By finding these trends in the data, we could make more data-informed
decisions in the best Coffees to sell to businesses throughout the year.

- By performing data analysis techniques on the orders, customers, and products, I could join information from different sheets and create columns necessary for data analysis.

## Recommendations/Results
1. **Geographic targeting**: We should prioritize the United States, Ireland, and the United Kingdom as they generate the most revenue among other Countries
   
2. **Seasonal shipping plans**: Different coffee types tend to do better based on the seasons, so we should tailor the coffee based on the month
   
3. **Customer Retention**: Promote loyalty cards as they have a higher sales average compared to non-loyalty cards
   
4. **Coffee roast considerations**: Light-roasted coffee performs the best in sales all year round, emphasizing that we should promote light roasts compared to dark and medium roasts
  
5. **Size recommendations**: Between 0.5 kg and 1.0 kg coffee sizes tend to be used and generate the most revenue. 

## Skills used
- Excel - Pivot Tables, XLOOKUP, IF Statements, Match, and Aggregation 

- Dashboard - Line Graphs, Bar Charts, Filters, Timelines, and Styling

## Data Cleaning
Standardize Date to fit Global standards: European countries might get confused between the months and days

![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/c170c538-dbe0-485a-bc84-d7f5e8486e2f)
---->
![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/1233289e-49d3-4825-b51b-cd6d7d32d185)

Created new columns to make sense of abbreviated names:

![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/104a062b-1a1b-49a6-8b76-c763be449ec5)
---->
![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/3f193aff-3f9d-47ee-8c2a-01eae0cb1821)

![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/27a433db-1d9d-4bfa-b67f-57058a78f5f0)
---->
![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/d3ef3b43-c9ef-41c5-b9b4-cadadb151e25)


## Data Analysis
Orders Sheet Results
![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/f036b9ac-2334-478a-94c2-60bd38e311db)
---->
![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/5ce65375-aa55-4add-ab1d-103ad264be8f)

- **Populating Customer Names/Email/Country/Loyalty Card Column in orders sheet using XLOOKUP in customers sheet:**

=XLOOKUP(C2, customers!$A$1:$A$1001,customers!$B$1:$B$1001,,0)

=IF(XLOOKUP(C2,customers!$A$1:$A$1001,customers!C1:C1001,,0)=0,"",XLOOKUP(C2,customers!$A$1:$A$1001,customers!C1:C1001,,0))

=XLOOKUP(C2,customers!$A$1:$A$1001,customers!$G$1:$G$1001,,0)

=XLOOKUP([@[Customer ID]],customers!$A$1:$A$1001,customers!$I$1:$I$1001,,0)

- **Using Index and Match to find Coffee Type/Roast Type/Size all at once from the products sheet:**

=INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!I$1,products!$A$1:$G$1,0))

- **Created three pivot tables for the dashboard and to measure -**

- **Total Sales Over Time -**

![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/5a31c738-528c-4db6-916a-f15ff743f595)

**Top Customers -**

![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/8edc9d2b-d3e2-4c22-a2d3-c9c074c20713)

**
Sales By Country -**

![image](https://github.com/jsonshan/Coffee-Sales/assets/122257933/bbe66ef3-1481-42d7-b305-743932ca61d1)


## Limitations
- This dataset does not go past 2022 unfortunately, so we do not know if this information is accurate for today's Coffee Sales
- There are not enough customers surveyed, only being 1000 customers, meaning there is sampling bias
