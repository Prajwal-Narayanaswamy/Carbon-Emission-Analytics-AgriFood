## Introduction
The agricultural sector is responsible for approximately 62% of the total global CO2 emissions, making it a major contributor to climate change. This project aims to develop a dashboard that visualizes and monitors the impact of agricultural activities on CO2 emissions. To build the Power BI dashboard, we will utilize various data engineering tools and principles throughout the process.

## Project Architecture
The source data will be stored in Azure Blob Storage. Whenever a new source file is added, an Azure Data Factory pipeline will automatically ingest it into our raw container within Azure Data Lake Storage Gen 2, triggered by an event. After the data is in the raw container, we will use Data Flows to perform basic transformations, as the data source does not require complex modifications. The transformed data will then be stored in our gold layer, also in ADLS Gen 2. Finally, the cleaned data will be made available for visualization in Power BI. Below is the architecture diagram of the proposed solution!
![Diagram](misc/ArchitectureDiagram.png)


## Appendix

Data used in this project has been obtained from [Kaggle](https://www.kaggle.com/datasets/alessandrolobello/agri-food-co2-emission-dataset-forecasting-ml)

