# Jumia Product Performance Analysis — Excel Dashboard

![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Pivot Tables](https://img.shields.io/badge/Pivot%20Tables-Analysis-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

> Analyzing how pricing, discounts, and customer feedback drive product engagement on Africa's largest e-commerce platform — built entirely in Excel.

---

## The Question I Was Trying to Answer

Do higher discounts actually lead to better product performance? Or is there more to it?

That's what drove this project. Using product-level data scraped from Jumia, I wanted to understand the relationship between pricing strategy, customer ratings, and engagement — and surface which products are genuinely performing versus just appearing to.

---

## Dataset

Product-level data including current price, old price, discount percentage, number of reviews, and customer ratings.

<img width="1306" alt="Dataset preview" src="https://github.com/user-attachments/assets/b2ac0ae4-c6b6-4c58-b900-7ea5eda8e770" />

---

## Data Cleaning

The raw data had a few issues that needed sorting before any analysis could be trusted:

- Price columns had currency symbols embedded as text — stripped and converted to numeric
- Some review counts came in as negative values, which were corrected
- Ratings stored as text strings were cast to numbers
- Missing values in Reviews and Rating columns were handled
- Duplicate product entries removed

<img width="1574" alt="Data cleaning steps" src="https://github.com/user-attachments/assets/eb3158c0-54dc-46ca-907a-2aea6d43fcfd" />

---

## Feature Engineering

Three new columns were created to make the data more useful for segmentation:

**Discount Amount** — difference between old price and current price, giving an absolute figure rather than just a percentage

<img width="1064" alt="Discount amount formula" src="https://github.com/user-attachments/assets/46b4bac5-97cf-4115-9df8-25b80e694aaa" />

**Rating Category** — Poor / Average / Excellent buckets to make ratings easier to filter and visualize

<img width="988" alt="Rating category formula" src="https://github.com/user-attachments/assets/04c54ee8-7e79-43f6-8557-3492bcd6d75a" />

**Discount Category** — Low / Medium / High groupings for the same reason

<img width="935" alt="Discount category formula" src="https://github.com/user-attachments/assets/d9a2c11a-ec4a-4a96-99f4-7592e371b448" />

---

## Analysis

<img width="1387" alt="Analysis overview" src="https://github.com/user-attachments/assets/e0206411-a9c9-41b4-9bb2-1949362a68a9" />

### Descriptive Stats

Starting point was getting a feel for the data — averages for price, discount, and rating; most and least expensive products; how items were distributed across rating and discount categories.

<img width="1518" alt="Descriptive statistics" src="https://github.com/user-attachments/assets/410f1595-82b8-4070-896e-d342382b62f6" />

### Discount vs. Engagement

This is where things got interesting. I looked at whether higher discounts correlated with more reviews (a proxy for customer traffic and purchases). The short answer: somewhat, but not as strongly as you'd expect.

<img width="977" alt="Discount vs reviews chart" src="https://github.com/user-attachments/assets/540d365b-6a70-499d-abe4-2202e9ef741f" />

### Product Performance Rankings

- Top 10 by discount
- Top 10 by number of reviews  
- Top 5 highest-rated and bottom 5 lowest-rated
- Head-to-head: high-discount vs low-discount products on ratings and reviews

<img width="1443" alt="Product performance rankings" src="https://github.com/user-attachments/assets/8f859c57-f50c-4d85-95c3-2b13412be384" />

---

## Dashboard

Built an interactive dashboard with slicers so anyone can explore the data without touching the underlying sheets.

<img width="635" alt="Excel dashboard" src="https://github.com/user-attachments/assets/4f5cde94-3335-4493-9040-c0ef1c74a2f5" />

**What's on it:**
- KPI cards: total products, average rating, average discount, total reviews
- Top products by rating, reviews, and discount
- Scatter plots for discount vs. reviews and rating vs. reviews
- Donut/bar charts for rating and discount category distributions

---

## What I Found

**Discounts drive attention, not loyalty.** Products with the biggest markdowns pulled in more reviews on average — but their ratings weren't higher. People click on a deal; they don't necessarily love what they receive.

**High ratings and high engagement go together.** Well-rated products consistently had more reviews, which suggests trust compounds — customers are more likely to buy (and leave feedback on) something others have already validated.

**Some products are hiding a quality problem behind a discount.** A cluster of items had high discounts but below-average ratings. That's a flag worth flagging to any merchandising team.

**The sweet spot is quality at a fair price** — not the deepest discount, not the flashiest product page.

---

## Tools Used

Excel — specifically: Pivot Tables, XLOOKUP / IF / nested formulas, bar/pie/scatter charts, conditional formatting, and slicers for dashboard interactivity.

---

## Files

```
📂 Jumia_Sales_Excel_Project/
├── 📊 Jumia_Analysis.xlsx      # Main workbook (raw data, cleaned data, analysis, dashboard)
└── 📄 README.md
```
