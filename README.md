Topic Modeling is a technique used to extract information from a huge text corpus and classify them into relevant topics. There are no pre-defined examples to input-output mapping and hence I've used unsupervised machine learning techiques to create the model. There occur various methods to topic modeling. But in my code, I have applied the NMF and SVD technique to convert the tfidf and count vectorizer generated input vectors to matrices. I've also compared the SVD approach to NMF to gauge which one is computationally expensive. 

Steps to approaching the topic modeling problem using Count Vectorize and SVD approach:

    1. Preprocessing the text by removing stop words, punctuation and performing lemmatization
    2. Using the count vectorizer technique to convert the processed text corpus to input vectors
    3. Fitting the vectors into linalg SVD method to get a pair of orthonormal input matrices 
    4. Testing the orthonormality of those matrices by using multiplying the matrix's transpose with itself and verify if an identity matrix of the same size is generated 
    5. Check the topics created

Steps to approaching the topic modeling problem using TFIDF Vectorize and NMF approach:

    1. Preprocessing the text by removing stop words, punctuation and performing lemmatization
    2. Using the tfidf vectorizer technique to convert the processed text corpus to input vectors
    3. Fitting the vectors into decomposition NMF method to get a pair of input matrices with non-negative values. The input matrices are not fully decomposed and hence this is not an exact matrix generation approach
    4. Check the topics created
    
**Inference from comparing the SVD and NMF approach:**

SVD is slow and it undertakes exact matrix decomposition. It converts the entire text corpus into matrix irrespective of its size. So deploying SVD on huge datasets could be cumbersome. 
NMF is quick and effective non-exact matrix decomposition technique. 
