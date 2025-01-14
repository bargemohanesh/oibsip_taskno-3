# oibsip_taskno-3
# Car Price Prediction Project

## Project Overview
This project is focused on predicting the selling price of second-hand cars using a machine learning pipeline. The dataset contains various features such as car name, year of manufacture, fuel type, transmission, and mileage.

## Dataset
The dataset contains the following columns:
- **Car_Name**: Name of the car.
- **Year**: Manufacturing year of the car.
- **Selling_Price**: Price at which the car is being sold (target variable).
- **Present_Price**: Current showroom price of the car.
- **Driven_kms**: Kilometers driven by the car.
- **Fuel_Type**: Type of fuel used (Petrol/Diesel/CNG).
- **Selling_type**: Indicates if the seller is an individual or a dealer.
- **Transmission**: Transmission type (Manual/Automatic).
- **Owner**: Number of previous owners.

## Steps Followed

### Data Preprocessing
1. **Loading Data**: The dataset is loaded using Pandas.
2. **Backup Creation**: A backup of the original dataset is created for safety.
3. **Unique Value Checks**: Inspected unique values in categorical columns.
4. **Column Transformation**: Modified `Car_Name` to extract brand names for simplicity.
5. **Handling Missing Values**: Checked and confirmed no missing values in the dataset.
6. **Descriptive Statistics**: Examined summary statistics of the dataset.

### Data Visualization
1. Explored relationships between:
   - Car names and selling price.
   - Year of manufacture and selling price.
   - Mileage and selling price.
   - Fuel type and selling price.
2. Used Seaborn for visualizations:
   - **Swarmplots**: Showed distribution of selling prices across different categories.
   - **Boxplots**: Analyzed price variations with respect to fuel type.
   - **Scatterplots**: Investigated the impact of driven kilometers on selling price.

### Feature Engineering
- Selected important features:
  - `Car_Name`, `Present_Price`, `Year`, `Driven_kms`, `Fuel_Type`, `Transmission`, and `Owner`.
- Dropped the `Selling_type` column as it had minimal impact on price prediction.

### Model Training
1. **Train-Test Split**: Split the dataset into training and testing sets (80:20 ratio).
2. **Encoding Categorical Features**: Used `OneHotEncoder` for categorical variables like `Car_Name`, `Fuel_Type`, and `Transmission`.
3. **Pipeline Creation**:
   - Applied `ColumnTransformer` for encoding and numeric feature transformation.
   - Built a pipeline with preprocessing steps and the regression model.
4. **Model**: Linear Regression.
5. **Training**: Fitted the pipeline on training data.

### Model Evaluation
- Evaluated the performance of the model using the R² score on test data.

## Libraries Used
- `pandas`: Data manipulation.
- `numpy`: Numerical operations.
- `matplotlib`: Data visualization.
- `seaborn`: Advanced data visualization.
- `sklearn`: Machine learning pipeline and model evaluation.

## Results
- The model demonstrates a reasonable prediction accuracy for selling prices of cars. Further tuning and testing could improve its performance.

## Future Work
1. Experiment with other regression algorithms such as Random Forest and Gradient Boosting.
2. Incorporate additional features like car condition or location for better predictions.
3. Deploy the model using Flask or Streamlit for user interaction.

## How to Run the Code
1. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
2. Load the dataset and execute the provided script in a Python environment.
3. Visualize and interpret the results based on the output.
