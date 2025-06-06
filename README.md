

# 🗽 NYC Airbnb Market Analysis (June 2024 – May 2025)

## 📌 Project Overview

This project presents a deep dive into New York City's Airbnb market between **June 2024 and May 2025**, highlighting the effects of **Local Law 18**, seasonal travel dynamics, political developments (e.g., 2024 U.S. elections, travel policies), and evolving guest behaviors. It includes **time-series trend analysis**, **property segmentation**, **pricing models**, **sentiment tracking**, and **hypothesis-driven statistical tests**.

> ✅ All data cleaning, feature engineering, statistical analysis, and visualizations were performed by the author.
> 📊 Visual insights are supported by hypothesis tests and regulatory context for robust interpretation.

---

## 📂 Data Source

* **Original Dataset:** [Inside Airbnb – NYC Listings Data (June 2024)](http://insideairbnb.com/get-the-data.html)
* **Data Type:** Detailed snapshot of active Airbnb listings in NYC, including room type, price, minimum nights, host details, reviews, and availability.
* **Temporal Scope:** Time-series augmentation was applied from June 2024 to May 2025 using calendar and review data.

---

## 🎯 Objective

To explore how regulations, seasonality, pricing models, and guest behavior impact the **availability**, **pricing**, and **performance** of Airbnb listings in NYC.

---

## 👥 Who Can Benefit

This project provides actionable insights for:

* **Urban Policy Makers**: Evaluate the effects of Local Law 18 on rental dynamics.
* **Short-Term Rental Investors**: Understand what listing configurations generate the highest revenue.
* **Data Scientists**: Reference a well-structured end-to-end exploratory and statistical analysis pipeline.
* **Travel Economists**: Examine the interplay between policy, travel behavior, and economic indicators.
* **NYC Residents and Hosts**: Assess profitability based on room type, location, and guest group size.

---

## 🧹 Data Cleaning & Processing

Performed by the author. Key steps included:

* Removal of duplicates and null entries.
* Standardization of pricing, minimum/maximum nights.
* Feature engineering for:

  * Host tenure (in years)
  * Availability grouping
  * Property type consolidation
  * Guest sentiment scores (via NLP on guest comments)
* Time-based slicing to enable monthly trend analysis.

---

## 💡 Key Takeaways

* **Availability dropped** below 50% after February 2025, likely driven by regulatory changes and travel slowdowns.
* **Shorter availability windows** (30–60 days) show **higher nightly prices**, indicating better monetization for brief stays.
* **Entire home listings** dominate in revenue, while **private rooms** receive higher guest satisfaction scores.
* Listings with **1–4 night minimums** generate **peak pricing**, whereas 28–30 night listings underperform financially.
* Hosts active for **5–10 years** yield the **highest revenue**; **10–15 year veterans** earn the best ratings.
* **Guest sentiment peaked in February** and fell sharply in March, correlating with political instability.
* **Listings for 1–2 guests** attract higher review sentiment than larger accommodations.
* **Statistical tests confirm** strong relationships between pricing, availability, host tenure, and listing configuration.
* **Listings accommodating 1–2 guests are the most common and attract significantly higher guest sentiment, reflecting NYC’s large influx of solo travelers and small groups.
*  **Many of these smaller guest groups prefer private rooms in shared homes, which offer more affordable pricing and higher satisfaction compared to entire homes.


---

## 📊 Key Visual Insights

### 📈 **1. Time Series Trends: Availability and Price**

From June 2024 to May 2025, **monthly availability** peaked at 68% in November, declining gradually due to policy enforcement and election-related travel slowdowns. **Average prices** ranged from \$139–\$154, dipping during off-seasons and increasing in response to travel announcements.

> 🔍 *Insight*: Trump's travel restrictions in early 2025 likely contributed to decreased availability and a price dip in April.

---

### 🏠 **2. Availability vs. Price by Time Horizon (30/60/90/365 days)**

Heatmaps revealed that **longer-term listings (365 days)** have the highest consistent availability, while **30-day listings** fluctuate more. Higher short-term prices suggest increased profitability under shorter availability windows.

> 💡 *Conclusion*: Hosts targeting short-term stays can command higher nightly prices but must manage lower average availability.

---

### 🧱 **3. Listings vs. Price by Property Type**

Treemaps and boxplots confirmed that:

* **Entire Homes** command the highest prices (avg. \$217)
* **Private Rooms** remain the most affordable (\~\$60–\$75)
* Distribution aligns with **Local Law 18**, which restricts unhosted stays.

---

### 🛏️ **4. Room Types, Availability & Performance**

Entire homes dominate both **volume and revenue**, while private rooms have higher **review scores** due to host presence and guest interaction.

---

### 📆 **5. Minimum Stay vs. Price**

Listings with **1–4 night minimums** yield the **highest average prices** (>\$250), while 28–30 night listings cluster around \$60–\$85, reflecting lower demand for long stays.

> 📘 *Regulatory Factor*: NYC’s Local Law 18 prohibits stays under 30 days without host presence, pushing longer-stay listings into a lower-priced category.

---

### ⭐ **6. Host Tenure vs. Performance**

* **Review ratings** peak for hosts with 10–15 years of experience.
* **Revenue** is highest for those with 5–10 years.
* **Price** tends to increase slightly with host experience, peaking above \$500 for veteran hosts.

---

### 💬 **7. Sentiment Trends (Guest Reviews)**

Sentiment peaked at **0.79 in February 2025**, then fell to **0.56 in March**, aligning with political turbulence. Sentiment partially rebounded by April.

---

## 📈 Statistical Tests & Findings

### ✅ **1. Availability & Price (Next 30 Days)**

* **ANOVA**: F = 11.199, p < 0.001
* **Kruskal-Wallis**: H = 74.995, p < 0.001
  → Prices vary significantly by short-term availability.

---

### ✅ **2. Property Type vs. Price**

* **ANOVA**: F = 70.062, p < 0.001
  → Price significantly depends on property type (e.g., Entire Home vs. Shared Room).

---

### ✅ **3. Room Type vs. Price**

* **ANOVA**: F = 159.066, p < 0.001
  → Entire units have the highest pricing; shared rooms the lowest.

---

### ✅ **4. Guests Accommodated vs. Price**

* **Spearman Correlation**: ρ = 0.719, p < 0.001
  → Strong positive correlation between guest capacity and price.

---

### ✅ **5. Minimum Nights vs. Availability & Price**

* **T-test** shows longer minimum stays (30+ nights) =
  → **Lower availability** (t = 7.107)
  → **Higher prices** (t = 5.781)

---

### ✅ **6. Guest Capacity & Sentiment**

* **T-test**: t = 10.534, p < 0.001
  → Smaller group listings (≤2 guests) have significantly higher sentiment.

---

## 🌇 Policy & Urban Context

* **Local Law 18** restricts short-term rentals unless the host is present and limits occupancy to two guests.
* These rules shift listing dynamics:

  * Increased **private room listings**
  * Decline in **unhosted entire home availability**
  * Encouraged **longer minimum stays**
  * Local Law 18 restricts short-term rentals unless the host is present and limits occupancy to two guests. As a result, private room listings catering to 1–2 guest groups have increased, matching the demand from solo travelers and small parties visiting NYC.
  * Entire home listings have declined in availability due to regulatory constraints, pushing smaller guests toward shared home accommodations.


---

## 📌 Conclusion

This analysis presents an in-depth, data-driven understanding of Airbnb activity in NYC under shifting political, seasonal, and legal conditions. By combining rigorous visualizations with statistical backing, this project offers practical insights for stakeholders navigating the evolving short-term rental landscape. Notably, the majority of Airbnb demand is driven by small groups of one to two guests who frequently choose private rooms in host-present homes due to affordability and regulatory requirements. Local Law 18’s occupancy and host presence restrictions have reshaped the market by reducing unhosted entire home availability and encouraging growth in private room listings. While entire homes generate the highest revenue, private rooms enjoy higher guest satisfaction, reflecting the preferences of NYC’s predominantly solo and duo travelers. These findings provide valuable guidance for policymakers, hosts, and investors aiming to optimize strategies within this dynamic environment.

---

## 🧠 Future Work

* Forecasting availability and pricing using time-series models.
* Spatial analysis with geolocation clusters.
* Integration with economic indicators (e.g., tourism spend, hotel occupancy rates).
* Host classification using clustering (e.g., superhosts, casual hosts).

---

## ✍️ Author

**Qazi Fabia Hoq**


---
## Acknowledgement
This project was completed as part of the Schulich School of Business program at York University. The author thanks the program instructors and peers for their guidance and support throughout the research and analysis process.



