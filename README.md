**Project Title:** Student List Data Wrangling : Data Analysis of the Student Dataset for UCW Academic Domain

**Project Description:** 
The project demonstrates the implementation of a data analytics platform using AWS services to perform data wrangling on the student_list dataset. The workflow included uploading data to AWS S3, profiling and cleaning the data using AWS Glue, and querying the processed data with AWS Athena. These steps provided actionable insights, such as the gender distribution among students, highlighting the power of AWS in handling data analytics tasks.

•	Gender Distribution Analysis:   
  By calculating the percentage of male and female students, the university can assess gender representation within the institution. This can help identify disparities in enrollment, aiding initiatives to promote diversity and inclusivity.     
•	Strategic Recruitment Efforts:    
  Insights from demographic data can guide recruitment campaigns targeted at underrepresented groups, helping the university attract a more diverse student body.    
•	Facilities Planning:        
  Insights from demographic distribution can inform decisions about campus facilities, such as allocating resources for male and female dormitories, restrooms, and student support services.           
•	Program Development:       
  Understanding trends in age or gender distribution can help design courses or extracurricular activities tailored to specific student segments.         

**Objective:**       
•	Data wrangling ensures the student dataset is clean, consistent, and ready for analysis, enabling the university to create accurate predictive models for student outcomes.     
•	By focusing on relevant variables and removing duplicates, the university can analyze key factors influencing student success, such as demographics and performance.        
•	Cleaned data enables better decision-making, helping the university identify trends and make data-driven choices for curriculum adjustments, faculty development, and academic support.       
•	The process aids in more effective resource allocation by highlighting areas where students need additional support or where improvements are needed.         
•	Data wrangling supports continuous improvement by allowing the university to monitor changes over time and adjust strategies accordingly.           
•	Clean, structured data enables the development of personalized learning experiences, increasing student engagement and success rates.           
•	The wrangled dataset facilitates benchmarking against industry standards and peer institutions, helping the university plan for long-term growth and success.            

**Dataset:** The Student_List dataset highlights diverse academic backgrounds, work experience levels, and global representation.       
•	Student_ID: Unique identifier for each student        
•	Name: Student's name                
•	Age: Ranges from 22 to 35 years                   
•	Gender: Male or Female                
•	GPA: Ranges from 2.55 to 4.0     
•	Work_Experience_Years: Ranges from 0 to 10 years                  
•	Specialization: Fields of study (HR, Finance, Marketing, IT, Operations)       
•	Country: Diverse, including India, USA, UK, China, Germany, Canada                   
•	Admission_Year: Mainly 2021 to 2023    
•	Graduation_Status: Ongoing or Completed        

**Methodology:**
**Data Ingestion**  
•	Upload raw dataset to an AWS S3 bucket for secure and scalable storage.

 
Ingestion to the Raw Bucket
<img width="1127" alt="Data ingestion" src="https://github.com/user-attachments/assets/885476a5-6704-405d-938e-ef587255b7ed" />
Note.  Primary Source.

**Data Profiling and Cleaning:**          
•	AWS Glue DataBrew was used to profile and clean the data.     
•	Identified and addressed issues such as missing values and inconsistent formatting.         
•	Data cleaning involved dropping irrelevant columns, renaming fields, and correcting formats.      
•	Saved cleaned data in Parquet and CSV formats in a designated S3 bucket.           

Data Profiling Overview
<img width="1127" alt="Data profiling" src="https://github.com/user-attachments/assets/f556ac0e-cc13-4a43-a249-b124a9e6fa9d" />
Note.  Primary Source.

Data Profiling results in Transform bucket Note.  Primary Source.
<img width="1127" alt="profiling results" src="https://github.com/user-attachments/assets/c068a6b5-68c5-4434-9612-a477f286ee39" />
Note.  Primary Source.

Creation of a Project for Data Cleaning
 <img width="1127" alt="Data cleaning" src="https://github.com/user-attachments/assets/38c12123-f62f-4210-b936-ea32c36b2da1" />
Note.  Primary Source.


**Transformation and Storage:**                   
•	Transformed the cleaned dataset into Parquet format for optimized querying.           
•	Stored the processed dataset in a designated S3 bucket.     

Data Cleaning Results for System
 <img width="1126" alt="partitioned cleaning results for system" src="https://github.com/user-attachments/assets/fbec9734-2457-4fe0-b296-72469cec86c6" />
Note.  Primary Source.

Data Cleaning Results for User
<img width="1127" alt="partitioned cleaning results for user" src="https://github.com/user-attachments/assets/b68a41e7-8b67-4898-b0de-351af925ee27" />
Note.  Primary Source.

**Data Analysis:**              
•	Utilized SQL queries in AWS Athena to calculate the percentage of students grouped by gender.   
•	Generated insights into trends and demographic composition and diversity.    

Analysis result obtained by running SQL query on the Data catalog
<img width="1124" alt="SQL Query using Athena" src="https://github.com/user-attachments/assets/42d457a1-5904-4526-95f9-79c657c5c8ec" />
Note.  Primary Source.


**Visualization:**

 <img width="398" alt="data visualization of percentage" src="https://github.com/user-attachments/assets/cd245254-d8bf-46b3-a765-6d81d9a51a42" />



**Tools and Technologies:**            
•  AWS S3 for data storage and organization.           
•  AWS Glue and DataBrew for data profiling and cleaning.          
•  AWS Athena for SQL-based analysis.           

**Deliverables:**                
The final analysis revealed the gender distribution: Male: 55%, Female: 45%.          
Highlighted trends in demographic and academic profiles, aiding strategic decision-making.     

**Timeline for AWS Implementation:**                
•	Day 1: Define project objectives and prepare the dataset.       
•	Day 2: Upload dataset to AWS S3 and organize folder structure.         
•	Day 3: Profile the dataset using AWS Glue DataBrew to identify issues.         
•	Days 4–5: Clean the dataset (handle missing values, standardize formats, remove duplicates).         
•	Day 6: Transform cleaned data into Parquet format and store it in S3.      
•	Days 7–8: Run SQL queries in AWS Athena for data analysis and insights.      
•	Days 9–10: Prepare report and visualizations of insights.         
•	Day 11: Review, document, and finalize the portfolio report.        


**Conclusion:**             
This implementation showcases a scalable and efficient use of AWS services for data wrangling and analysis. It highlights how integrating AWS S3, Glue, and Athena can transform raw datasets into actionable insights, suitable for institutional decision-making and future planning. The process is adaptable for handling larger datasets and more complex analytical requirements.


