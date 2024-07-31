README.md:

---

# Data Analysis Project

This repository contains a data analysis project focusing on sales data. The analysis involves calculating customer revenue, monthly revenue, product revenue, and identifying the top customers. The project is containerized with Docker, and includes automated tests to verify the accuracy of the analysis functions.

You can Watch working and Execution of Project Here:
https://youtu.be/lUklLdR5yZY
## Project Structure

```plaintext
.
├── Dockerfile
├── Dockerfile.test
├── README.md
├── data_analysis.py
├── docker-compose.yml
├── orders.csv
├── requirements.txt
└── test_data_analysis.py
```

- **Dockerfile**: Configuration for building the main application Docker image.
- **Dockerfile.test**: Configuration for building the test Docker image.
- **data_analysis.py**: Main script containing data analysis functions.
- **docker-compose.yml**: Docker Compose file for managing services.
- **orders.csv**: Sample dataset used for the analysis.
- **requirements.txt**: Dependencies required for the project.
- **test_data_analysis.py**: Unit tests for the data analysis functions.

## Setup and Usage

### Prerequisites

- Docker
- Docker Compose

### Build and Run the Application
1. **Create Docker Container Getting started**:
    ```sh
    docker run -d -p 80:80 docker/getting-started

    ```

2. **Build the Docker Images**: Here it will save all files to container Images 
    ```sh
    docker build -t app .
    ```

3. **Run the Application**:
    ```sh
    docker run --rm app
    ```

### Run the Tests

1. **Build the Docker Images** (if not already done):
    ```sh
    docker build -f Dockerfile.test -t test-image .
    ```

2. **Run the Tests**:
    ```sh
    docker run --name test-container --rm test-image
    ```

## If Your using Decompose
1. **Clone the Repository**:
    ```sh
    git clone <repository-url>
    cd <repository-directory>
    ```

2. **Build the Docker Images**:
    ```sh
    docker-compose build
    ```

3. **Run the Application**:
    ```sh
    docker-compose up app
    ```

### Run the Tests

1. **Build the Docker Images** (if not already done):
    ```sh
    docker-compose build
    ```

2. **Run the Tests**:
    ```sh
    docker-compose up test
    ```

## Data Analysis Functions

### `compute_customer_revenue(df)`

Calculates the total revenue for each customer.

**Parameters**:
- `df` (DataFrame): The input dataframe containing sales data.

**Returns**:
- DataFrame: A dataframe with customer IDs and their respective total revenue, sorted in descending order.

### `compute_monthly_revenue(df)`

Calculates the total revenue for each month.

**Parameters**:
- `df` (DataFrame): The input dataframe containing sales data.

**Returns**:
- DataFrame: A dataframe with months and their respective total revenue, sorted by month.

### `compute_product_revenue(df)`

Calculates the total revenue for each product.

**Parameters**:
- `df` (DataFrame): The input dataframe containing sales data.

**Returns**:
- DataFrame: A dataframe with product IDs and their respective total revenue, sorted in descending order.

### `get_top_customers(df, top_n=2)`

Identifies the top customers based on total revenue.

**Parameters**:
- `df` (DataFrame): The input dataframe containing sales data.
- `top_n` (int): The number of top customers to return (default is 2).

**Returns**:
- DataFrame: A dataframe with the top N customers and their respective total revenue, sorted in descending order.

## Running Analysis Manually

To run the analysis without Docker:

1. **Install Dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

2. **Run the Script**:
    ```sh
    python data_analysis.py orders.csv
    ```

## Contributing

I welcome contributions! Please fork the repository and create a pull request with your changes.

##Suggesstions:

I welcome all Suggestions if had any please mention in Discussions..


---
