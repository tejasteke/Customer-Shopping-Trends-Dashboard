# 🛍️ Customer Shopping Trends Dashboard (Power BI)

An interactive Power BI dashboard that analyses customer shopping behaviour across Indian retail and e-commerce. It covers revenue by channel, city, month and subscription status, plus discounts, returns, delivery time and review ratings.

![Dashboard Preview](Customer_shopping_Trendss.png)

> Replace the image path above with your dashboard screenshot (for example `images/dashboard.png`).

---

## 📌 Project Overview

Understanding how customers shop helps businesses tune their products, pricing and marketing. This project turns a raw transaction dataset into a single-page dashboard that answers questions like:

- Which channel (online or offline) and which cities bring in the most revenue?
- How much do subscribers contribute compared with non-subscribers?
- How do discounts vary by category and platform?
- Where are returns concentrated?
- How do delivery time and review ratings look across brands and cities?

---

## 📂 Dataset

**Customer Shopping Trends – Indian Dataset** (10,000 customers, January 2023 – December 2024).

> ⚠️ This is a **synthetic dataset** created for learning data analysis. It was generated with a custom Python relational engine designed to mimic the constraints of Indian retail and e-commerce. Patterns in it reflect the generation logic, not real market behaviour.

**Design logic of the dataset**

- **Brand and category logic:** brands only sell what they make (for example, Nike sells activewear and footwear).
- **Platform exclusivity:** flagship sales are tied to their real platforms and months (for example, Big Billion Days on Flipkart in Sept/Oct).
- **Economic tiers:** price = `Base Cost` × `Brand Premium Multiplier`.
- **Logistical integrity:** "Same Day" delivery = 0 days, in-store purchases have no delivery time, and premium brands generally get higher ratings.

**Key columns:** Transaction ID, Customer ID, Purchase Date, Age, Gender, Location, Purchase Channel, Online Store, Category, Item, Brand, Color, Size, Quantity, Purchase Amount (₹), Discount (%), Festival/Sale Event, Shipping Charge (₹), Delivery Speed/Time, Subscription Status, Payment Method, Review Rating, Return Status, Frequency of Purchases, Previous Purchases.

---

## 🧹 Data Cleaning

Rather than dropping columns with missing values, I replaced the blanks to keep all records and fields:

| Column | Issue | Action |
|---|---|---|
| Festival/Sale Event | ~67% empty | Filled the blanks (these are non-sale days, not lost data) |
| Size | 10 blank values | Replaced the blanks instead of removing the column |
| Brand | ~22% empty | Replaced the blanks with `Other` |

---

## 📊 Dashboard Features

**KPI cards**

- Total Purchase Amount: **₹18.90M**
- Online Purchase Amount: **₹14.51M**
- Offline Purchase Amount: **₹4.39M**
- Customer Count: **10K**
- Average Delivery Time: **3.70 days**
- Average Discount: Accessories **32.23%**, Clothing **32.76%**, Footwear **33.71%**

**Visuals**

- Purchase amount by subscription status (donut)
- Purchase amount by month (column chart)
- Purchase amount by location (column chart)
- Average discount by online store and online/offline (bar chart)
- Item count by colour (pie chart)
- Return status by location (pie chart)
- Average review rating by brand, gender and location

---

## 🎛️ Slicers (Interactive Filters)

Four slicers let you filter the whole dashboard and explore the data from different angles:

| Slicer | Type | Options | What it helps you do |
|---|---|---|---|
| **Gender** | Button slicer | Female, Male | Compare purchase behaviour and review ratings by gender |
| **Brand** | Dropdown (searchable) | Enter or pick a brand | Focus on one brand's sales, discounts and ratings |
| **Location** | Dropdown (searchable) | Enter or pick a city | Drill into a single city's revenue and returns |
| **Return Status** | Button slicer | Returned, Not Returned | Separate returned orders from completed ones |

Slicers can be combined. For example, select **Female + Pune + Returned** to see how returned orders from female customers in Pune look across every chart.

---

## 🔍 Key Insights

- **Online dominates:** online sales are about **77%** of total revenue (₹14.51M of ₹18.90M).
- **Subscribers are a minority:** subscribers contribute **30.71%** (₹5.80M) of revenue, while non-subscribers contribute **69.29%** (₹13.09M).
- **Revenue is concentrated in a few cities:** Pune, Chennai, Mumbai, Bangalore, Kolkata, Hyderabad and Delhi lead, each at roughly ₹1.5–1.9M. Cities after Kochi fall below ₹0.7M.
- **Discounts are uniform:** average discount is about 32–34% across categories and platforms.
- **Monthly revenue is steady:** it stays roughly between ₹1.4M and ₹1.8M with no strong seasonal spike.
- **Colour preference is balanced:** each colour accounts for about 8–11% of items purchased.

---

## 🛠️ Tools Used

- **Power BI Desktop:** data modelling, measures and dashboard design
- **Excel / Power Query:** data cleaning and preparation

---

## ⚠️ Limitations

- The dataset is synthetic, so uniform discounts and flat monthly sales are likely artefacts of how the data was generated.
- About 22% of brand values are grouped as `Other`, which limits brand-level analysis.

---

## 🚀 Future Improvements

- Return rate (%) by city instead of the return count pie chart
- Average review rating by brand as a clustered bar chart
- RFM (Recency, Frequency, Monetary) customer segmentation
- Age-group analysis by category
- Delivery time vs. review rating and return analysis
- Year-wise view of festival/sale event impact (for example, Big Billion Days)

---

## 📁 Repository Structure

```
├── Customer_Shopping_Trends.pbix    # Power BI dashboard file
├── Customer_shopping_Trendss.pdf    # Dashboard export
├── dataset.csv                      # Dataset (cleaned)
├── images/
│   └── dashboard.png                # Dashboard screenshot
└── README.md
```

> Adjust file names to match your repository.

---

## 👤 Author

**Tejas Teke**
MCA Student, IMSCDR Ahmednagar | Aspiring Data Analyst
Skills: Python (Pandas, NumPy, Scikit-learn), SQL, PostgreSQL, Power BI, Excel
🌐 Portfolio: [tejasteke.github.io](https://tejasteke.github.io)
"# Customer-Shopping-Trends-Dashboard" 
