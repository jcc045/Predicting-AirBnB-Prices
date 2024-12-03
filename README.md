# Airbnb Price Prediction

## Overview

This project aims to predict the nightly pricing of Airbnb listings in New York City using property and listing attributes. By leveraging data analysis and machine learning techniques, this project helps Airbnb hosts set competitive prices and enables guests to make informed booking decisions.

## Key Features

- **Data Exploration**: Examines patterns and insights from the dataset, including handling missing data and identifying outliers.
- **Modeling Approaches**: Implements multiple regression models (Decision Tree, LassoCV, Gradient Boosting) to predict prices, with a comparison of performance metrics.
- **Recommendations**: Suggests the Gradient Boosting model for deployment due to its superior predictive performance.

## Dataset

The original dataset can be found on [Kaggle](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data/data). It includes information about 48,895 Airbnb listings in NYC with 16 attributes, such as:
- Property location and type (e.g., latitude, longitude, room type)
- Host details (e.g., host ID, number of listings)
- Reviews (e.g., review counts, reviews per month)
- Availability and pricing

### Data Cleaning
- **Handling Missing Data**: Replaced missing values in non-critical fields (e.g., reviews) with zeros.
- **Outlier Treatment**: Analyzed and retained outliers due to their significance and the use of tree-based models.

## Methodology

### Models Used
1. **Decision Tree Regression**: Tuned using Grid Search for optimal parameters.
2. **LassoCV Regression**: Applied cross-validation for feature selection.
3. **Gradient Boosting Regression**: Improved predictions by iteratively correcting residuals.
4. **Dummy Model**: Baseline model using the dataset’s average price.

### Performance Metrics
The models were evaluated using:
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**

### Results
The Gradient Boosting model achieved the best results, with an MAE of $69.45, significantly outperforming the baseline Dummy model.

## Getting Started

### Prerequisites
- Python 3.7+
- Libraries: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/jcc045/airbnb-price-prediction.git
   cd airbnb-price-prediction
   ```
2. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

### Usage
1. Place the dataset (`AB_NYC_2019.csv`) in the `data/` directory.
2. Run the Jupyter notebook or Python scripts to explore data and train models.

## Contributions

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m 'Add feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.

## License

This project is licensed under the MIT License.
