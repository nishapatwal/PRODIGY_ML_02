# Customer Clustering Analysis

## Overview

This project performs customer segmentation analysis using K-Means clustering on retail customer data. The analysis groups customers based on their annual income and spending score to identify distinct customer segments for targeted marketing strategies.

## Features

- **Data Analysis**: Loads and analyzes customer data from CSV files
- **K-Means Clustering**: Groups customers into 3 distinct segments
- **Data Visualization**: Creates scatter plots showing customer clusters and centroids
- **Feature Scaling**: Normalizes data using StandardScaler for optimal clustering results

## Dataset

The project uses a customer dataset (`custom.csv`) containing:
- **CustomerID**: Unique identifier for each customer
- **Annual Income (k$)**: Customer's annual income in thousands of dollars
- **Spending Score (1-100)**: Customer's spending behavior score

## Requirements

### Python Dependencies
```
pandas
matplotlib
scikit-learn
numpy
```

### Installation

1. Clone or download this repository
2. Install required packages:
```bash
pip install pandas matplotlib scikit-learn numpy
```

## Usage

### Running the Analysis

1. Ensure your customer data is in `custom.csv` format
2. Run the clustering script:
```bash
python custom.py
```

### Expected Output

The script will:
1. Display the first few rows of the dataset
2. Perform K-Means clustering with 3 clusters
3. Show the dataset with cluster labels
4. Generate a visualization plot showing:
   - Customer data points colored by cluster
   - Cluster centroids (red X markers)
   - Scaled features for optimal visualization

## Analysis Results

The clustering analysis identifies three customer segments:

1. **High Income, High Spending**: Customers with high annual income and high spending scores
2. **High Income, Low Spending**: Customers with high income but conservative spending
3. **Low Income, Variable Spending**: Customers with lower income and varying spending patterns

## Visualization

The generated plot shows:
- **X-axis**: Scaled Annual Income
- **Y-axis**: Scaled Spending Score
- **Colors**: Different colors represent different customer clusters
- **Red X markers**: Cluster centroids (center points of each segment)

## Customization

### Changing Number of Clusters
Modify the `n_clusters` parameter in the KMeans initialization:
```python
kmeans = KMeans(n_clusters=5, random_state=42)  # Change to 5 clusters
```

### Using Different Features
Update the feature selection to include other variables:
```python
X = df[['Annual Income (k$)', 'Spending Score (1-100)', 'Age']]
```

### Adjusting Visualization
Modify plot parameters in the matplotlib section for different visual styles.

## Business Applications

This analysis can be used for:
- **Targeted Marketing**: Design campaigns for specific customer segments
- **Product Recommendations**: Suggest products based on spending patterns
- **Customer Retention**: Identify high-value customers for retention strategies
- **Inventory Management**: Stock products based on segment preferences

## File Structure

```
customer-cluster/
├── custom.py          # Main clustering script
├── custom.csv         # Customer dataset
└── readme.md         # This file
```

## Contributing

Feel free to contribute improvements:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is open source and available under the MIT License.

## Contact

For questions or suggestions, please open an issue in the repository.
