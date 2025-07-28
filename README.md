# Git History Workshop

A comprehensive repository designed for learning and practicing Git history commands, featuring **892 commits** spanning over **4+ years** of realistic development history.

## 🎯 Workshop Overview

This repository simulates a real-world web development project that evolved from January 2021 to July 2025, providing extensive material for exploring Git's powerful history and analysis commands.

### 📊 Repository Statistics

- **892 commits** across 4+ years
- **Timeline**: January 1, 2021 → July 31, 2025
- **Commit frequency**: Multiple commits per week (realistic development patterns)
- **File diversity**: 50+ files including HTML, CSS, JavaScript, JSON, and more
- **Realistic patterns**: Business hours commits, weekend gaps, organic growth

## 🚀 Getting Started

### Clone the Repository
```bash
git clone https://github.com/j-marek/git-history-workshop.git
cd git-history-workshop
```

### Verify the History
```bash
# Check total commit count
git rev-list --count HEAD

# See the timeline span
git log --oneline | tail -1  # First commit
git log --oneline | head -1  # Latest commit
```

## 📚 Workshop Exercises

### 1. Basic History Exploration

```bash
# View commit history in different formats
git log --oneline
git log --oneline --graph
git log --pretty=format:"%h %ad %s" --date=short

# Count commits by year
git log --since="2021-01-01" --until="2021-12-31" --oneline | wc -l
git log --since="2022-01-01" --until="2022-12-31" --oneline | wc -l
```

### 2. Time-Based Filtering

```bash
# Explore specific time periods
git log --since="2023-01-01" --until="2023-12-31"
git log --since="6 months ago"
git log --since="2022-06-01" --until="2022-08-31"

# Find commits from specific days of the week
git log --since="2023-01-01" --until="2023-12-31" --pretty=format:"%h %ad %s" --date=format:"%A %Y-%m-%d"
```

### 3. Content-Based Searching

```bash
# Search commit messages
git log --grep="CSS"
git log --grep="Fix"
git log --grep="Update"
git log --grep="Add" --since="2022-01-01"

# Search for code changes
git log -S "function" --oneline
git log -S "background-color" --oneline
git log --all --full-history -- "*.css"
```

### 4. File History Analysis

```bash
# Track file evolution
git log --follow style.css
git log --follow index.html
git log --stat style.css

# See who changed what
git blame style.css
git blame index.html
git blame script.js
```

### 5. Advanced History Analysis

```bash
# Compare different time periods
git diff HEAD~100 HEAD --stat
git diff 2021-01-01 2022-01-01 --stat
git diff 2023-01-01 2024-01-01 --name-only

# Find the busiest development periods
git log --pretty=format:"%ad" --date=format:"%Y-%m" | sort | uniq -c | sort -nr

# Analyze commit patterns
git log --pretty=format:"%ad" --date=format:"%H" | sort | uniq -c
```

### 6. Interactive Exploration

```bash
# Use gitk for visual exploration (if available)
gitk --all

# Interactive log browsing
git log --oneline --graph --all --decorate
```

## 🎓 Learning Objectives

By working with this repository, you'll master:

- **Basic Git Log Commands**: `git log`, `--oneline`, `--graph`, `--stat`
- **Time-Based Filtering**: `--since`, `--until`, date ranges
- **Content Searching**: `--grep`, `-S`, `--all`
- **File History**: `--follow`, `git blame`, file-specific logs
- **Comparative Analysis**: `git diff` across time periods
- **Pattern Recognition**: Understanding real development workflows
- **Advanced Formatting**: Custom `--pretty` formats

## 📁 Repository Structure

```
git-history-workshop/
├── index.html              # Main HTML file (evolved over 4+ years)
├── style.css               # Primary stylesheet (hundreds of updates)
├── script.js               # JavaScript functionality (continuous evolution)
├── README.md               # This file
├── .gitignore              # Git ignore patterns
├── LICENSE                 # MIT License
├── config*.json            # Various configuration files
├── utils*.js               # Utility JavaScript files
├── component*.css          # Component stylesheets
├── page*.html              # Additional HTML pages
└── ...                     # 50+ total files
```

## 🔍 Interesting Discoveries to Make

### Development Patterns
- **Peak development periods**: When were the most commits made?
- **Quiet periods**: When was development slower?
- **File evolution**: How did core files grow over time?
- **Commit message patterns**: What types of work were most common?

### Time Analysis
- **Daily patterns**: What time of day were most commits made?
- **Weekly patterns**: Which days saw the most activity?
- **Seasonal trends**: How did development vary throughout the years?

### Content Evolution
- **CSS evolution**: Track styling improvements over 4+ years
- **JavaScript growth**: See how functionality expanded
- **HTML structure**: Observe semantic improvements
- **File additions**: When were new files introduced?

## 🛠 Advanced Challenges

1. **Create a timeline** of major milestones using `git log --grep`
2. **Identify the longest gap** between commits
3. **Find the most modified file** using `git log --stat`
4. **Analyze commit message patterns** by year
5. **Track the introduction** of specific technologies or patterns
6. **Create visualizations** of development activity over time

## 💡 Tips for Workshop Facilitators

- **Start simple**: Begin with basic `git log` commands
- **Build complexity**: Gradually introduce filtering and formatting
- **Encourage exploration**: Let participants discover patterns
- **Use real examples**: Point out interesting commits or periods
- **Compare approaches**: Show multiple ways to find the same information
- **Practice regularly**: Repetition builds muscle memory

## 🤝 Contributing

This repository is designed for educational purposes. The commit history is intentionally comprehensive and should not be modified to preserve its value as a learning resource.

## 📄 License

MIT License - See [LICENSE](LICENSE) file for details.

---

**Happy Git History Exploring!** 🎉

*This repository contains 892 commits of realistic development history spanning 4+ years, providing endless opportunities to practice and master Git history commands.*
