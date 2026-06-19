# 🔍 Quick Reference: Common Commands

Quick reference guide for Git, Python, and portfolio management commands.

---

## 🐙 Git Commands

### Setup
```bash
# Initialize git in folder
git init

# Configure your name and email (one-time)
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Clone existing repository
git clone https://github.com/USERNAME/REPO.git
```

### Daily Workflow
```bash
# Check status
git status

# Add files for commit
git add .                    # Add all files
git add filename.txt         # Add specific file

# Commit with message
git commit -m "Your message here"

# Push to GitHub
git push                     # Push to main branch
git push -u origin BRANCH    # Push to specific branch

# Pull latest changes
git pull

# View commit history
git log
git log --oneline            # Shorter version
```

### Branching (Advanced)
```bash
# Create new branch
git branch new-branch

# Switch to branch
git checkout new-branch
git checkout -b new-branch   # Create and switch

# Merge branch
git checkout main
git merge feature-branch

# Delete branch
git branch -d feature-branch
```

---

## 🐍 Python Commands

### Virtual Environment
```bash
# Create virtual environment
python -m venv venv

# Activate (Windows)
venv\Scripts\activate

# Activate (macOS/Linux)
source venv/bin/activate

# Deactivate
deactivate

# Check if active
# You should see (venv) at start of terminal line
```

### Package Management
```bash
# Install packages
pip install pandas numpy matplotlib

# Install from requirements.txt
pip install -r requirements.txt

# List installed packages
pip list

# Freeze current environment
pip freeze > requirements.txt

# Upgrade package
pip install --upgrade pandas
```

### Jupyter Notebook
```bash
# Install Jupyter
pip install jupyter

# Start Jupyter
jupyter notebook

# List running notebooks
jupyter notebook list

# Stop Jupyter (in terminal)
# Press Ctrl + C twice
```

---

## 📊 Pandas Quick Commands

```python
# Read data
df = pd.read_csv('file.csv')
df = pd.read_excel('file.xlsx')

# Basic info
df.head()                    # First 5 rows
df.tail()                    # Last 5 rows
df.info()                    # Data types & missing values
df.describe()                # Summary statistics
df.shape                     # Rows and columns count

# Filtering
df[df['column'] > 100]       # Filter rows
df[['col1', 'col2']]         # Select columns

# Grouping
df.groupby('category')['sales'].sum()
df.groupby('category').agg({'sales': 'sum', 'qty': 'mean'})

# Handling missing values
df.isnull().sum()            # Count missing values
df.fillna(0)                 # Fill with value
df.dropna()                  # Remove missing values

# Duplicates
df.duplicated().sum()        # Count duplicates
df.drop_duplicates()         # Remove duplicates

# Save data
df.to_csv('output.csv', index=False)
df.to_excel('output.xlsx', index=False)
```

---

## 📈 Matplotlib & Seaborn Quick Commands

```python
import matplotlib.pyplot as plt
import seaborn as sns

# Basic plot
plt.plot(x, y)
plt.bar(x, y)
plt.hist(data)
plt.scatter(x, y)

# Formatting
plt.title('Title')
plt.xlabel('X Axis')
plt.ylabel('Y Axis')
plt.legend()
plt.grid(True)

# Display
plt.show()
plt.savefig('filename.png', dpi=300, bbox_inches='tight')

# Subplots
fig, axes = plt.subplots(2, 2, figsize=(12, 10))
axes[0, 0].plot(data)

# Seaborn
sns.heatmap(df.corr(), annot=True)
sns.boxplot(data=df, x='category', y='value')
sns.barplot(data=df, x='category', y='value')
```

---

## 🎨 Portfolio Setup Commands

### Initial Setup
```bash
# Step 1: Navigate to project folder
cd "d:\Superstore Sales"

# Step 2: Initialize git
git init

# Step 3: Add all files
git add .

# Step 4: First commit
git commit -m "Initial commit: Superstore Sales Analysis"

# Step 5: Connect to GitHub (replace USERNAME)
git remote add origin https://github.com/YOUR-USERNAME/data-analyst-portfolio.git

# Step 6: Push to GitHub
git push -u origin main
```

### After Making Changes
```bash
# 1. Check what changed
git status

# 2. Add changes
git add .

# 3. Commit with descriptive message
git commit -m "Add Tableau dashboard link"

# 4. Push to GitHub
git push
```

---

## 📁 File & Folder Commands

```bash
# Navigate
cd foldername                # Go into folder
cd ..                        # Go back one level
cd ~                         # Go to home
pwd                          # Print current directory
ls or dir                    # List contents

# Create/Delete
mkdir folder-name            # Create folder
touch filename.txt           # Create file
rm filename.txt              # Delete file
rm -r folder-name            # Delete folder

# Copy/Move
cp source.txt dest.txt       # Copy file
mv source.txt dest.txt       # Move/rename file

# View file
cat filename.txt             # View file contents
```

---

## 📝 Markdown Cheatsheet (For README files)

```markdown
# Heading 1
## Heading 2
### Heading 3

**Bold text**
*Italic text*
***Bold italic***

- Bullet point
  - Nested point
    - Deeper point

1. Numbered list
2. Second item

[Link text](https://url.com)
![Image alt text](image.png)

| Column 1 | Column 2 |
|----------|----------|
| Data 1   | Data 2   |

`inline code`

```code block```

> Blockquote
>> Nested quote

---

✓ Checkmarks
⚡ Emoji
🎯 Symbols
```

---

## 🔗 Useful Links

- [GitHub Docs](https://docs.github.com)
- [Git Cheatsheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
- [Pandas Docs](https://pandas.pydata.org/docs/)
- [Matplotlib Docs](https://matplotlib.org/)
- [Tableau Public](https://public.tableau.com/)

---

## ⚠️ Common Mistakes to Avoid

❌ **Don't**: `git push` without committing first  
✅ **Do**: `git add .` → `git commit -m "message"` → `git push`

❌ **Don't**: Push raw CSV files (too large)  
✅ **Do**: Add `*.csv` to `.gitignore`

❌ **Don't**: Use generic commit messages  
✅ **Do**: Use descriptive: "Add Tableau dashboard link" not "update"

❌ **Don't**: Forget to activate virtual environment  
✅ **Do**: See `(venv)` at terminal start

❌ **Don't**: Mix spaces and tabs in Python  
✅ **Do**: Use consistent indentation

---

## 💡 Pro Tips

1. **Commit often**: Small commits are easier to track
2. **Meaningful messages**: "Add correlation heatmap" not "fix"
3. **Test before pushing**: Run notebooks before git push
4. **Use branches**: Keep main branch clean for production
5. **Document everything**: Future you will thank present you

---

## 🎯 Portfolio Workflow

```
1. Work on analysis in Jupyter
   ↓
2. Test and verify all cells run
   ↓
3. Save notebook
   ↓
4. Update README with findings
   ↓
5. git add . (stage changes)
   ↓
6. git commit -m "message" (commit)
   ↓
7. git push (upload to GitHub)
   ↓
8. Verify on GitHub website
```

---

## 🆘 When Things Go Wrong

### Problem: Wrong commit message
```bash
git commit --amend -m "New message"
```

### Problem: Need to undo last commit
```bash
git revert HEAD
```

### Problem: Lost changes
```bash
git reflog                   # See history
git checkout <hash>          # Go back to specific commit
```

### Problem: Need to see what changed
```bash
git diff                     # Show changes
git show <hash>              # Show specific commit
```

---

## ✅ Checklist Before Pushing

- [ ] All notebooks run without errors
- [ ] README updated with latest findings
- [ ] Images/visualizations included
- [ ] No sensitive data in files
- [ ] Files are under size limits
- [ ] Commit message is descriptive
- [ ] No test files included
- [ ] .gitignore properly configured

---

**Bookmark this page for quick reference! 📌**

*Last Updated: 2026-06-19*
