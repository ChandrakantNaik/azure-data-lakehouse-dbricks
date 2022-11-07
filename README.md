# azure-data-lakehouse-dbricks
## Data lake solution for Divvy bikeshare using Databricks

### The goal of this project is to develop a data lake solution using Azure Databricks using a lake house architecture. You will:
- Design a star schema based on the business outcomes listed below.
- Import the data into Azure Databricks using Delta Lake to create a Bronze data store.
- Create a gold data store in Delta Lake tables.
- Transform the data into the star schema for a Gold data store.

### The business outcomes you are designing for are as follows:
- Analyze how much time is spent per ride
  - Based on date and time factors such as day of week and time of day
  - Based on which station is the starting and / or ending station
  - Based on age of the rider at time of the ride
  - Based on whether the rider is a member or a casual rider
- Analyze how much money is spent
  - Per month, quarter, year
  - Per member, based on the age of the rider at account start
- EXTRA CREDIT - Analyze how much money is spent per member
  - Based on how many rides the rider averages per month
  - Based on how many minutes the rider spends on a bike per month

## Divy Bikeshare Dimensional Model (Star Schema)
![Divy Bikeshare Dimensional Model](dimensional-model/divy-data-model-star-schema-model.drawio1024_1.jpg)

## Project Setup
- **For this project i'm using databricks community edition**
  ### Infrastructure Setup
  - Create a databricks cluster. To create a cluster using the user interface, either 
    - Click the Create Cluster button in the Compute section
    - Click New > Cluster in your workspace's side navigation. Refer to screenshot below
  ![Create Databricks Cluster](images/create-cluster.GIF)
  - To Import data (.csv files) into databricks you need to enable DBFS File Browser.
    - Go to the admin console.
    - Click the Workspace Settings tab.
    - In the Advanced section, click the DBFS File Browser toggle.
    - Click Confirm.
    - Refresh the workspace. Refer to screenshot below
  ![DBFS enabled](images/dbfs-enabled.GIF)

  ### Data Lakehouse Setup
  - Import the data (.csv files) into Azure Databricks using Delta Lake to create a Bronze data store
    - Select **Upload data** to access the **data upload UI** and load CSV files into Delta Lake tables. Refer to screenshot below
  ![DBFS data upload](images/dbfs-data-upload.GIF)
