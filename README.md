# Feature Engineering with Cluster Analysis
## Applied Data Engineering - Week 8

This repository contains materials for our feature engineering lecture focusing on using cluster analysis to improve regression models. We'll use the Carbitrage dataset to explore how clustering can help us incorporate location effects into our car pricing models.

### Repository Structure
```
├── data/                     # Data files and preprocessing scripts
│   ├── location_info.csv     # Location metadata including lat/long
│   └── location_data.csv     # Aggregated Craigslist location statistics
├── exercises/                # In-class exercises
│   ├── market_compare/       # Compare national vs local models
│   └── clustering/           # Implement clustering solution
├── assignments/              # Weekly assignment
│   ├── instructions.md       # Assignment details
│   └── getting_started.ipynb # Starter code
└── solutions/                # [Hidden] Solution code
```

### Knowledge Needed from Past Classes
- Regression modeling of car prices (Advanced Applied Modeling)
- Cluster analysis (ADE Week 6)
- Regression modeling at scale (ADE Week 7) 
- Familiarity with the Carbitrage data pipeline (ADE Weeks 1-4)

### Learning Objectives
After completing this module, learners will be able to:
- Assess areas of improvement for regression models
- Select relevant variables for clustering
- Implement cluster analysis for feature engineering
- Assess the impact of cluster-based features on model performance

### In-Class Exercises
1. **Market Comparison**
   - Compare national model performance across different markets
   - Identify patterns in model errors
   - Test location-specific models

2. **Clustering Implementation**
   - Select and prepare variables for clustering
   - Implement Gower distance for mixed data types
   - Evaluate different numbers of clusters
   - Integrate cluster assignments into regression models

### Weekly Assignment
Learners will:
- Apply clustering to a different subset of car models
- Compare performance across different clustering approaches
- Write a technical summary of their findings
- [Solution code available to instructors]

### Additional Resources
- Documentation for the Carbitrage data pipeline
- [K-Means in `scikit-learn` documentation](https://scikit-learn.org/1.5/modules/generated/sklearn.cluster.KMeans.html)
