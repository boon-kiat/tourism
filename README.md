## Big Data Pipeline for Analyzing Tourism Dataset

### Module:
WQD7007 Big Data Management 

### Problem Statement:
- Select an online big data resource for tourism industry.
- Choose the most suitable method to store the big data resource.
- Demonstrate the process to store and access the big data resource, then extract meaningful outcomes for the tourism industry.
- Draw a big data pipeline for analyzing the big data resource.

### Dataset:
- TripAdvisor Hotel Reviews dataset on [Kaggle](https://www.kaggle.com/datasets/joebeachcapital/hotel-reviews/data)
- Contain 878,561 reviews from 4333 hotels crawled from TripAdvisor.
- Consist of 2 files, including ‘offerings’ and ‘reviews’.
- The ‘offerings’ has 9 attributes whereas the ‘reviews’ has 10 attributes.
- The use of JSON would make it easier to read the data. 

### Methodology:
_Choosing the most suitable method to store big data:_  
- Considering the characteristics of TripAdvisor data, which includes structured and unstructured content, MongoDB stands out as a suitable choice.
- MongoDB is a NoSQL, document-oriented database. Its document-based model allows the storage of data in BSON (Binary JSON) format, a binary representation of JSON-like documents. This is well-suited for the diverse nature of the TripAdvisor data, which includes both structured (e.g., ratings, dates) and unstructured content (e.g., text reviews).
    
_Data Storage:_  
- In the MongoDB shell, create a database named WQD7007 to store data.  
- Use ‘mongoimport’ to import the JSON files into their respective collections.
- Use the $lookup stage of the aggregation pipeline to perform a left outer join between the ‘review’ collection and the ‘offering’ collection based on the ‘offering_id’ field.
- Data is stored in MongoDB, utilizing its document-based structure.
    
_Data Access:_  
- Perform 6 queries to provide insights for tourism industry, such as identifying top-rated hotels, understanding customer preferences across hotel classes, understanding user engagement through helpful reviews, etc.
- The extracted outcomes offer a holistic view of hotel performance, customer behaviour, and content creation within the tourism industry.
- Collectively, the big data pipeline offers a comprehensive approach to extracting insights, making it a valuable asset for businesses and stakeholders in the tourism sector.
