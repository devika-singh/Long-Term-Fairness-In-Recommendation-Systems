### Pointers: 
- [Paper (arxiv preprint)](https://arxiv.org/pdf/2101.03584)
- [Dataset (MovieLens 100K Dataset)](https://grouplens.org/datasets/Movielens/)
- [Experimental data (Github)](https://github.com/TobyGE/FCPO)
- [Personal Implementation (Google Colab Link)](https://colab.research.google.com/drive/1ZNfXGe6nSjRmBTUGD2ALOLjtmUfhw96Y#scrollTo=8nuKH3BfrWL3)

### Explanation Video
![Phase 1 - The original code](https://github.com/user-attachments/assets/0d3d5eeb-4ac2-4034-8085-192e8985ea01)
![Phase 2 - Our improvements](https://github.com/user-attachments/assets/b846198b-248c-4de9-9457-326330ed0a55)


### MovieLens 100K Dataset
- 100,000 ratings (1-5) from 943 users on 1682 movies.
- Each user has rated at least 20 movies.
- Simple demographic info for the users (age, gender, occupation, zip)
- Collected through the MovieLens web site from September 19th, 1997 through April 22nd, 1998
- Data has been cleaned up with  80%/20% splits of the data into training and test data
- Detailed Data File Description: 
  - u.data : This is a tab separated list of user id | item id | rating | timestamp (unix seconds since 1/1/1970 UTC)
  - u.info : The number of users, items, and ratings in the u.data.
  - u.item : this is a tab separated list of
              movie id | movie title | release date | video release date |
              IMDb URL | unknown | Action | Adventure | Animation |
              Children's | Comedy | Crime | Documentary | Drama | Fantasy |
              Film-Noir | Horror | Musical | Mystery | Romance | Sci-Fi |
              Thriller | War | Western |
              The last 19 fields are the genres, a 1 indicates the movie
              is of that genre, a 0 indicates it is not; movies can be in
              several genres at once.
  - u.genre : A list of the genres.
  - u.user : Demographic information, tab separated list of
              user id | age | gender | occupation | zip code
  - u.occupation : A list of the occupations.

### FCPO: Fairness Constrained Policy Optimization
Use an Actor-Critic learning scheme, but with an extra critic network designed for the fairness constraint.
