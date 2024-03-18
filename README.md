# Real-Time ETL Pipeline

This repository contains an example of a real-time ETL (Extract, Transform, Load) pipeline implemented using Apache Airflow. The pipeline scrapes data from a website, transforms it, and loads it into a CSV file.

## Overview

The ETL pipeline consists of the following steps:

1. **Scrape Data**: The `scrape_data()` function retrieves data from a website using requests and BeautifulSoup libraries. It extracts relevant information and returns it as a list of dictionaries.

2. **Transform Data**: The `transform_data()` function performs any necessary transformations on the scraped data. For this example, no transformations are applied, and the data is returned as is.

3. **Load Data**: The `load_data()` function loads the transformed data into a CSV file named `data.csv`. It uses the csv module to write the data in CSV format.

The pipeline is orchestrated using Apache Airflow, a workflow management platform. The `realtime_etl_pipeline.py` file defines the DAG (Directed Acyclic Graph) that specifies the tasks and their dependencies.

## Setup

1. Clone the repository:

    ```
    git clone https://github.com/ndungek/Real-Time-ETL-Pipeline.git
    ```

2. Install dependencies:

    ```
    pip install -r requirements.txt
    ```

3. Initialize Airflow database:

    ```
    airflow db init
    ```

4. Start the Airflow webserver and scheduler:

    ```
    airflow webserver --port 8080
    airflow scheduler
    ```

5. Access the Airflow UI in your web browser at `http://localhost:8080` and trigger the `realtime_etl_pipeline` DAG.

## Customization

Feel free to customize the pipeline according to your specific requirements. You can modify the scraping logic, apply transformations, or load the data into different destinations.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
