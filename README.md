# Understanding-ML

A simple Python project to get an understanding of how **Machine Learning** works.  
The project follows the standard ML pipeline: importing data, cleaning, splitting into train/test datasets, training a model, making predictions, evaluating results, and visualizing outcomes.

---

## Overview
- Imported a dataset from **Kaggle**.  
- Preprocessed and split the dataset into **training** and **testing** sets.  
- Built and trained a **Decision Tree (DT) model**.  
- Used the model to **predict outcomes**.  
- Visualized the Decision Tree with the **Graphviz `.dot` format**.  
- Interpreted model decisions based on **age and gender**.

---

## Dependencies
The following Python libraries were used:
- `pandas` → for data manipulation  
- `scikit-learn` → for ML model building and training  
- `graphviz` → for visualizing the Decision Tree  

# Walkthrough/Test/Understanding

Predicting Model:

<img width="284" height="49" alt="image" src="https://github.com/user-attachments/assets/163a468f-0bcd-4bb4-bf57-cbb2623afab2" />

<img width="284" height="33" alt="image" src="https://github.com/user-attachments/assets/bb8aec29-ccd6-48d4-8c21-d7cfc1bbf5d7" />


Splitting model:

While splitting the dataset, I evaluated the model’s accuracy. Initially, it achieved 100%, but after several runs it dropped to around 67–70%. This variation is due to the small dataset size, which provides limited data for the model to learn and generalize from.

<img width="432" height="28" alt="image" src="https://github.com/user-attachments/assets/89277c23-86a1-43a3-9820-f027c5a2388b" />

<img width="262" height="43" alt="image" src="https://github.com/user-attachments/assets/0b394266-854b-4f97-a204-8166df716230" />


Using Graphiz to visualise

<img width="396" height="89" alt="image" src="https://github.com/user-attachments/assets/c7e70266-0f31-4459-8209-e447fdcc119b" />

<img width="565" height="214" alt="image" src="https://github.com/user-attachments/assets/73723ced-f401-4463-a486-238d3060dea3" />

Dot extension in vscode:

<img width="571" height="114" alt="image" src="https://github.com/user-attachments/assets/629ebf8b-1bbc-430f-912d-306298eaf676" />

After downloading the .dot file, run the following command in your terminal:
```dot -Tpng music-recommender.dot -o tree.png```
This will generate a PNG image (tree.png) of the decision tree for easier visualization.

<img width="349" height="368" alt="image" src="https://github.com/user-attachments/assets/421bc2a5-959d-4057-9952-a37c8f483358" />

The decision tree generates predictions based primarily on age (and to a lesser extent, gender). For example:
- If a person’s age is greater than 41, they are most likely classified as listening to Classical music.
- If age is less than or equal to 28.5, the model predicts Jazz; otherwise, it predicts HipHop.
- If age is less than or equal to 17.5, the model predicts HipHop; otherwise, it predicts Dance.
Here, “HipHop,” “Jazz,” etc. represent the genre classes that the model assigns based on the individual’s profile age.
