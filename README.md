# US-Company-Bankruptcy-Prediction

## 1. Business Problem
Our analysis involves a thorough examination of numerous feature variables that contain comprehensive information about financial statement indices, from Current Assets to Total Operating Expenses, which are essential in providing an in-depth understanding of a company's financial health. In addition to this, we incorporate the temporal dimension by including a year column, which enables us to unveil trends and conditions over time. Our primary objective is to leverage this extensive dataset to predict a company's financial stability or its likelihood of facing bankruptcy.

![image](https://github.com/user-attachments/assets/2e5bcb58-d617-460c-a01e-a4c5dd857897)

## 2. Challenge
Given the highly imbalanced nature of our dataset, where approximately 97% of datapoints represent the "alive" class and only 3% represent the "failed" class, we implement several strategies for effective evaluation.

Firstly, in response to the challenge posed by imbalanced datasets, we prioritize balanced accuracy over traditional accuracy metrics when assessing our models. Traditional accuracy can be misleading in imbalanced scenarios as it tends to favor the majority class. Balanced accuracy, which considers the mean of sensitivity and specificity, offers a more reliable evaluation across all classes.

Secondly, in our model tuning, we incorporate the class_weight='balanced'  hyperparameter to address the impact of imbalanced data. This adjustment ensures that the model assigns appropriate weights to different classes during training, giving emphasis to the minority class and enhancing predictive accuracy for both major and minor classes.

Thirdly, we employ resampling techniques, specifically over-sampling, to tackle the imbalance. This involves duplicating or generating synthetic samples for the minority class, providing the model with more instances to learn and distinguish patterns related to that class. This technique is crucial in preventing bias towards the majority class and fostering a more equitable model.

Fourthly, we also leverage the SMOTE (Synthetic Minority Over-sampling Technique) method to address the imbalanced problem. SMOTE helps by creating new data points for the smaller group, making the data more balanced. This way, the model can learn better from both groups and make fair predictions.

Lastly, K-fold cross-validation serves as an additional tool to address this problem. Specifically, K-fold cross-validation, when combined with these strategies, helps us navigate the challenges posed by imbalanced datasets.

Through these thoughtful approaches, our goal is to enhance the robustness and fairness of our machine learning models in the context of imbalanced datasets.

## 3. Conclusion
In our comprehensive project journey, our primary objective was to craft a classification model that excels in balanced accuracy, particularly within the intricate landscape of a highly imbalanced dataset. Our exploration spanned various models, encompassing Logistic Regression, Random Forest, K-Nearest Neighbors (KNN), and Support Vector Machines (SVM). Despite exhaustive efforts in training diverse models, the incremental gains in balanced accuracy were modest.

Beyond model selection, our focus extended to feature selection, delving into the nuanced impact of each variable on shaping the growth and success trajectories of the companies under scrutiny.

In summary, our project underscores the paramount importance of achieving peak accuracy in predictive modeling. The preference for KNN SMOTE signifies its adeptness in navigating imbalanced data challenges. Additionally, insights gained from feature selection illuminate how specific variables shape the growth dynamics of companies.

Further enriching our understanding is the recognition that stakeholders hold different perspectives on particular issues. For companies, a grasp of their financial health guides future plans, influencing decisions to earn more, spend judiciously, or seek external assistance. Simultaneously, investors keenly analyze a company's financial standing to make informed investment decisions, directing capital where growth potential is perceived. Predicting a company's trajectory, therefore, becomes pivotal for both business entities and investors alike, shaping strategic actions and investment choices. Ultimately, our work not only aids investors in making well-informed decisions but also empowers companies to navigate toward success with a nuanced understanding of their growth dynamics.
