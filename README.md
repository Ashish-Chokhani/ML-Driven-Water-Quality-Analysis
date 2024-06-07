# Water Quality Assessment Using Big Data and Machine Learning

## Description

This project integrates big data analytics and machine learning techniques to assess water quality. The process involves data collection, preprocessing, exploratory data analysis, heat map generation, and model training and validation to predict water quality patterns and identify anomalies.

## Table of Contents

- [Data Collection and Preprocessing](#data-collection-and-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Heat Maps Generation](#heat-maps-generation)
- [Model Training and Validation](#model-training-and-validation)
- [Conclusion](#conclusion)
- [Usage](#usage)
- [License](#license)

## Data Collection and Preprocessing

### Data Extraction
- Used pandas in Python to read CSV data.
- Imported data from Gemstat for Indus and Godavari regions in India.
- Employed `pd.read_csv()` function with specified delimiters.

### Data Concatenation
- Merged data from multiple sources.
- Combined Indus and Godavari datasets into one DataFrame.
- Saved merged DataFrame to a new CSV for further analysis.

### Data Preprocessing
- Removed irrelevant columns.
- Identified unique parameters.
- Created a parameter dictionary and converted it into a DataFrame.
- Combined original and parameter DataFrames for a comprehensive dataset.

### Missing Data Handling
- Imputed missing numerical values with mean.
- Replaced missing categorical data with mode (most frequent values).

### Feature Engineering
- Created new features like dew point temperature from existing data.
- Conducted PCA for dimensionality reduction.
- Utilized K-Means for clustering to uncover data patterns.

## Exploratory Data Analysis

### Histogram Analysis
- Utilized histograms with KDE to visualize the distribution of key variables.
- Highlighted central tendency measures such as mean and median for each variable using vertical dashed lines.

### Correlation Analysis
- Employed a heatmap to visualize pairwise correlations between different variables.
- Annotated correlation coefficients on the heatmap to identify strong positive or negative relationships.

### Principal Component Analysis (PCA)
- Examined the explained variance ratio to determine the number of principal components required.
- Visualized clusters in the PCA space to identify inherent patterns or groupings within the data.

### Box Plot Analysis
- Conducted box plot analysis for key variables such as Turbidity, Water Temperature, pH, and Rainfall.
- Identified outliers and assessed the spread and central tendency of each variable.

### Time-Series Analysis
- Plotted individual variables as a function of time to observe temporal trends.
- Analyzed fluctuations over time and identified seasonal patterns or anomalies.

### Comparative Analysis
- Compared the distribution of variables across different categories or datasets to identify variations and trends.
- Utilized box plots to compare the distribution of Turbidity, Water Temperature, and Rainfall.

## Heat Maps Generation

### Heat Maps for Generation
- Generated heat maps for Canada and Australia.
- Coverage: 20 sites for Australia and 58 sites for Canada.
- Analyzed parameters: pH, Rainfall, Water Temperature, and Turbidity.
- Visualization techniques: Box plots, heat maps, plotting parameters over time.

### Heat Maps for Canada
- pH
- Temperature
- Similar heat maps generated for Australia as well for 20 different stations.

## Model Training and Validation

### Logistic Regression Model
- Utilized a multinomial logistic regression model to predict water quality classes.
- Split the data into training and testing sets, and evaluated model performance using accuracy metrics.

### LSTM Model
- Organized the dataset for LSTM training, sorting it by date and scaling target values.
- Trained LSTM models for each target variable (Turbidity, Water Temperature, Rainfall) using sequential data.
- Split the dataset into training and testing sets, and assessed model performance using Mean Absolute Error (MAE).

## Conclusion

- Identified strong predictive capabilities of logistic regression model for water quality classification.
- LSTM models demonstrated effectiveness in forecasting environmental variables with low prediction errors.
- Reliable water quality prediction models can inform decision-making for resource management and public health initiatives.

## Usage

1. Open the Jupyter notebook:
    ```bash
    jupyter notebook 1.ipynb
    ```

2. Run the cells sequentially to perform data preprocessing, exploratory data analysis, heat map generation, and model training and validation.

## License

This project is licensed under the IIITH License
