                                                                                                               Telugu Story Recommendation Engine

This project presents the development of a multi-phase story recommendation engine designed to deliver relevant and engaging Telugu stories based on user behavior, popularity, time trends, and real-world context. The system begins with a popularity-based recommender that suggests widely appreciated stories suitable for new or anonymous users. It then advances to a collaborative filtering model, offering personalized recommendations by analyzing patterns in user ratings. A time-based recommendation phase highlights stories that have remained consistently popular over the years or during specific periods, capturing shifting reader interests. Finally, a context-aware recommendation system integrates real-world festivals and holidays by using semantic text similarity and external API data to recommend culturally relevant stories. This layered approach ensures both personalized and occasion-specific story suggestions, enhancing the reader’s experience and making the platform more interactive, intelligent, and culturally meaningful.

Phase 1: Popularity-Based Recommender
Goal: Suggest widely appreciated stories to all users, especially first-time visitors.
Method: Ranks stories based on number of ratings and average rating to produce a list of the most engaging and liked stories.

Phase 2: Collaborative Filtering
Goal: Provide personalized story recommendations based on user behavior.
Method:
Filters out inactive users and unpopular stories.
Constructs a user-story matrix.
Uses cosine similarity to find stories similar to those a user liked.
Returns top matches for any given story.

Phase 3: Time-Based & Trend-Based Recommender
Goal: Highlight stories with lasting appeal and those that are trending during a specific time period.
Method:
Adjusts story popularity by considering the number of years since publication.
Extracts year-wise trends using grouped analysis.
Provides genre-based insights for each time window.

Phase 4: Context-Aware Recommender
Goal: Recommend festival-themed Telugu stories using real-world context.
Method:
Extracts story text from .txt files.
Detects current festivals via the Calendarific API.
Generates semantic embeddings using pretrained multilingual sentence transformers.
Uses cosine similarity to match relevant stories with festivals.

Tech Stack:
Python (Pandas, NumPy, Matplotlib, Seaborn)
Scikit-learn (Similarity computation)
Sentence Transformers (sentence-transformers library)
Calendarific API (for dynamic festival detection)
Google Colab

Outcomes
General-purpose story ranking for cold-start users.
Personalized recommendations for returning users.
Insights into long-term popular and trending stories.
Smart story suggestions based on real-life festivals.



