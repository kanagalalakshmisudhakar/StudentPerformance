# Student Performance Prediction Project

This project involves an Exploratory Data Analysis (EDA) of student performance data, building a machine learning model to predict final grades (G3), and deploying the model using Gradio.

## Project Structure

1.  **Data Loading and Cleaning**: The `StudentsPerformance.csv` dataset is loaded and basic information is displayed.
2.  **Exploratory Data Analysis (EDA)**: 
    *   Distribution of numerical features like age, absences, and final grade (G3) are visualized using histograms.
    *   Distribution of categorical features such as sex, parents' cohabitation status (`Pstatus`), and mother's job (`Mjob`) are analyzed using count plots.
    *   Correlation matrix of numerical features is displayed.
    *   Relationships between categorical variables (sex, desire for higher education, internet access) and final grade (G3) are explored using box plots.
    *   Relationships between initial grades (G1, G2), past failures, and the final grade (G3) are visualized using scatter plots and box plots.
3.  **Machine Learning Model**: A Random Forest Regressor model is trained to predict the final grade (G3).
4.  **Gradio Deployment**: An interactive web interface is created using Gradio to demonstrate the trained model.

## Dataset

The project uses the `StudentsPerformance.csv` dataset, which contains various attributes related to student demographics, family information, academic performance (G1, G2, G3), and lifestyle factors.

## EDA Key Findings

*   Initial grades (G1 and G2) show a strong positive correlation with the final grade (G3).
*   The number of past failures tends to be inversely related to the final grade.
*   Students who desire higher education and have internet access at home tend to have higher final grades.

## Machine Learning Model

### Model Used

*   **Random Forest Regressor**

### Performance Metrics

After training, the model achieved the following performance on the test set:

*   **Mean Absolute Error (MAE)**: 0.75
*   **Mean Squared Error (MSE)**: 1.54
*   **R-squared (R2)**: 0.84

These metrics indicate that the model has a strong predictive capability for student final grades.

## Gradio Deployment

The trained model is deployed using Gradio, providing an interactive interface to predict the final grade based on user-inputted student attributes. The interface allows users to select values for each feature and get a real-time prediction.

### How to run the Gradio application:

1.  Ensure you have all necessary libraries installed (`pandas`, `scikit-learn`, `matplotlib`, `seaborn`, `gradio`).
2.  Run the notebook cells sequentially to load data, preprocess, train the model, and define the Gradio interface.
3.  The last code cell in the deployment section will launch the Gradio interface.

**Note on Gradio Share Links**: The `iface.launch(share=True)` command generates a temporary public URL, typically valid for one week. For permanent hosting, consider deploying to Hugging Face Spaces.

### Permanent Hosting on Hugging Face Spaces

To deploy your Gradio application permanently to Hugging Face Spaces, navigate to your project directory in the terminal and run:

```bash
gradio deploy
```

This command facilitates free permanent hosting and allows for GPU upgrades through the Hugging Face Spaces platform.
