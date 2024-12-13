Exploratory Data Analysis

**Project 1 Title:** Bikeway Analytics: An Exploratory Data Analysis of Cycling Infrastructure in Vancouver
**Project Description:**
The project utilized data from Vancouver’s Open Data Portal to perform an exploratory analysis of bikeways across the city. It focused on understanding trends in bikeway usage, infrastructure development, and environmental impact. The primary goal was to provide actionable insights into cycling trends, improve urban mobility, and support sustainable transportation policies.
The analysis examined bikeway lengths, types of cycling routes, connectivity, and relationships between cycling volume and geographic features. The findings aim to guide infrastructure planning and promote increased adoption of cycling as a green transportation mode.
**Objective:**
What insights can be derived from analyzing bikeway data in Vancouver, and how can these insights improve cycling infrastructure and urban mobility?
To analyze Vancouver’s bikeway data to understand trends, optimize infrastructure development, and provide sustainable urban mobility recommendations.

**Dataset:**
The dataset file used in this analysis contained 21 columns and over 463 records detailing Vancouver's cycling routes. The filters applied included the Protected Bikeway Lanes constructed in the 21st century. Key attributes include bikeway type, subtype, segment length, and safety features. The focus was on Protected Bike Lanes and their subtypes, exploring their average segment length and speed limits to inform design and safety improvements.

•	**Object ID:** Unique segment identifier; essential for indexing and filtering.                       
• **Bike Route Name:** The route's official name; used for spatial grouping.                 
•	**Street Name:** The road hosting the segment; helpful in mapping and understanding local contexts.                       
•	**Bikeway Type:** Facility type (e.g., protected lanes); critical for type-based analysis.           
•	**Subtype:** Detailed classification of bikeway type; helps refine analysis of safety and usability.
•	**Status**: Indicates active or legacy routes; used to focus on current infrastructure.
•	**Street Segment Type:** Road classification (e.g., arterial); aids in traffic pattern studies.
•	**Overall Direction & Bikeway Direction:** Directional attributes; vital for planning connectivity.
•	**Vehicle Direction:** Direction of vehicle flow; analyzed for coexistence efficiency.
•	**Speed Limit:** Vehicle speed; correlates with safety and accessibility.
•	**Surface Type:** Paved or unpaved; impacts usability.
•	**AAA Network & Segment:** Compliance with All Ages and Abilities standards; evaluates inclusivity.
•	**W/N & E/S Bound Type:** Direction-specific facility types; supports traffic pattern studies.
•	**Snow Removal:** Inclusion in snow-cleared routes; seasonal analysis relevance.
•	**Segment Length:** Length in meters; key for network density studies.
•	**Year of Construction & Upgrade Year:** Timeline attributes; important for trend analysis.

**Methodology:**
Data Ingestion:
•	Upload raw dataset to an AWS S3 bucket for secure and scalable storage.

Ingestion to the Raw Bucket
![Ingestion for Exploratory analysis](https://github.com/user-attachments/assets/781a0f2f-7732-4aa1-ab20-94c1efeac332)
 Note.  Primary Source.

**Data Profiling and Cleaning:**
•	AWS Glue DataBrew was used to profile and clean the data.
•	Identified and addressed issues such as missing values and inconsistent formatting.
•	Data cleaning involved dropping irrelevant columns, renaming fields, and correcting formats.
•	Saved cleaned data in Parquet and CSV formats in a designated S3 bucket.
Data Lineage (Concept of transformation)
 Note.  Primary Source.

Data Profiling results in Transform bucket Note.  Primary Source.

Creation of a Project for Data Cleaning
 Note.  Primary Source.

Recipe for Cleaning job
 Note.  Primary Source.



Data Cleaning Results for System
 
Note.  Primary Source.

Data Cleaning Results for User
 Note.  Primary Source.
•  ETL Pipeline:
•	Designed an ETL pipeline in AWS Glue to process Protected Bike Lanes data.
•	Calculated average segment lengths and average speed limits, grouped by subtypes.
•	Output stored in system and user folders in S3 for analysis.
ETL Pipeline Design
 Note.  Primary Source.

ETL Pipeline results for System partitioned as per Bikeway Subtypes
 Note.  Primary Source.


ETL Pipeline results for Users using Auto balance transform and just a single output file
 Note.  Primary Source.

**Data Analysis:**
•	Utilized SQL queries in AWS Athena to calculate metrics such as average speed limits and segment lengths for bikeway subtypes.
•	Generated insights into trends and infrastructure recommendations.
Analysis result obtained by running SQL query on the ETL pipeline output for User
 Note.  Primary Source.

**Visualization:**
•	Created visualizations comparing metrics such as average segment length and speed limits.
•	Highlighted discrepancies and provided actionable insights for city planners.

Analysis using two metrics (Averages of Segment Length & Speed Limit) for the dataset
 Note. (Bikeways, 2024)


**Tools and Technologies:**
•  AWS S3 for data storage and organization.
•  AWS Glue and DataBrew for ETL processes and data profiling.
•  AWS Athena for SQL-based analysis.
•  City of Vancouver’s Open Data Portal for visualization and insights.

**Deliverables:**
Insights generated from the exploratory analysis, include:
•	Analysis Report summarizing key trends and insights on Vancouver's bikeway infrastructure.
•	Recommendations for optimizing urban cycling infrastructure and safety.
 

