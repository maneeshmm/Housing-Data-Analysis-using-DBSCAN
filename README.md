# Housing Data Analysis using DBSCAN

## 1. Introduction

This report analyzes housing data using DBSCAN clustering. The goal is to group similar houses based on location, room count, population, and other features to identify patterns in housing prices and density.

## 2. Dataset Description

The dataset consists of various attributes related to housing units within a block. Below is a brief description of each feature:

longitude: How far west a house is (higher values indicate farther west).

latitude: How far north a house is (higher values indicate farther north).

housingMedianAge: Median age of houses in a block (lower values indicate newer buildings).

totalRooms: Total number of rooms within a block.

totalBedrooms: Total number of bedrooms within a block.

population: Total number of people residing in a block.

households: Total number of households (groups of people living in home units) in a block.

medianIncome: Median income of households (measured in tens of thousands of USD).

medianHouseValue: Median house value (measured in USD).

oceanProximity: Location of the house concerning the ocean.

## 3. Data Preprocessing

Handling Missing Values:

Checked for missing values in totalBedrooms and other attributes.

Used imputation techniques to fill missing values.

Feature Engineering:

Created new features such as room-to-household ratio and bedroom-to-room ratio.

Data Cleaning:

Removed outliers in house prices and income to improve analysis.

## 4. DBSCAN Clustering Analysis

DBSCAN (Density-Based Spatial Clustering of Applications with Noise) was applied to group houses based on similarities.

Parameter Selection:

Explored different values of epsilon (eps) and min_samples to determine the best clustering structure.

Used silhouette score to evaluate clustering performance.

Cluster Identification:

Houses were clustered based on latitude, longitude, and other numerical attributes.

Noise points (outliers) were identified where DBSCAN could not group them into a cluster.

## 5. Results & Findings

Key Insights:

Houses near coastal regions tend to form distinct clusters.

High-density regions were identified, indicating areas with larger population clusters.

Some houses were classified as noise, possibly indicating outliers in pricing or location.

Silhouette Score Evaluation:

The best clustering parameters were chosen based on silhouette score performance.

A moderate silhouette score indicated reasonably well-defined clusters.

## 6. Conclusion

This analysis used DBSCAN to identify housing clusters based on location and structural attributes. The algorithm effectively grouped houses while detecting anomalies. The results provide insights into the distribution of houses and pricing trends in different areas.
