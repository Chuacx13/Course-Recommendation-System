# Course-Recommendation-System

Attached in this repository are solely the source codes and results for the course recommendation system project.

To run the project, make a shortcut of this [drive](https://drive.google.com/drive/u/0/folders/1a_pL2hVAQ5S_1n2Erin0-WcN9boa204e) and run the code on Google Collab.

[README Link](https://docs.google.com/document/d/1AOam-Jret7EDbg-m-JkoYGtkRkke7WFLBUhP20Ho-Sc/edit)

## Objective

Developed a hybrid model that leverages different machine learning models to provide tailored course recommendations. Incoporated job data into recommendation system to attempt to provide users with recommendations that are aligned with their job interests.

## Datasets

- **Coursera_courses.csv**  
  _Main dataset for courses_  
  [Kaggle Link](https://www.kaggle.com/datasets/imuhammad/course-reviews-on-coursera?select=Coursera_courses.csv)

- **Coursera_reviews.csv**  
  _Main dataset for reviewers (users)_  
  [Kaggle Link](https://www.kaggle.com/datasets/imuhammad/course-reviews-on-coursera?select=Coursera_reviews.csv)

- **CourseraDataset-Unclean.csv**  
  _Dataset with additional courses’ metadata_  
  [Kaggle Link](https://www.kaggle.com/datasets/elvinrustam/coursera-dataset?select=CourseraDataset-Unclean.csv)

- **coursera_course_dataset_v3.csv**  
  _Dataset with additional course descriptions_  
  [Kaggle Link](https://www.kaggle.com/datasets/azraimohamad/coursera-course-data?select=coursera_course_dataset_v3.csv)

- **coursera_courses (2).csv**  
  _Dataset with additional course descriptions_  
  [Kaggle Link](https://www.kaggle.com/datasets/tianyimasf/coursera-course-dataset)

- **job_skills.csv**  
  _Main dataset for jobs_  
  [Kaggle Link](https://www.kaggle.com/datasets/asaniczka/1-3m-linkedin-jobs-and-skills-2024?select=job_skills.csv)

- **linkedin_job_postings.csv**  
  _Dataset with additional jobs’ metadata_  
  [Kaggle Link](https://www.kaggle.com/datasets/asaniczka/1-3m-linkedin-jobs-and-skills-2024?select=linkedin_job_postings.csv)

## File Overview

1. **1_Data_Preprocessing_EDA.ipynb**  
   _Merges data preprocessing_

2. **2_User_Based.ipynb**  
   _Conducts user-based collaborative filtering based on user-course interactions, including the sentiment of their reviews and the ratings given to the courses._

3. **3_Content_Based.ipynb**  
   _The recommendation model uses content-based filtering on user-course interactions. It profiles users and courses using TF-IDF on text data and normalized numeric features, computing similarities across multiple dimensions and adjusting recommendations based on weighted attributes._

4. **4_lightGCN.ipynb**  
   _Recommendation model with LightGCN (Graph Convolutional Network architecture) to learn representation of users and courses through a user-course interaction graph._

5. **5_NCF.ipynb**  
   _Recommendation model using Neural Collaborative Filtering (NCF) to capture complex relationships between user-course interactions._

6. **6_Item_Based.ipynb**  
   _Recommendation model using Jaccard similarity to capture similarity between courses, considering the strength of user-course interactions._

7. **7_Recommendation_With_Jobs.ipynb**  
   _Recommendation model that links users' existing skills from taken courses and job cluster assignments to generate course recommendations that fill the users’ skill gaps._

8. **8_Implicit_lightFM.ipynb**  
   _Recommendation model using implicit feedback from users to train a LightFM model for determining recommendations._

9. **9_Hybrid_Recommendation.ipynb**  
   _Final recommendation model that assigns weights and combines the scoring matrices from individual models (2-8), ultimately choosing the top 10 recommendations for users based on the highest score._
