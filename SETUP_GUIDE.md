# 🚀 Portfolio Setup Guide

Follow these steps to set up your Data Analyst Portfolio locally and prepare it for GitHub.

---

## ✅ Pre-requisites

- **Git** installed ([Download](https://git-scm.com/))
- **Python 3.8+** installed ([Download](https://www.python.org/))
- **GitHub account** ([Create](https://github.com/signup))
- **VS Code or any code editor**

---

## 📋 Step 1: Verify Your Folder Structure

Ensure your local folder looks like this:

```
d:\Superstore Sales\
├── 📄 README.md                              # Main portfolio README
├── 📄 SETUP_GUIDE.md                         # This file
├── 📁 project-1-superstore/
│   ├── 📄 README.md                          # Project README
│   ├── 📄 requirements.txt                   # Dependencies
│   ├── 📄 .gitignore                         # Git ignore rules
│   ├── 📁 notebooks/
│   │   └── 📓 superstore_analysis.ipynb
│   ├── 📁 data/
│   │   ├── 📊 train.csv
│   │   └── 📊 superstore_sales_cleaned.csv
│   └── 📁 images/
│       ├── 📷 superstore_eda_visualizations.png
│       └── 📷 correlation_heatmap.png
```

---

## 🔧 Step 2: Initialize Git Repository

Open your terminal/Git Bash and navigate to the project folder:

```bash
cd "d:\Superstore Sales"
```

Initialize git:

```bash
git init
git add .
git commit -m "Initial commit: Superstore Sales Analysis portfolio"
```

---

## 🐙 Step 3: Create GitHub Repository

1. Go to [GitHub.com](https://github.com)
2. Click **"New repository"** button (top left)
3. Fill in:
   - **Repository name**: `data-analyst-portfolio`
   - **Description**: "A portfolio of data analysis projects showcasing Python, SQL, and BI tools"
   - **Visibility**: Select **Public** (for portfolio visibility)
   - **Initialize**: Do NOT check "Add a README.md" (we already have one)
4. Click **"Create repository"**

---

## 📤 Step 4: Push to GitHub

Copy the repository URL from GitHub, then run:

```bash
git remote add origin https://github.com/YOUR-USERNAME/data-analyst-portfolio.git
git branch -M main
git push -u origin main
```

**Replace** `YOUR-USERNAME` with your actual GitHub username.

---

## ✏️ Step 5: Update README Files

Edit these files and add your actual information:

### Main README.md
```markdown
# 👋 About Me
- Your name
- Your background
- Your interests

### 🔗 Connect With Me
- LinkedIn: [Your LinkedIn URL]
- GitHub: [Your GitHub URL]
- Email: your.email@example.com
```

### project-1-superstore/README.md
```markdown
- Update the "Tableau Public Version" and "Power BI Version" links once you create dashboards
- Add any additional findings specific to your analysis
```

---

## 🔄 Step 6: Update After Creating Dashboards

Once you create your Tableau or Power BI dashboard:

1. Get the public dashboard link
2. Update the README files with the link:

```markdown
### Tableau Public Version
**Link**: [Your Dashboard Title](https://public.tableau.com/YOUR-DASHBOARD-URL)
```

3. Commit and push changes:

```bash
git add .
git commit -m "Add Tableau dashboard link"
git push
```

---

## 📊 Step 7: Creating a Tableau Dashboard (Quick Guide)

### Option A: Tableau Public (Free)

1. **Download** Tableau Public from [tableau.com/public](https://public.tableau.com/)
2. **Open** and create a new workbook
3. **Connect** to your CSV file: `superstore_sales_cleaned.csv`
4. **Create sheets**:
   - Sheet 1: Sales by Category (bar chart)
   - Sheet 2: Sales by Month (line chart)
   - Sheet 3: Top Products (horizontal bar chart)
   - Sheet 4: Sales by Region (map or pie chart)
   - Sheet 5: KPI Cards (total sales, avg transaction)
5. **Combine** sheets into a dashboard
6. **Add filters** for interactivity
7. **Publish** to Tableau Public
8. **Share** the public link

### Option B: Power BI Desktop (Free)

1. **Download** Power BI Desktop
2. **Get Data** → Select your CSV file
3. **Create visualizations**:
   - Clustered bar chart (sales by category)
   - Line chart (sales by month)
   - Map visual (sales by region)
   - Card visuals (KPIs)
   - Slicers (filters)
4. **Arrange** on dashboard page
5. **Publish** to Power BI Service (requires Power BI account)

---

## 🌐 Step 8: Create GitHub Pages Portfolio (Optional)

### Easy Option: Use GitHub's Built-in Pages

1. Go to your repository settings
2. Scroll to **"GitHub Pages"** section
3. Select source: **Main branch**
4. Your portfolio will be live at: `https://YOUR-USERNAME.github.io/data-analyst-portfolio/`

---

## 📝 Step 9: Update Your Resume

Add this to your **Projects** section:

```markdown
## Projects

**Superstore Sales Analysis**
- Cleaned and analyzed 9,800 retail transactions using Python (Pandas, Matplotlib, Seaborn)
- Identified Technology as top revenue category ($827K) using exploratory data analysis
- Built interactive Tableau dashboard with regional breakdowns and KPIs
- Generated 5 strategic recommendations to increase profitability
- [GitHub Repo](https://github.com/YOUR-USERNAME/data-analyst-portfolio) | [Dashboard](#)

**Skills Used**: Python, Pandas, Data Visualization, Tableau, Excel, Business Analysis
```

---

## 🔄 Step 10: Recurring Updates

### Weekly/Monthly
```bash
# After completing analysis work
git add .
git commit -m "Add new analysis: [Description]"
git push
```

### Before Interviews
- ✅ Update contact information
- ✅ Verify all links work
- ✅ Add latest projects
- ✅ Update skills list
- ✅ Review README for typos

---

## 🎯 Portfolio Checklist

- [ ] Folder structure created
- [ ] All files populated with content
- [ ] Git repository initialized locally
- [ ] GitHub repository created
- [ ] Code pushed to GitHub
- [ ] GitHub Pages enabled (optional)
- [ ] Personal info updated in README
- [ ] Dashboard links added
- [ ] Resume updated
- [ ] Portfolio shared with connections

---

## 🚀 Next Steps

After completing this setup:

1. **Build Tableau/Power BI Dashboard** (1-2 hours)
2. **Share Portfolio** with LinkedIn & GitHub network
3. **Start Project 2** (using different dataset)
4. **Apply to Jobs** and link to your portfolio
5. **Keep Updating** with new projects quarterly

---

## 💡 Tips for Success

✅ **Keep it Simple**: Don't overcomplicate early projects  
✅ **Show Your Work**: Include notebooks, not just dashboards  
✅ **Tell a Story**: Explain your findings clearly  
✅ **Regular Updates**: Add projects consistently  
✅ **Network**: Share your projects with peers  
✅ **Learn Continuously**: Add new tools/skills to each project  

---

## 🆘 Common Issues & Solutions

### Issue: Files too large for GitHub
**Solution**: Use `.gitignore` to exclude CSV and image files, or use Git LFS

```bash
git rm --cached *.csv
echo "*.csv" >> .gitignore
git add .gitignore
git commit -m "Remove CSV files from tracking"
```

### Issue: Need to update remote URL
```bash
git remote set-url origin https://github.com/NEW-USERNAME/NEW-REPO.git
```

### Issue: Forgot to add .gitignore before first push
```bash
git rm --cached .
git add .
git commit -m "Apply gitignore"
```

---

## 📚 Helpful Resources

- [GitHub Guides](https://guides.github.com/)
- [Git Basics](https://git-scm.com/book/en/v2/Getting-Started-The-Basics)
- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [Tableau Public Tips](https://public.tableau.com/)
- [Power BI Learning](https://learn.microsoft.com/power-bi/)

---

## ❓ FAQ

**Q: Should I make my portfolio public?**  
A: Yes! Recruiters search GitHub for portfolios. Make it public.

**Q: How many projects do I need?**  
A: Start with 2-3 quality projects. Quality > Quantity.

**Q: Should I include raw data?**  
A: Keep cleaned data, exclude raw data to save space.

**Q: Can I showcase work from others?**  
A: Yes, but give credit and explain what YOU did.

---

## 🎉 Congratulations!

Your Data Analyst Portfolio is now set up! 

**Next Action**: Create your first Tableau dashboard and update the README with the link.

---

**Questions?** Check the main README or reach out to the data analysis community!

**Happy Analyzing! 📊**
