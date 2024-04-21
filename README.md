# Web-Log-Anomaly-Detection
This project focuses on detecting anomalies in web log data from a NASA dataset from August 1995. The goal is to identify unusual patterns in the data that may indicate errors or malicious activities.

## Table of Contents

- [Project Description](#project-description)
- [Data](#data)
- [Prerequisites](#prerequisites)
- [Methods and Techniques](#methods-and-techniques)
- [Results and Visualization](#results-and-visualization)
- [Future Work](#future-work)

## Project Description

The project includes data cleaning, exploration, and applying anomaly detection techniques using an isolation forest model. Anomalies are identified based on different features like response size, request length, and HTTP status codes.

## Data

- The dataset used in this project is a NASA web log dataset from August 1995.
- The data file should be in the project directory as `nasa_aug95.csv`.

## Prerequisites

- Python 3.x
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`
- You can install the required libraries using:

    ``` shell
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```

## Methods and Techniques

- **Data Cleaning:** Handles missing values in the `response_size` column.
- **Feature Engineering:** Extracts features such as request type, request length, and other time-based features.
- **Anomaly Detection:** Uses an Isolation Forest model to detect anomalies based on features such as `response_size`, `request_length`, `http_status`, `hour`, and `day_of_week`.
- **Evaluation:** Compares predicted anomalies with manually labeled true anomalies to calculate the F1 score.

## Results and Visualization

- The script generates various plots to visualize data distributions and anomalies:
    - Time series plot of response size.
      ![image](https://github.com/IshwaryaKeerthivasan/Web-Log-Anomaly-Detection/assets/92322280/e007ef9a-8242-4c75-860d-0e78c25e5bb2)

    - Distribution of response size.
      ![image](https://github.com/IshwaryaKeerthivasan/Web-Log-Anomaly-Detection/assets/92322280/6693d938-1f35-4feb-800c-e02b2b4868db)

    - Response size by status.
      ![image](https://github.com/IshwaryaKeerthivasan/Web-Log-Anomaly-Detection/assets/92322280/06c79064-2b26-4134-940f-403235d15003)

    - Correlation heatmap.
      ![image](https://github.com/IshwaryaKeerthivasan/Web-Log-Anomaly-Detection/assets/92322280/2d52020b-46b7-458e-ac77-7e5fc18fb709)

    - Scatter plot of anomalies in response size vs request length.
      ![image](https://github.com/IshwaryaKeerthivasan/Web-Log-Anomaly-Detection/assets/92322280/aacf4f1c-4f44-4be7-9573-d23211740830)

    - Anomalies distribution by hour of the day and day of the week.
      ![image](https://github.com/IshwaryaKeerthivasan/Web-Log-Anomaly-Detection/assets/92322280/d31dddc0-011a-4030-9a45-6e6313c73490)
      ![image](https://github.com/IshwaryaKeerthivasan/Web-Log-Anomaly-Detection/assets/92322280/2c995ae5-e39e-4d39-835a-9d9b66a2e924)


## Future Work
- Improve model performance by fine-tuning hyperparameters.
- Explore additional anomaly detection techniques.
- Investigate potential reasons for anomalies and suggest preventive measures.
