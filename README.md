# 📊 UPI Transaction Dashboard (Excel)

An interactive, single-page **Excel dashboard** that gives a real-time style overview of UPI / online transactions. It lets you slice half a million transactions by city, gender, merchant and category, and instantly see volume, value, success rate, cashback and suspected fraud.

---

## 🖼️ Dashboard Preview

### Full Dashboard (all data)

### Dashboard inside Excel

### Filtered Views (Slicers in action)

| Gender = Male | City = Dwarka (Delhi) |

## 🎯 Objective

To turn raw UPI transaction data into clear, actionable insights:

- How much money is moving, and through which apps, banks and transaction types?
- When (hour / day) do people transact the most?
- Which states and cities drive the highest value?
- How healthy is the system: success vs. failed vs. pending, and how much is flagged as suspicious?

---

## 🧮 Key Metrics (KPI Cards)

| KPI | Value (full dataset) |
|---|---|
| Total Transactions | 502,887 |
| Total Amount (INR) | 44.25 Cr |
| Success Rate | 91% |
| Total Cashback (INR) | 34.6 L |
| Suspected Fraud | 17,089 |

> Transaction status split: **Success 91% · Failed 7% · Pending 2% · Refunded ~0%**

---

## 📈 Dashboard Components

1. **KPI Cards**: total transactions, total amount, success rate, cashback, suspected fraud.
2. **Transaction Amount over Time (Daily)**: area/line chart to spot daily trends and spikes.
3. **Transaction by UPI App**: donut chart showing share of each UPI app.
4. **Transaction by Status**: donut chart for success / failed / pending / refunded.
5. **Transaction Amount by State**: filled map with a ranked state table.
6. **Transaction Amount by Bank Name**: bar chart comparing banks (HDFC, SBI, Kotak, Canara, ICICI, Axis, BoB, PNB).
7. **Transaction Amount by Transaction Type**: P2M, P2P, Bill Payment, Online Shopping, Recharge, Subscription, Wallet Transfer.
8. **Transaction Amount by Hour**: column chart showing peak hours (evening peak around 7 PM).
9. **Hour × Day Heatmap**: conditional-formatted matrix showing when activity is highest across the week.

---

## 🎛️ Filter Panel (Slicers)

- **City**
- **Gender**
- **Merchant Name**
- **Merchant Category**

All slicers are connected to the dashboard's PivotTables, so every chart and KPI updates together.

---

## 🛠️ Tools & Techniques

- **Microsoft Excel**
- **Power Query**: data cleaning and transformation *(update if you used a different approach)*
- **PivotTables & PivotCharts**: aggregation behind every visual
- **Slicers**: interactive filtering
- **Map Chart (Bing)**: state-wise geographic view
- **Conditional Formatting**: hour × day heatmap
- **Custom layout & formatting**: purple theme, icons, card-style KPIs

---

## 🚀 How to Use

1. Open the `.xlsx` file in **Microsoft Excel (2019 / Microsoft 365 recommended)**.
2. Go to the **Dashboard** sheet.
3. Use the **Filter Panel** on the left to filter by city, gender, merchant or category.
4. Click **Clear Filter** (the funnel icon on a slicer) to reset.

> ⚠️ Map charts need Excel 2019+ / Microsoft 365 and an internet connection (Bing Maps).

---

## 🔍 Key Insights

- **P2M (Person-to-Merchant)** is the largest transaction type by value, well ahead of P2P.
- Transaction activity is **highest in the evening (≈ 6–8 PM)**, with a smaller peak around midday.
- The **success rate is ~91%**, so roughly 1 in 11 transactions fails or stays pending.
- Banks are fairly evenly spread, with **HDFC Bank and SBI** slightly on top.
- Daily transaction value stays stable with small spikes, indicating consistent usage.

---

## ⚠️ Challenges & Known Issues

- **Slicer–map conflicts:** the Bing map and its helper pivot sometimes show `#REF!` values when a single city is selected, because the state pivot collapses to one row.
- **KPI formulas on empty selections:** the Success Rate card returns `#REF!` when a filter leaves too little data to divide.
- **Status donut not filtering:** the centre total of the *Transaction by Status* chart stays fixed at the full count, as its pivot isn't linked to every slicer.
- **Heatmap on small selections:** narrow filters can show `###` in the Hour × Day matrix due to column width and sparse data.
- **Performance:** 5 lakh+ rows with multiple pivots and slicers can slow down refresh and filtering.

**Example: City = Bhopal, Gender = Female, Category = Education** (map table and Success Rate show ):


**Yuvraj**
B.Tech (Artificial Intelligence), Sage University, Indore

📫 Connect with me on [LinkedIn](#https://www.linkedin.com/in/yuvraj-singh-kaurav-b025232a8/) 

---

⭐ If you found this project useful, feel free to star the repo!
