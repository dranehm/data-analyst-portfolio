# 📊 Tableau Dashboard Creation Guide

Complete step-by-step guide to build your interactive Superstore Sales dashboard.

---

## 🚀 Quick Start

**Time Required**: 1.5-2 hours  
**Difficulty**: Beginner-Friendly  
**Cost**: FREE (Tableau Public)

---

## 📥 Step 1: Download & Install Tableau Public

1. **Go to**: https://public.tableau.com/
2. **Click**: "Download Tableau Public" (blue button, top right)
3. **Choose**: Windows or Mac version
4. **Run** the installer and follow prompts
5. **Launch** Tableau Public when installation completes

---

## 📂 Step 2: Prepare Your Data File

Your cleaned CSV is already created: `superstore_sales_cleaned.csv`

**Location**: `d:\Superstore Sales\project-1-superstore\data\superstore_sales_cleaned.csv`

✅ Make sure you have this file ready!

---

## 🎨 Step 3: Create a New Workbook

1. **Open** Tableau Public
2. **Click**: "Create a visualization" OR "File" → "New"
3. **Click**: "Connect to Data"
4. **Choose**: "Text File"
5. **Navigate** to: `d:\Superstore Sales\project-1-superstore\data\superstore_sales_cleaned.csv`
6. **Select** the file and click "Open"
7. **Wait** for data to load (you'll see a preview)
8. **Click**: "Sheet 1" (bottom) to start creating

---

## 📊 Sheet 1: Sales by Category (Bar Chart)

### Setup:
1. **In the main canvas area**, you should see:
   - **Dimensions** (left side): Category, City, Country, etc.
   - **Measures** (left side): Sales, Quantity, Row ID, etc.

### Create Bar Chart:
1. **Drag** `Category` → Columns shelf (top)
2. **Drag** `Sales` → Rows shelf (left)
3. **Click** "Show Me" (right side) → Select "Bar Chart"
4. **Right-click** the chart → "Format" → Add title: "Sales by Category"

### Result:
You should see three bars: Technology, Furniture, Office Supplies

**Rename Sheet**: Right-click "Sheet 1" → Rename to "Sales by Category"

---

## 📈 Sheet 2: Sales Trend by Month (Line Chart)

1. **Click**: "+" (bottom, next to sheet tabs) → "New Sheet"
2. **Drag** `Month` → Columns shelf
3. **Drag** `Sales` → Rows shelf
4. **Click** "Show Me" → Select "Line Chart"
5. **Add title**: "Sales Trend by Month"
6. **Rename** sheet to "Monthly Trend"

### Format the line:
1. **Right-click** the line → "Format"
2. **Make it thicker**: Line Thickness → Automatic or choose thickness
3. **Add data labels**: Right-click line → "Show data labels"

---

## 🏆 Sheet 3: Top 10 Sub-Categories

1. **Create** new sheet
2. **Drag** `Sub-Category` → Rows shelf
3. **Drag** `Sales` → Columns shelf
4. **Click** "Show Me" → "Horizontal Bar Chart"
5. **Sort** descending: Click axis → Sort Descending
6. **Limit to top 10**:
   - Right-click `Sub-Category` pill (Rows)
   - "Filter" → "Top" → "Top 10 by Sales"
7. **Add title**: "Top 10 Sub-Categories"
8. **Rename** sheet to "Top Products"

---

## 🗺️ Sheet 4: Sales by Region (Pie Chart)

1. **Create** new sheet
2. **Drag** `Region` → Color shelf
3. **Drag** `Sales` → Size shelf
4. **Click** "Show Me" → "Pie Chart"
5. **Add labels**:
   - Right-click pie chart
   - "Show data labels"
   - Select "Percent of total"
6. **Add title**: "Sales Distribution by Region"
7. **Rename** sheet to "Regional Sales"

---

## 👥 Sheet 5: Sales by Segment (Bar Chart)

1. **Create** new sheet
2. **Drag** `Segment` → Columns shelf
3. **Drag** `Sales` → Rows shelf
4. **Click** "Show Me" → "Bar Chart"
5. **Color by segment**:
   - Drag `Segment` → Color shelf
6. **Add title**: "Sales by Customer Segment"
7. **Rename** sheet to "Customer Segment"

---

## 💰 Sheet 6: KPI - Total Sales (Single Number)

1. **Create** new sheet
2. **Drag** `Sales` → Text shelf
3. **Click** "Show Me" → "Number Card"
4. You should see a large number (around $2.26M)
5. **Add title**: "Total Sales"
6. **Format**: 
   - Right-click number
   - Format → Font size (make it BIGGER)
7. **Rename** sheet to "KPI - Total Sales"

---

## 💳 Sheet 7: KPI - Average Transaction

1. **Create** new sheet
2. **Drag** `Sales` → Text shelf
3. **Click** the `Sales` pill (on Text) → "Average"
4. **Click** "Show Me" → "Number Card"
5. **Add title**: "Average Transaction Value"
6. **Format**: Increase font size
7. **Rename** sheet to "KPI - Avg Transaction"

---

## 🎯 Step 4: Create Dashboard

1. **Click** the "+" icon (bottom) → **"New Dashboard"**
2. **You should see**:
   - Left sidebar with your sheets listed
   - Empty white canvas (dashboard area)
   - Toolbar at top

### Add Sheets to Dashboard:

1. **Drag** "Sales by Category" sheet → Top-left corner of dashboard
2. **Resize**: Drag corners to make it smaller (about 1/3 of width)
3. **Drag** "Monthly Trend" → Top-right (next to Category chart)
4. **Resize** to match size
5. **Continue adding**:
   - "Top Products" → Bottom-left
   - "Regional Sales" → Bottom-middle
   - "Customer Segment" → Bottom-right
   - "KPI - Total Sales" → Top (between the two bar charts)
   - "KPI - Avg Transaction" → Top

### Layout:
```
┌─────────────────┬──────────────┬──────────────┐
│ Total Sales KPI │ Avg Trans KPI│              │
├─────────────────┼──────────────┤              │
│   Category      │  Monthly     │   Segment    │
│    Sales        │    Trend     │    Sales     │
├─────────────────┼──────────────┼──────────────┤
│   Top Products  │  Regional    │              │
│                 │   Sales (Pie)│              │
└─────────────────┴──────────────┴──────────────┘
```

---

## 🎨 Step 5: Add Filters to Dashboard

Filters make your dashboard interactive!

### Add Category Filter:

1. **On Dashboard**, click "Sales by Category" chart
2. **Right-click** → "Use as Filter"
3. Now clicking a category on one chart filters all connected charts!

### Add Region Filter:

1. **Click** "Regional Sales" (pie chart)
2. **Right-click** → "Use as Filter"
3. Now you can click regions to filter all data

### Add Year Filter (Optional):

1. **Add** a new sheet with just `Year` as a filter
2. **Use** as filter on dashboard
3. Now you can filter by specific years (2015-2018)

---

## ✨ Step 6: Format & Polish Dashboard

### Add Title:
1. **Click** the "T" (text icon, top toolbar)
2. **Click** dashboard area → Add title: "Superstore Sales Analysis Dashboard"
3. **Format**: Increase font size, make bold

### Color Scheme:
1. **Select** dashboard
2. **Dashboard** menu → "Format Colors"
3. Choose professional color scheme

### Titles for Sheets:
1. Right-click each sheet on dashboard
2. Add descriptive titles explaining what each chart shows

---

## 📸 Step 7: Publish to Tableau Public

### Before Publishing:
- [ ] Dashboard title looks good
- [ ] All filters working
- [ ] Charts are labeled clearly
- [ ] No broken data

### Publish Steps:

1. **File** → **"Save As"**
2. **Choose**: "Tableau Public"
3. **Sign in** with your Tableau Public account (create if needed)
4. **Give it a name**: "Superstore Sales Analysis Dashboard"
5. **Add description**:
   ```
   Interactive dashboard analyzing retail sales data across 
   categories, regions, and time periods. Click charts to filter!
   ```
6. **Click**: "Save"
7. **Wait** for upload (1-2 minutes)
8. **You'll get a public URL** like: 
   `https://public.tableau.com/views/SuperstoreSalesAnalysisDashboard/Dashboard1`

---

## 🔗 Step 8: Get Shareable Link

1. After publishing, go to your dashboard on Tableau Public
2. **Click** "Share" (top-right)
3. **Copy the link** to your dashboard
4. **Copy** the embed code if you want to add to website

### Your Dashboard Link:
```
https://public.tableau.com/views/[YourDashboardName]/Dashboard1
```

---

## 📝 Step 9: Update Portfolio README

1. **Open**: `d:\Superstore Sales\project-1-superstore\README.md`
2. **Find** the "Interactive Dashboard" section
3. **Replace** `[Insert Tableau Public Link Here]` with your actual link
4. **Save** the file
5. **Commit to GitHub**:
   ```bash
   git add .
   git commit -m "Add Tableau dashboard link"
   git push
   ```

---

## 🎯 Dashboard Features to Add (Optional)

### Advanced Filters:
- [ ] Date range selector (order date)
- [ ] Customer segment filter
- [ ] Product category multi-select
- [ ] Regional multi-select

### Additional Visualizations:
- [ ] Customer satisfaction heatmap
- [ ] Product performance scatter plot
- [ ] Sales forecast line chart
- [ ] Shipping method efficiency

### Interactive Features:
- [ ] Drill-down from Region → Sub-Region
- [ ] Hover tooltips with detailed info
- [ ] Parameter dropdowns for custom analysis
- [ ] URL actions to external reports

---

## ✅ Checklist: Dashboard Complete

- [ ] All 5-7 sheets created
- [ ] Dashboard assembled with all charts
- [ ] Filters working correctly
- [ ] Title and description added
- [ ] Published to Tableau Public
- [ ] Public link obtained
- [ ] README updated with link
- [ ] GitHub committed and pushed
- [ ] Shared with LinkedIn/friends

---

## 🆘 Troubleshooting

### Problem: Data not loading
**Solution**: Check CSV file path is correct, ensure file is not open in Excel

### Problem: Charts look empty
**Solution**: Drag dimensions to Columns/Rows AND measures to Values

### Problem: Can't publish
**Solution**: Create free Tableau Public account at https://public.tableau.com/

### Problem: Filter not working
**Solution**: Ensure all sheets have the same data source connected

### Problem: Dashboard looks cluttered
**Solution**: Resize and reposition sheet elements using drag handles

---

## 📊 Expected Results

After completing all steps, your dashboard should show:

✅ **Sales by Category**: Technology leading at ~$827K  
✅ **Monthly Trends**: Clear peak in November  
✅ **Top 10 Products**: Phones, Chairs, Storage leading  
✅ **Regional Distribution**: West region dominates  
✅ **Customer Segments**: Consumer segment largest  
✅ **KPIs**: Total $2.26M, Avg $230.77 per transaction  

All charts should be **interactive** - clicking on one filters all others!

---

## 🚀 Pro Tips

1. **Use consistent colors** across dashboard for professional look
2. **Add descriptions** to confusing charts
3. **Test filters** - make sure they work together
4. **Use contrasting colors** for easy visibility
5. **Mobile-optimize** by arranging for phone viewing
6. **Update regularly** as new data comes in
7. **Get feedback** from colleagues before publishing

---

## 📚 Learning Resources

- **Tableau Public Gallery**: https://public.tableau.com/ (inspiration!)
- **Tableau Learning Videos**: https://www.tableau.com/learn/training
- **Tableau Community Forums**: https://community.tableau.com/

---

## ⏱️ Time Breakdown

| Step | Time |
|------|------|
| Download & Install | 10 min |
| Connect data | 5 min |
| Create 5 sheets | 30 min |
| Build dashboard | 20 min |
| Format & polish | 15 min |
| Publish to Public | 10 min |
| **Total** | **~90 min** |

---

## 🎉 After Publishing

**Share Your Dashboard!**

1. **LinkedIn**: "Just published my Superstore Sales dashboard on Tableau Public! 📊 Check it out: [link]"
2. **GitHub**: Update README with link
3. **Email**: Send to friends/mentors
4. **Portfolio**: Feature on your portfolio website

---

## 💡 Next Steps After Dashboard

1. ✅ Create Project 2 dashboard
2. ✅ Add more interactivity
3. ✅ Create multiple views
4. ✅ Build prediction model
5. ✅ Create story (Tableau feature)

---

**Ready to create your dashboard? Let's go! 🚀**

*Estimated completion time: 1.5 - 2 hours*

---

## 📞 Need Help?

- **Dashboard not loading?** → Check CSV file path
- **Filter issues?** → Ensure using "Use as Filter" option
- **Can't publish?** → Create free account at Tableau Public
- **Want more features?** → Explore Tableau's built-in resources

---

**You're about to create your first professional data visualization dashboard! 🎨📊**

Let me know when your dashboard is published and I'll help you optimize it! 💪
