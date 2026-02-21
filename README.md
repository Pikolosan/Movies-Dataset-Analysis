<<<<<<< HEAD
# 🎬 Advanced Movie Dataset Analysis - TMDB 9000+ Movies

**Moving beyond beginner-level EDA to advanced analytics, machine learning, and business intelligence.**
=======
# **9000 movies from TMDB API**
| Contents 											 	   	|
| -------- 											 	   	|
| [Dataset Description](#Dataset-Description)			   	|
| [Columns Descreption](#Columns-Descreption) 		   		|
| [EDA Questions](#eda-questions)							|
| [Data Wrangling](#Data-Wrangling)					   		|
| [Data Cleaning](#Data-Cleaning)						   	|
| [Data Visualization](#Data-Visualization)					|
| [Conclusion](#Conclusion)									|
| [Built with](#Built-with)							   		|
>>>>>>> eaff8ec3e58e7367ad26595292a0517eb0137f00

| Quick Links |
| --- |
| [Overview](#overview) |
| [Research Questions](#research-questions) |
| [Dataset Description](#dataset-description) |
| [Key Findings](#key-findings) |
| [Technologies](#technologies) |
| [Project Structure](#project-structure) |

---

## Overview

This project analyzes 9,000+ movies from TMDB API using **advanced analytical techniques** that go far beyond basic exploratory data analysis. Rather than answering beginner questions like "What's the most common genre?", we focus on **business-level insights** that would inform studio strategy.

### Key Innovation

Instead of answering shallow questions, this analysis:
- ✅ Implements weighted rating formulas (IMDb methodology)
- ✅ Normalizes popularity metrics across time periods
- ✅ Builds predictive ML models for popularity drivers
- ✅ Reveals hidden correlations and market paradoxes
- ✅ Provides strategic recommendations for studios/platforms

---

## Research Questions

### NOT Beginner-Level Questions Like...
❌ What's the most frequent genre?  
❌ Which movie has highest popularity?  
❌ How many movies per year?  

### Instead, We Ask...
✅ **Which genres generate highest WEIGHTED rating** after normalizing for vote count?  
✅ **What factors most influence popularity?** (Correlation: 0.81 for Vote_Count, 0.34 for Quality)  
✅ **How did genre dominance shift over decades?** (Sci-Fi +18%, Comedy declining)  
✅ **Can we predict popularity** using ML? (R² = 0.51 - revealing hidden factors)  
✅ **What's the genre market paradox?** (Drama oversupplied, Action undervalued)  

---

## Dataset Description

**Source**: TMDB API  
**Size**: 9,000+ unique movies, 25,500+ rows after genre expansion  
**Time Span**: 1960-2020  
**Format**: CSV (mymoviedb.csv)

### Key Columns:
1. **Release_Date**: Year of release
2. **Title**: Movie name
3. **Vote_Average**: User rating (0-10)
4. **Vote_Count**: Number of votes received
5. **Popularity**: TMDB engagement metric
6. **Genre**: Movie categories (multi-valued)

---

## Key Findings

### 🎯 Business-Level Insights (Not Beginner Observations)

#### 1. **Genre Market Paradox**
- Drama dominates production (14%) but does NOT dominate popularity
- Action/Adventure show **2.3x higher average engagement**
- **Implication**: Market misalignment; studios oversupply drama while audiences prefer action

#### 2. **Quality vs. Visibility: Weak Correlation (0.34)**
- High-rated movies ≠ Popular movies
- Vote_Count (visibility) shows **0.81 correlation** with popularity
- **Key insight**: Marketing > Quality for popularity metrics

#### 3. **Post-2015 Fundamental Shift**
- Popularity increased significantly after streaming boom (2015)
- 2020 showed highest variance (pandemic effect)
- Modern metrics not comparable to pre-2015 era

#### 4. **Machine Learning Reveals Limits (R² = 0.51)**
- Only 50% of popularity explained by available features
- Other factors: cultural moments, celebrity power, timing, marketing
- Genre impact on popularity is minimal

#### 5. **Genre Evolution: Clear Trends**
- **Sci-Fi**: +18% growth post-2010 (fastest-growing)
- **Action**: Stable 15-20% (consistent favorite)
- **Comedy**: Declining since 2000s
- **Horror**: Resurgent in 2010s-2020s

#### 6. **Production Volume ≠ Quality**
- 2020 had most movies; average rating remained ~6.2/10
- Higher volume doesn't guarantee higher quality
- Suggests strategic shift in industry metrics

---

## Technologies Used

- **Data Processing**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Machine Learning**: Scikit-Learn (Linear Regression)
- **Environment**: Python 3.8+, Jupyter Notebook
- **Methods**: 
  - Weighted Rating Formulas (IMDb methodology)
  - Z-score Normalization
  - Correlation Analysis & Heatmaps
  - Linear Regression with Feature Importance
  - Time Series Analysis
  - Categorical Encoding

---

## Project Structure

```
9000-movies-dataset-analysis.ipynb    # Main analysis notebook
mymoviedb.csv                         # Raw data (9000+ movies)
README.md                             # This file
```

### Notebook Sections

1. **Data Loading & Wrangling** - Load CSV, handle genres, extract year
2. **Advanced Metrics** - Weighted rating (IMDb formula)
3. **Normalization Analysis** - Z-score popularity by year
4. **Correlation Analysis** - Heatmap of what drives popularity
5. **Genre Evolution** - Market share trends across decades
6. **Machine Learning** - Linear regression to predict popularity
7. **Genre Analysis** - Rating vs. Popularity vs. Production volume
8. **Executive Insights** - Strategic recommendations

---

## Strategic Recommendations

For Studios/Streaming Platforms:

💡 **Rethink Drama Strategy** - Oversaturated; ROI analysis needed  
💡 **Invest in Marketing** - Vote_Count predicts popularity better than quality  
💡 **Monitor Post-2015 Trends** - Streaming changed engagement fundamentally  
💡 **Use Weighted Ratings** - Don't rely on raw popularity for greenlighting  
💡 **Diversify Genres** - Sci-Fi growing; Horror underutilized; Comedy declining

---

## How to Use

1. **Clone/Download** this repository
2. **Ensure dependencies** installed: `pip install pandas numpy matplotlib seaborn scikit-learn`
3. **Open notebook**: `9000-movies-dataset-analysis.ipynb` in Jupyter
4. **Run cells sequentially** from top to bottom
5. **Review insights** in the "KEY BUSINESS INSIGHTS" section

### Expected Runtime
- Data loading & cleaning: ~5-10 seconds
- Weighted rating calculation: ~2 seconds
- ML model training: ~3-5 seconds
- Visualizations: ~10-15 seconds
- **Total**: ~30-40 seconds

---

## Advanced Techniques Demonstrated

✅ **Weighted Rating Formula**  
Implements IMDb's methodology: WR = (v/(v+m))R + (m/(v+m))C

✅ **Z-Score Normalization**  
Normalizes popularity by year to remove temporal bias

✅ **Correlation Analysis**  
Heatmap showing what truly influences movie popularity

✅ **Machine Learning**  
Linear regression with feature importance analysis

✅ **Time Series Analysis**  
Genre market share trends across decades

✅ **Statistical Insights**  
Executive-level conclusions from data patterns

---

## Future Enhancements

🔮 Add logistic regression for popularity classification (High/Medium/Low)  
🔮 Sentiment analysis on movie overviews  
🔮 Network analysis of actor collaborations  
🔮 Time series forecasting for future trends  
🔮 Interactive Tableau/Power BI dashboard  
🔮 Deep learning models for recommendation  

---

## About This Project

This project started as basic EDA and evolved into a demonstration of **professional data science practices** including:
- Advanced feature engineering (weighted metrics)
- Machine learning modeling
- Business intelligence insights
- Strategic recommendations backed by data

**Not recommended for beginners** - assumes understanding of:
- Pandas/NumPy
- Statistical concepts (correlation, normalization)
- Machine learning basics
- Data visualization best practices

Perfect for portfolios demonstrating **intermediate+ data science skills**.

---

## Data Source

Dataset: [TMDB 9000+ Movies Dataset](https://www.kaggle.com/datasets/disham993/9000-movies-dataset)  
License: CC0 (Public Domain)  
Last Updated: 2020
