# 🍽️ Restaurant Analysis 
 
A Power BI dashboard analyzing restaurant performance, consumer demographics, and cuisine preferences. The report provides insights into ratings, customer profiles, and geographic distribution to support data-driven decisions in the food service industry.
 
---
 
## 📊 Dashboard Overview
 
The report is built as a single-page interactive dashboard containing the following visuals:
 
| Visual | Chart Type | Description |
|---|---|---|
| City Food Rating | Ribbon Chart | Overall ratings broken down by city |
| Children Food Rating | Clustered Column Chart | Food ratings segmented by whether consumers have children |
| Parking Rating | Donut Chart | Service ratings by consumer occupation |
| Restaurant Rating by State | Clustered Bar Chart | Overall ratings across different states |
| Consumer's Preference | Pie Chart | Distribution of consumer preferences by rating |
| Restaurant Detail Table | Table | Restaurant name, cuisine type, and overall rating |
 
### KPI Cards
 
Four summary cards are displayed at the top of the report:
 
- **Total Customers** — total number of consumers in the dataset
- **Cuisines** — number of distinct cuisine types available
- **Preferred Cuisine** — the most popular cuisine among consumers
- **Overall Ratings** — aggregate rating metric across all restaurants
---

## Dashboard
<img width="967" height="553" alt="Restaurant Rating Dashboard" src="https://github.com/user-attachments/assets/941e4057-d5d7-4c50-aace-0567d5da8684" />

---
## 🗂️ Data Model
 
The report is powered by five related tables:
 
### `restaurants`
Contains restaurant-level information.
 
| Column | Description |
|---|---|
| `Name` | Restaurant name |
| `State` | State where the restaurant is located |
 
### `consumers`
Contains demographic information about customers.
 
| Column | Description |
|---|---|
| `City` | City of residence |
| `Children` | Whether the consumer has children |
| `Occupation` | Consumer's occupation |
| `Total Customers` | Calculated measure — total customer count |
 
### `ratings`
Contains review and rating data linking consumers to restaurants.
 
| Column | Description |
|---|---|
| `Overall_Rating` | Overall rating score |
| `Food_Rating` | Rating specific to food quality |
| `Service_Rating` | Rating specific to service quality |
| `Overall Ratings` | Calculated measure — sum or average of overall ratings |
 
### `restaurant_cuisines`
Maps restaurants to the cuisine types they serve.
 
| Column | Description |
|---|---|
| `Cuisine` | Type of cuisine offered |
| `Cuisines` | Calculated measure — count of distinct cuisines |
| `Preferred Cuisine` | Calculated measure — most popular cuisine |
 
### `consumer_preferences`
Records cuisine preferences per consumer.
 
| Column | Description |
|---|---|
| `Consumer_ID` | Foreign key linking to the consumers table |
 
