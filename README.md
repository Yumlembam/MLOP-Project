
# MLOP-Project: Linear Regression Model for Predicting Math Scores

## Overview

This project demonstrates a Linear Regression model used to predict students' math scores based on various features. The project includes exploratory data analysis (EDA), model training, and deployment on both AWS and Azure platforms using Flask.

## Project Structure

```
MLOP-Project/
├── Notebooks/
│   └── EDA/                       # Contains Jupyter notebooks for Exploratory Data Analysis
├── Template/
│   └── index.html                 # HTML file for the web application
├── application.py                 # Flask application to serve the model
├── setup.py                       # Script to set up the environment and install requirements
├── requirements.txt               # List of dependencies required for the project
├── Src/
│   ├── Component/
│   │   ├── data_ingestion.py      # Script for data ingestion
│   │   ├── data_transformation.py # Script for data transformation
│   └── Pipeline/
│       ├── training_pipeline.py   # Script to handle the training pipeline
│       ├── prediction_pipeline.py # Script to handle the prediction pipeline
├── .github/
│   └── workflows/
│       └── azure_webapp.yml       # GitHub Actions workflow for deploying to Azure Web Apps
└── .ebextensions/
    └── option_settings.config     # Configuration for deploying to AWS Elastic Beanstalk
```

## Getting Started

### Prerequisites

- Python 3.x
- Required Python libraries can be installed using:

  ```bash
  pip install -r requirements.txt
  ```

### Running the Project

#### Clone the Repository:

```bash
git clone https://github.com/YourUsername/MLOP-Project.git
cd MLOP-Project
```

#### Set Up the Environment:

```bash
python setup.py install
```

#### Run the Flask Application:

```bash
python application.py
```

The application will be available at [http://localhost:5000/](http://localhost:5000/).

## Project Components

- **Exploratory Data Analysis (EDA):**

  Jupyter notebooks located in the `Notebooks/EDA/` folder provide insights into the dataset used for model training.

- **Web Application:**

  The web interface for the model is served using Flask. The HTML template for the app is located in the `Template/` folder.

- **Source Code:**

  - `Src/Component/`: Contains scripts for data ingestion and transformation.
  - `Src/Pipeline/`: Contains scripts to manage the training and prediction pipelines.

## Deployment

### AWS Elastic Beanstalk

The project includes an `.ebextensions/` folder containing configuration settings for deploying the Flask application on AWS Elastic Beanstalk.

To deploy, ensure you have the AWS CLI set up and run:

```bash
eb init
eb create
```

This will initialize and create an Elastic Beanstalk environment, deploying the application automatically.

### Azure Web Apps

The `.github/workflows/` folder contains a GitHub Actions workflow for deploying the application to Azure Web Apps.

The deployment can be triggered by pushing to the `main` branch. The workflow defined in `azure_webapp.yml` automates the deployment process.

More information on the Azure Web Apps deployment action can be found here: [Azure Web Apps Deploy](https://github.com/Azure/webapps-deploy).

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
