# AI-BASED RECOMMENDATION SYSTEM

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : GIRISH KUMAR

*INTERN_ID* : CT06DF2915

*DOMAIN* : Java Programming

*DURATION* : 6 WEEKS

*MENTOR* : Neela Santhosh Kumar
  
  
<br/><br/><br/>

## Description

### System Architecture  

* Dual-approach collaborative filtering using Apache Mahout framework  
* User-based and item-based algorithms for comprehensive recommendation coverage  
* FileDataModel integration for CSV data processing and matrix operations  
* Modular design with clear separation between data layer, algorithm layer, and presentation layer 
* Enterprise-ready architecture supporting scalability and maintainability  
 
### Core Implementation Components  
 
Data Infrastructure  

* CSV-based data model with user-item-rating triplets (UserID, MovieID, Rating)  
* In-memory movie metadata storage for title mapping and display  
* Synthetic dataset generation with 50 ratings across 13 movies and 10 users  
* Rating scale normalization using 1-5 star system for consistency  
* Data validation and error handling for missing or invalid entries  

User-Based Collaborative Filtering  

* Pearson correlation similarity for user preference matching  
* Threshold-based neighborhood (0.1 threshold) for statistical significance  
* Rating scale compensation to handle different user rating behaviors  
* Sparse data handling through robust similarity calculations  
* Neighborhood filtering to eliminate weak correlations and noise  

Item-Based Collaborative Filtering  

* Log-likelihood similarity for item-to-item relationship analysis  
* Sparsity optimization better performance with incomplete rating matrices  
* Stable recommendation patterns due to consistent item characteristics  
* Popular item bias mitigation through advanced similarity measures  
* Matrix factorization support for scalable computations


### Output Images

![](https://github.com/girishkr9331/AI-Based-Recommendation-System/blob/main/AiBasedRecommendationSystem1.png) <br/><br/>
![](https://github.com/girishkr9331/AI-Based-Recommendation-System/blob/main/AiBasedRecommendationSystem2.png)
  
<br/><br/><br/>
Welcome to AI Recommendation system  

(Preferred terminal git bash & os windows)
Insturctions to follow(must) & Internet connection required

 1. Create required directories using following commands 
    ```mkdir recommendation-system```  
    ```cd recommendation-system```  
    ```mkdir lib```  

 2. Install Apache mahout in your system by following command

    ```curl -O https://archive.apache.org/dist/mahout/0.13.0/apache-mahout-distribution-0.13.0.tar.gz```  
    ```tar -xzf apache-mahout-distribution-0.13.0.tar.gz```  
    ```cp apache-mahout-distribution-0.13.0/lib/*.jar lib/```  
    ```cp apache-mahout-distribution-0.13.0/*.jar lib/```  

 3. Download hadoop client libs
    ```curl -O https://archive.apache.org/dist/hadoop/common/hadoop-2.8.5/hadoop-2.8.5.tar.gz```  
    ```tar -xzf hadoop-2.8.5.tar.gz```  
    ```cp hadoop-2.8.5/share/hadoop/common/*.jar lib/```  
    ```cp hadoop-2.8.5/share/hadoop/common/lib/*.jar lib/```  
 
 4. Set classpath

    ```export CLASSPATH=".:lib/*"```  

 5. Compile the java files using following commands

    ```javac -cp ".;lib\mahout-mr-0.13.0.jar;lib\mahout-math-0.13.0.jar;lib\hadoop-common-2.8.5.jar;lib\commons-math3-3.6.1.jar;lib\slf4j-api-1.7.25.jar;lib\guava-20.0.jar" *.java```  
    ```javac -cp $CLASSPATH *.java```  
 
 6. Run the application 

    ```java -cp ".;lib\*" RecommendationDemo```  
