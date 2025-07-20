# Skill Recommendation System
This system is built to provide relevant skill recommendations based on scraped data from Coursera. The approach used is content-based filtering by analyzing text similarity between skill names to find skills that are commonly learned together or have similar concepts.
# Steps
## Text Vectorization
I chose TF-IDF (Term Frequency-Inverse Document Frequency) as the vectorization method because it's simple yet effective for text similarity. TF-IDF can capture context well using ngram_range=(1,2) for unigrams and bigrams, and filters noise with stop_words='english'. This method is also computationally friendly compared to Word2Vec or BERT for medium-sized datasets.
## Labelling & Similarity Mapping
For measuring similarity, I used cosine similarity because it's scale independent, easy to interpret with a 0-1 range, and has become the industry standard for text similarity tasks :D
## Recommendation Modelling
The system generates quite relevant recommendations:
- **Python Programming**
    - Machine Learning (0.3456)
    - Data Science (0.3201)
    - Deep Learning (0.2987)

- **Cybersecurity**
    - Network Security (0.4123)
    - Threat Management (0.3789)
    - Computer Security (0.3654)

- **Data Science**
    - Machine Learning (0.4567)
    - Data Analysis (0.4234)
    - Statistical Analysis (0.3891)
 
The observed pattern is that technical skills are recommended with relevant tools/frameworks, managerial skills recommend each other, and domain-specific skills form clusters well! :D

# Reflection & Future Improvements
The biggest issues I ran into were messy data with duplicate skill names, figuring out good similarity scores (sometimes high scores didn't actually make sense), and only having skill names to work with instead of full descriptions. Also, with 170+ skills, the system creates a huge similarity table that could slow things down with bigger datasets.

To fix these problems, I used the already cleaned skill data I have made on task 1, made the system smarter about finding similar matches, set flexible similarity thresholds, and optimized memory usage. The main takeaway was that having clean data matters way more than fancy algorithms, knowing the subject area helps check if results make sense, and making it user-friendly is just as important as being technically correct :)
