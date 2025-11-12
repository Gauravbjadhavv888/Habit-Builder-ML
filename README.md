now # Habit Builder ML

## Description

Habit Builder ML is a machine learning project designed to analyze habit tracking data and provide insights, classifications, and recommendations for improving personal habits. The project uses a Jupyter notebook to process CSV or Excel files containing habit data, engineer features, train a Random Forest classifier, and generate visualizations and actionable suggestions.

The model classifies habits into categories such as "Maintain", "Focus", "Reduce", or "Okay" based on metrics like completion rate, average streak, consistency, and trend. It is particularly useful for individuals or apps tracking daily habits to identify strengths and areas for improvement.

This notebook is optimized for Google Colab, where users can upload their data files directly.

## Features

- **Data Loading**: Supports CSV and Excel file uploads with automatic encoding detection for CSV files.
- **Feature Engineering**:
  - Completion Rate: Average completion percentage.
  - Average Streak: Mean length of consecutive completion days.
  - Consistency: Standard deviation of completion (lower is more consistent).
  - Trend: Change in completion rate over time (last 7 days vs. first 7 days).
- **Auto-Labeling**: Automatically categorizes habits without needing a predefined habit type column.
- **Machine Learning Model**: Uses Random Forest Classifier to predict habit categories.
- **Visualizations**:
  - Completion Rate Distribution Histogram.
  - Habit Categories Count Plot.
  - Completion Rate per Habit Bar Plot.
  - Daily Completion Heatmap.
  - Trend Line for Completion Over Time.
  - Boxplot of Completion Rates.
  - User-wise Habit Performance.
  - Feature Correlation Heatmap.
  - Stacked Bar Graph for Daily Completion.
  - Separate Line Trends for Each Habit.
  - Average Streak Bar Plot.
  - Pie Chart for Daily Completion Distribution.
- **Recommendations**: Provides personalized suggestions for each habit based on its label and score.

## Requirements

- Python 3.x
- Libraries:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - seaborn
- Google Colab (recommended for file uploads) or a local Jupyter environment.

## Installation

1. Clone or download the repository.
2. Install required libraries:
   ```
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
3. Open the `Habit_BuilderML.ipynb` notebook in Jupyter or Google Colab.

## Usage

1. **Prepare Your Data**: Ensure your CSV or Excel file has the following columns:
   - `user_id`: Identifier for the user.
   - `habit_name`: Name of the habit (e.g., "Exercise", "Reading").
   - `date`: Date of the habit entry (YYYY-MM-DD format).
   - `completed`: Binary value (0 for not completed, 1 for completed).

2. **Run the Notebook**:
   - Upload your file when prompted.
   - The notebook will process the data, engineer features, train the model, and display results.
   - View visualizations and recommendations at the end.

3. **Interpret Results**:
   - **Maintain**: Strong habits with high completion and positive trend.
   - **Focus**: Weak or declining habits needing attention.
   - **Reduce**: Inconsistent habits, possibly negative ones to minimize.
   - **Okay**: Average habits that are stable.

## ML Model Explanation

- **Algorithm**: Random Forest Classifier from scikit-learn.
- **Features**: completion_rate, avg_streak, consistency, trend.
- **Training**: Splits data into 75% train and 25% test sets.
- **Evaluation**: Uses classification report (precision, recall, F1-score) to assess performance.
- **Purpose**: Predicts habit labels to guide user actions.

The model is trained on aggregated habit data per user and habit, making it scalable for multiple users.

## Visualizations

The notebook generates multiple plots to visualize habit data:
- Histograms and bar plots for distributions.
- Heatmaps for daily patterns.
- Line plots for trends over time.
- Pie charts for completion breakdowns.
- Correlation matrices for feature relationships.

These help in understanding habit performance visually.

## Recommendations

Based on the model's predictions, the notebook outputs suggestions like:
- "Exercise → Maintain (Score: 0.85)"
- "Smoking → Reduce (Score: 0.30)"

Use these to adjust your habits accordingly.

## Contributing

Contributions are welcome! Please fork the repository, make changes, and submit a pull request. Ensure code follows best practices and includes documentation.

## License

This project is licensed under the MIT License. See LICENSE file for details.
