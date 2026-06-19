# Project 1: Superstore Sales Analysis 📊

## 📌 Overview

This project provides a comprehensive analysis of retail superstore sales data to identify key business trends, top-performing products, and seasonal patterns. The analysis includes data cleaning, exploratory data analysis (EDA), and interactive visualizations designed to support strategic business decisions.

---

## 📊 Dataset Information

| Attribute | Details |
|-----------|---------|
| **Source** | [Kaggle Superstore Sales Dataset](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting) |
| **Records** | 9,800 transactions |
| **Columns** | 18 attributes |
| **Time Period** | 2015 - 2018 |
| **Unique Customers** | 793 customers |
| **Unique Products** | 1,861 products |

---

## 🛠️ Tools & Technologies Used

- **Python 3.x** - Core programming language
- **Pandas** - Data manipulation and cleaning
- **NumPy** - Numerical computations
- **Matplotlib & Seaborn** - Data visualization
- **Jupyter Notebook** - Interactive analysis environment
- **Tableau Public** (Optional) - Interactive dashboards
- **Power BI** (Optional) - Business intelligence dashboards

---

## 📁 Project Structure

```
project-1-superstore/
├── 📄 README.md                              # Project documentation
├── 📄 requirements.txt                       # Python dependencies
├── 📄 .gitignore                             # Git ignore rules
├── 📁 notebooks/
│   └── 📓 superstore_analysis.ipynb          # Main Jupyter Notebook
├── 📁 data/
│   ├── 📊 train.csv                          # Raw data
│   └── 📊 superstore_sales_cleaned.csv       # Cleaned data
└── 📁 images/
    ├── 📷 superstore_eda_visualizations.png  # EDA charts
    ├── 📷 correlation_heatmap.png            # Correlation analysis
    └── 📷 dashboard_preview.png              # Dashboard screenshot (optional)
```

---

## 🧹 Data Cleaning Process

### Issues Identified & Resolved

| Issue | Action Taken | Impact |
|-------|-------------|--------|
| **Missing Postal Codes** | Filled with median value | 11 records recovered |
| **Duplicate Records** | Identified and removed | Data quality improved |
| **Date Format** | Converted to datetime (DD/MM/YYYY) | Enabled time-based analysis |
| **Data Type Issues** | Corrected column types | Improved performance |
| **New Features** | Created Year & Month columns | Enabled temporal analysis |

### Cleaning Steps

```python
1. ✓ Loaded raw data (9,800 rows × 18 columns)
2. ✓ Checked for missing values (Postal Code: 11 missing)
3. ✓ Handled missing values (filled with median)
4. ✓ Removed duplicate records
5. ✓ Converted Order Date & Ship Date to datetime
6. ✓ Created Year and Month columns for analysis
7. ✓ Saved cleaned data to CSV
```

---

## 📊 Key Findings & Insights

### 💰 Revenue Metrics
- **Total Sales**: $2,261,536.78
- **Average Transaction**: $230.77
- **Median Transaction**: $54.49
- **Transactions Analyzed**: 9,800

### 🏆 Top Performers

#### By Category
| Rank | Category | Sales | % of Total |
|------|----------|-------|-----------|
| 1 | **Technology** | $827,456 | 36.6% |
| 2 | Furniture | $728,659 | 32.2% |
| 3 | Office Supplies | $705,422 | 31.2% |

#### By Sub-Category (Top 5)
1. **Phones** - $327,782
2. **Chairs** - $322,823
3. **Storage** - $219,343
4. **Tables** - $202,811
5. **Binders** - $200,029

#### By Region
| Region | Sales | % Share |
|--------|-------|---------|
| **West** | $710,220 | 31.4% |
| East | $669,519 | 29.6% |
| Central | $492,647 | 21.8% |
| South | $389,151 | 17.2% |

#### Top Customers
| Customer | Sales | Notes |
|----------|-------|-------|
| 1. Sean Miller | $25,043 | VIP Customer |
| 2. Tamara Chand | $19,052 | High Value |
| 3. Raymond Buch | $15,117 | High Value |

### 📅 Seasonal Trends
- **Peak Sales Month**: November ($350,162) - Holiday season
- **Lowest Sales Month**: February ($59,371) - Post-holiday slump
- **High Sales Period**: September-November (Q4)
- **Best Year**: 2018 ($722,052 total)

### 📍 Customer Segments
- **Top Segment**: Consumer
- **Shipping Method**: Standard Class dominates (59% of transactions)

---

## 📈 Visualizations

The analysis includes 6 comprehensive visualizations:

1. **Sales by Category** (Bar Chart) - Shows Technology as top revenue driver
2. **Sales Trend by Month** (Line Chart) - Reveals strong Q4 performance
3. **Sales Distribution by Region** (Pie Chart) - West region leads
4. **Top 10 Sub-Categories** (Horizontal Bar Chart) - Phones & Chairs lead
5. **Sales Distribution Histogram** - Right-skewed distribution
6. **Sales by Customer Segment** (Bar Chart) - Consumer segment dominance

Plus:
- **Correlation Heatmap** - Identifies relationships between variables

---

## ✅ Key Recommendations

### 🎯 Strategic Recommendations

1. **Focus on Technology Category**
   - Accounts for 36.6% of total revenue
   - Highest average transaction value ($456)
   - Action: Increase marketing spend & inventory

2. **Expand West Region Operations**
   - Highest regional sales ($710K)
   - Strong growth potential
   - Action: Open distribution centers or expand sales team

3. **Develop VIP Customer Loyalty Program**
   - Top 10 customers generate significant value
   - Sean Miller alone = $25K in sales
   - Action: Create personalized retention programs

4. **Optimize Seasonal Inventory**
   - November is peak sales month ($350K)
   - Plan inventory build-up for September-November
   - Action: Increase stock 2-3 months before peak

5. **Investigate Underperforming Regions**
   - South region at only 17.2% of sales
   - Potential growth opportunity
   - Action: Conduct market analysis & develop regional strategy

6. **Product-Level Optimization**
   - Focus on high-margin products (Phones, Chairs)
   - Consolidate or discontinue low performers
   - Action: Conduct product profitability analysis

---

## 🔄 How to Use This Project

### Prerequisites
```bash
# Install Python 3.x and pip
python --version
pip --version
```

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR-USERNAME/data-analyst-portfolio.git
   cd project-1-superstore
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Open Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

5. **Run the analysis**
   - Open `notebooks/superstore_analysis.ipynb`
   - Run cells in order (Kernel → Restart & Run All)

### Output Files Generated
- `superstore_sales_cleaned.csv` - Cleaned dataset
- `superstore_eda_visualizations.png` - EDA charts
- `correlation_heatmap.png` - Correlation analysis

---

## 📊 Interactive Dashboard

### Tableau Public Version
- **Link**: [Insert Tableau Public Link Here]
- **Features**:
  - Sales by Category (interactive filter)
  - Monthly trend chart (time-based)
  - Regional sales map
  - Top products ranking
  - KPI cards (total sales, avg transaction)

### Power BI Version
- **Link**: [Insert Power BI Link Here]
- **Features**: (Same as Tableau version)

---

## 📚 Learning Resources Used

| Topic | Resource |
|-------|----------|
| Python & Pandas | Kaggle Learn: Python & Data Analysis |
| Data Visualization | Matplotlib & Seaborn documentation |
| Tableau | Tableau Public + YouTube tutorials |
| Power BI | Microsoft Learn: Power BI |
| Data Analysis | Google Analytics IQ & Mode Analytics |

---

## 🎓 Skills Demonstrated

✅ **Data Cleaning & Preparation**
- Handling missing values
- Removing duplicates
- Data type conversion
- Feature engineering

✅ **Exploratory Data Analysis**
- Summary statistics
- Correlation analysis
- Distribution analysis
- Segmentation

✅ **Data Visualization**
- Multiple chart types (bar, line, pie, histogram)
- Professional formatting
- Color-coded insights
- Interactive filters

✅ **Business Insight Generation**
- Identifying trends
- Pattern recognition
- Strategic recommendations
- Data storytelling

---

## 🚀 Next Steps

- [ ] Build interactive Tableau/Power BI dashboard
- [ ] Add SQL queries for deeper analysis
- [ ] Create customer segmentation model
- [ ] Develop forecast model for future sales
- [ ] Add profitability analysis by product
- [ ] Conduct RFM (Recency, Frequency, Monetary) analysis

---

## 📞 Contact & Social

- **GitHub**: [Your GitHub Profile](https://github.com/YOUR-USERNAME)
- **LinkedIn**: [Your LinkedIn Profile](https://linkedin.com/in/YOUR-PROFILE)
- **Email**: your.email@example.com
- **Portfolio**: [Your Portfolio Website](https://your-portfolio.com)

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 📝 Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | 2026-06-19 | Initial project setup & analysis |
| 1.1 | TBD | Add dashboard link |
| 2.0 | TBD | Advanced analytics & forecasting |

---

**Last Updated**: 2026-06-19  
**Project Status**: ✅ Complete (Basic Analysis Phase)

---

## 🙏 Acknowledgments

- Dataset sourced from Kaggle
- Analysis techniques from Google Analytics IQ & Cisco Data Analytics Essentials
- Community support from data analyst communities

---

*This project is part of my Data Analyst Portfolio. I'm continuously learning and improving my skills in data analysis, visualization, and business intelligence.*
