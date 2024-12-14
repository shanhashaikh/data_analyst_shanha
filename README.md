**Data Quality Control**

**Project Title:** Data Quality Control for Bikeway Analytics

**Project Description:**   
This project focused on enhancing the quality of Vancouver's bikeway dataset to support data-driven decisions in urban infrastructure planning. The initiative ensured accuracy, consistency, and completeness of data, which is essential for reliable analysis of cycling infrastructure and its impact on urban mobility.

**Objective:**    
To improve data integrity and enrich the bikeway dataset by resolving quality issues, standardizing formats, and ensuring the data is ready for analysis and visualization to support sustainable transportation planning.

**Dataset:**        
The dataset file used in this analysis contained 21 columns and over 463 records detailing Vancouver's cycling routes. The filters applied included the Protected Bikeway Lanes constructed in the 21st century. Key attributes include bikeway type, subtype, segment length, and safety features. The focus was on Protected Bike Lanes and their subtypes, exploring their average segment length and speed limits to inform design and safety improvements.        
 
• Object ID: Unique segment identifier; essential for indexing and filtering.     
• Bike Route Name: The route's official name; used for spatial grouping.            
• Street Name: The road hosting the segment; helpful in mapping and understanding local contexts.        
• Bikeway Type: Facility type (e.g., protected lanes); critical for type-based analysis.            
• Subtype: Detailed classification of bikeway type; helps refine analysis of safety and usability.             
• Status: Indicates active or legacy routes; used to focus on current infrastructure.           
• Street Segment Type: Road classification (e.g., arterial); aids in traffic pattern studies.             
• Overall Direction & Bikeway Direction: Directional attributes; vital for planning connectivity.            
• Vehicle Direction: Direction of vehicle flow; analyzed for coexistence efficiency.             
• Speed Limit: Vehicle speed; correlates with safety and accessibility.               
• Surface Type: Paved or unpaved; impacts usability.          
• AAA Network & Segment: Compliance with All Ages and Abilities standards; evaluates inclusivity.                
• W/N & E/S Bound Type: Direction-specific facility types; supports traffic pattern studies.               
• Snow Removal: Inclusion in snow-cleared routes; seasonal analysis relevance.               
• Segment Length: Length in meters; key for network density studies.                
• Year of Construction & Upgrade Year: Timeline attributes; important for trend analysis.               


The bikeway dataset contained information about cycling routes in Vancouver, including attributes like bikeway type, segment length, and safety features. However, challenges such as missing values, inconsistencies, and redundant records limited its utility. This data quality control initiative aimed to resolve these issues, ensuring the dataset was reliable for urban mobility analysis and planning.                


**Methodology:**       

**Data Ingestion:**           
• Upload raw dataset to an AWS S3 bucket for secure and scalable storage.            

Ingestion to the Raw Bucket Ingestion for Exploratory analysis
![Ingestion for Data Quality Control](https://github.com/user-attachments/assets/c2c50490-a9b2-4e5b-a644-d5d410517054)
Note. Primary Source.


**Data Profiling and Cleaning:**            
• AWS Glue DataBrew was used to profile and clean the data.               
• Identified and addressed issues such as missing values and inconsistent formatting.              
• Data cleaning involved dropping irrelevant columns, renaming fields, and correcting formats.                
• Saved cleaned data in Parquet and CSV formats in a designated S3 bucket.              

Data Lineage (Concept of transformation) Data transformation lineage 
![Data transformation lineage](https://github.com/user-attachments/assets/1752c4c3-9542-4a62-96be-b57ed2939bca)
Note. Primary Source.

Data Profiling results in Transform bucket Profiling results 
![Profiling results](https://github.com/user-attachments/assets/ddf185aa-2734-4ae2-a25f-e3b9a52b8610)
Note. Primary Source.

Creation of a Project for Data Cleaning Cleaning job 
![Cleaning job](https://github.com/user-attachments/assets/889cafab-0308-4018-892b-a25b1ceb83ad)
Note. Primary Source.

Recipe for Cleaning job Recipe  
![Recipe](https://github.com/user-attachments/assets/5ff947a8-a2a4-4c5f-8596-faf5d3b1c8b5)
Note. Primary Source.

Data Cleaning Results for System Cleaning result for system 
![Cleaning result for system](https://github.com/user-attachments/assets/e8bcbc38-59cb-4166-a1ec-a1264f275b58)
Note. Primary Source.

Data Cleaning Results for User Cleaning result for User 
![Cleaning result for User](https://github.com/user-attachments/assets/40697a16-3fa7-4a92-9d2e-0ab359a4aed7)
Note. Primary Source.

**Data Enrichment:**          
• Incorporate derived metrics such as average segment length and categorize bikeway types for enhanced analysis.          
• Transform the dataset into a queryable and visualization-ready format for use in advanced analytics.          
• Converted the cleaned dataset into Parquet format for optimized querying and analysis.              
• Created new attributes for safety and usage analysis.         
• Check for the completeness, uniqueness and the freshness of the data and ensure it passes all the quality checks to ensure the integrity of the dataset.


Data Governance Pipeline _ Data quality & control implemented
![image](https://github.com/user-attachments/assets/08eae09c-b821-4d51-80b6-f945d2ecba13)
Note. Primary Source


Data Quality Check Rules
![image](https://github.com/user-attachments/assets/87fd207a-1f57-496d-af03-2640b21bac62) 
Note. Primary Source


Data Governance Pipeline _ Job Run
![image](https://github.com/user-attachments/assets/d138aaad-e664-4a0e-b513-b49f143b4b9f) 
Note. Primary Source


Quality Check “Passed” results_Stored in S3 transform bucket
![image](https://github.com/user-attachments/assets/f03d481c-3905-4c80-b0d7-920f97b5f6ff) 
Note. Primary Source


Quality Check “Failed” results_Stored in S3 transform bucket
![image](https://github.com/user-attachments/assets/5f3876fd-cb7f-499b-a1e4-906153351f5f) 
Note. Primary Source


**Data Analysis:**            
• Utilized SQL queries in AWS Athena to calculate metrics such as average speed limits and segment lengths for bikeway subtypes.           
• Generated insights into trends and infrastructure recommendations.  

Creation of Database in DataCatalog
![image](https://github.com/user-attachments/assets/3e39a6fd-9e25-497e-a5ca-3fc8dbbcf603) 
Note. Primary Source


Creation of Crawler
![image](https://github.com/user-attachments/assets/d9563284-1f62-415b-a5c7-10cbafc741f4)
Note. Primary Source


Tables created from Crawlers
![image](https://github.com/user-attachments/assets/310d1652-2a86-4bc8-a886-d7c44dff860b)
Note. Primary Source


Table overview
![image](https://github.com/user-attachments/assets/5ea90794-4b85-4d00-a3e3-3975069d7d41)
Note. Primary Source


SQL Query through Athena
![image](https://github.com/user-attachments/assets/21cf6514-66cd-4df3-968e-5307a080d04b) 
Note. Primary Source




**Visualization:**           
• Ensured data consistency by cross-referencing key metrics (e.g., segment lengths and construction years).          
• Highlighted discrepancies and provided actionable insights for city planners.             



**Tools and Technologies:**            
• AWS S3 for data storage and organization.              
• AWS Glue and DataBrew for ETL processes and data profiling.                 
• AWS Athena for SQL-based analysis.                         
• City of Vancouver’s Open Data Portal for visualization and insights.               


**Deliverables:**             
Output of the data quality control exercise are:               
• Cleaned Dataset: Ready-to-use bikeway dataset stored in AWS S3 in Parquet and CSV formats.            
• Data Quality Report: Documentation of quality issues identified and solutions implemented.            
• Analysis-Ready Data: Transformed and enriched dataset compatible with AWS Athena for querying and Tableau for visualization.                     


**Timeline:**             
Day 1: Upload dataset to AWS S3 and profile data.               
Day 2: Identify and address missing values and inconsistencies.             
Day 3: Standardize attributes and remove duplicates.             
Day 4: Enrich dataset with derived metrics and classifications.           
Day 5: Validate transformations and store in queryable formats.            
Day 6: Compile documentation and finalize deliverables.         

This project ensured the bikeway dataset met high-quality standards, enabling accurate analysis and actionable insights for urban planners and policymakers. The data enrichment process further enhanced the dataset's analytical value, supporting sustainable cycling infrastructure initiatives in Vancouver.
