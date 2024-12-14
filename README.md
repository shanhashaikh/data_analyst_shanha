**Project Title:** Descriptive Analysis of Final Grades: Insights by Course and Letter Grade

**Project Description:**
This project analyzes the final grades dataset to evaluate academic performance across various courses. The focus is on understanding the distribution of letter grades (A, B, C, D) within each course to uncover trends, identify patterns, and suggest areas for improvement.

**Objective:**   
•	Determine grade distribution per course and evaluate performance trends.    
•	Group and visualize data by letter grades to highlight variations across courses.      
•	Provide actionable recommendations for academic enhancement.          

**Dataset:**    
The final grade dataset provided contains a comprehensive breakdown of student performance in various courses, across different faculties. The key attributes in the dataset include:     
•	**Student_ID:** Unique identifier for each student, essential for linking records to specific individuals.                    
•	**Name:** The student's name, used for identification purposes.        
•	**Course:** The course in which the student is enrolled, important for course-specific analysis.              
•	**Faculty_ID:** The ID of the faculty offering the course, helpful for analyzing faculty performance or trends.            
•	**Assignment_Grade:** The grade achieved in assignments, a key component of the overall grade calculation.          
•	**Midterm_Grade**: The grade achieved in the midterm exam, part of the evaluation for the course.         
•	**Final_Exam_Grade:** The grade achieved in the final exam, another key component of the final grade.               
•	**Participation_Grade:** The grade based on class participation, reflecting the student's engagement.                
•	**Total_Grade:** The final calculated grade, taking into account all assessment components (assignments, midterms, finals, and participation).                 
•	**Grade_Letter:** The letter grade assigned based on the total grade, typically corresponding to letter grading scales (e.g., A, B, C, D).               
This dataset allows for detailed analysis of student performance across various assessment categories, enabling comparisons across students, courses, and faculties. Key metrics like average performance in assignments, exams, and participation can be derived to assess overall academic outcomes, trends, or areas needing improvement.


**Methodology:**          
**Data Ingestion:**
o	Uploaded the dataset to an AWS S3 bucket.
o	Structured storage in folders for courses.

Ingestion to the Raw Bucket
<img width="1127" alt="Ingestion" src="https://github.com/user-attachments/assets/41d1efc4-4710-48a9-9c0d-c8e067919d47" />
Note.  Primary Source.
 


**Data Profiling and Cleaning:**
•	AWS Glue DataBrew was used to profile and clean the data.
•	Removed duplicates and standardized formats for grades.
•	Verified consistency in letter grade calculations.

Data Lineage (Concept of transformation)
<img width="1127" alt="Profiling lineage" src="https://github.com/user-attachments/assets/ffe424aa-874f-41b5-8eb9-7488797de015" />
Note.  Primary Source.


Data Profile Overview 
<img width="1127" alt="Profile Overview" src="https://github.com/user-attachments/assets/cf5a4fbc-e921-48b1-82fe-4ba60f67e997" />
Note.  Primary Source.


Data Profiling results in Transform bucket
<img width="1127" alt="Data Profiling results" src="https://github.com/user-attachments/assets/3aee6321-d686-4cd1-8698-51e18d350895" />
Note.  Primary Source.


Creation of a Project for Data Cleaning
 <img width="1127" alt="Cleaning Job" src="https://github.com/user-attachments/assets/31757bf2-c104-4919-8fba-d47ad7c4e069" />
Note.  Primary Source.


Data Cleaning Results for System
<img width="1127" alt="Partitioned cleaning result for system" src="https://github.com/user-attachments/assets/8315d88d-9231-4100-883a-1e5be5c6d540" />
Note.  Primary Source.


Data Cleaning Results for User
<img width="1127" alt="Partitioned cleaning result for user" src="https://github.com/user-attachments/assets/82881e36-e252-4c38-9bd1-f3b9c92f7e69" />
Note.  Primary Source.

 
**ETL Pipeline:**
•	Designed an ETL pipeline in AWS Glue to process Final Grades data.           
•	Output stored in system and user folders in S3 for analysis.           

ETL Pipeline Design
<img width="1127" alt="ETL Pipeline" src="https://github.com/user-attachments/assets/89f26d75-ad30-48ce-b9d2-d94ae9511c7a" />
Note.  Primary Source.

**Visualization:**
Created bar charts and grouped visualizations to illustrate:          
•	Grade distribution per course.        
•	Proportion of A, B, C, D grades in each course.           


**Data Visualization:**
![Data visualization](https://github.com/user-attachments/assets/1305850c-1705-4f13-8806-2eccf538da45)
Note. Primary Source


**Tools and Technologies:**              
•  AWS S3 for data storage and organization.        
•  AWS Glue and DataBrew for ETL processes and data profiling.               

**Deliverables:**             
•	Grade Distribution Report: Summary of grade patterns across courses.                
•	Visualization: Charts displaying grade distribution per course.                 
•	Recommendations: Insights into course-level academic trends and areas needing focus.             


**Timeline:**    
•	Day 1: Upload dataset to AWS S3.            
•	Day 2: Profile data and identify cleaning requirements.            
•	Days 3–4: Clean dataset and ensure consistency in grades.                
•	Day 5: Analyze grade distribution using Athena SQL queries.             
•	Day 6: Create visualizations for grade distributions.
•	Day 7: Compile the report and finalize portfolio submission.

**Key Insights:**    
•	Courses with the highest proportion of "A" grades demonstrate strong academic performance.        
•	Disparities in grade distribution suggest areas for potential course review or support interventions.         
•	Visualization highlights trends like the prevalence of "C" or "D" grades in specific courses.         

**Conclusion:**
This project successfully provided an in-depth analysis of student performance by course and grade letter, helping identify trends and suggest improvements. By leveraging AWS and visualization tools, the dataset's potential for academic insights was fully realized.

