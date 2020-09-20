# Tinkofy
Tinkoff Advice hackathon | Skoltech, 18.09.20-20.09.20


# Setup:
Dowload dataset and weights from [https://drive.google.com/drive/folders/1UAQQjGppZ3Y8oA1mUWnJr4XPflbbVASf?usp=sharing](https://drive.google.com/drive/folders/1UAQQjGppZ3Y8oA1mUWnJr4XPflbbVASf?usp=sharing) and change data path.

# Content

1. 'AdviseSystem.ipynb' - notebook with code and examples for Recommender system.
2. 'ImprovedBaseline.ipynb' - notebook with improved baseline.


# Recommender System description

![alt text](https://github.com/kstepanov7/Tinkofy/blob/master/images/matrix_scheme.PNG?raw=true)


# Results

Our Recommender system can work in two approaches:

1. Post Factum Approach - user makes payment in one of the places belonging to a certain category (e.g. fast food restaurants), and then the system suggests him interesting places in this category for the future
![alt text](https://github.com/kstepanov7/Tinkofy/blob/master/images/PFA.jpg?raw=false)

2. Ante Factum Approach - Using a predictive model (improved baseline model) trained on transaction history, the system predicts to which category of merchants the user will more likely go, and suggests him interesting places in this category. 
![alt text](https://github.com/kstepanov7/Tinkofy/blob/master/images/AFA.jpg?raw=false)

# Baseline improvement:
We conducted search for optimal hyper parameters, and found that e.g. increasing feed forward size or model dimension actually worsens the result, and a slight improvement over the baseline can be done by increasing the number of attention heads (n_heads) to 4. We also set "MAP@30" as the main metric
