# DS301-AES
Daniel Lee &amp; JunSeob Shim DS301 Final Project: AES

# Edit made to add necessary credit to other users for using their code and results

Automated Essay Grading: Daniel Lee & Jun Seob Shim

Description:
This project focuses on the intriguing domain of automated essay grading. The initial approach began with simple machine learning models such as Linear Regression, SVM, and Random Forest. As the project matured, a shift was made to leverage deep learning models, including LSTM, BERT, and Word2Vec, aiming to enhance the accuracy and efficiency of grading.

Repository and Code Structure

Folders:
  - DeepML: Contains the AESDeepML.ipynb, which is the notebook that includes implementation and documentation for deep learning models like LSTM, BERT, and Word2Vec.
  - Dataset: Folder containing the dataset used for both simple and deep machine learning models.

Files:
  - AESSimpleML.ipynb: This notebook includes the implementation and documentation for traditional machine learning models such as Linear Regression, SVM, and Random Forest.
  - all_models_results.pdf: A comprehensive report containing the results of running both the simple and deep learning models.

Execution:

To run the code:
Import all files & folders into either google drive for colab or your local machine for jupyter. Open notebooks AESDeepML.ipynb and AESSimpleML.ipynb, then run each cell chronologically.

Results and Observations

The summarized results from running the deep ML models are available in all_models_results.pdf. The report comprises:

- Plots and tables presenting the results, specifically Kappa Score and runtime.
- Detailed information for each epoch for each set, allowing the user to follow along the training process.

Linear Regression Results:
MSE of 843.80, about 10 minutes to train and evaluate

SVM Results:
MSE of 2.23, about 20 minutes to train and evaluate

Random Forest Results:
MSE of 2.21, over 3 hours to train and evaluate

Given that the essay scores are out of 10, the MSE of our linear regression model tells us that our result is wrong and our model is not performing the way we want it to. Our SVM model gave us an MSE of 2.23, which was definitely better than our linear regression model, but still high for a dataset of scores out of 10. While the MSE of 2.21 from our random forest model is in the right direction, we were curious if we could improve on that further. So, we decided to explore deep ML models to see if they would result in better performance.

For these three models, we utilized Guarev Pande's results due to the deep ML models being too computationally expensive, which didn't allow us to run the code ourselves. We included these three results here to serve as additional information to the reader about how deep ML models could perform for our problem.

LSTM Results:
Individual Sets: Average κ of 0.685, about 30 minutes to train and evaluate.
Whole Dataset: Average κ of 0.487, about 45 minutes to train and evaluate.

BERT Results:
Individual Sets: Average κ of 0.568, over 2 hours to train and evaluate.
Whole Dataset: Average κ of 0.445, over 4 hours to train and evaluate.

Word2Vec Results: 
Individual Sets: Average κ of 0.972, about 20 minutes to train and evaluate.
Whole Dataset: Average κ of 0.968, about 30 minutes to train and evaluate.

Again, we are not trying to claim these results as our own. We merely seek to provide the reader with potential options that could be utilized.

Given that Kappa score is measured on a scale from 0-1, the performance of the two deep ML models is far from perfect. However,  the Word2Vec model performed amazingly, which is to be expected given that it was created to do exactly this sort of task. LSTM performed better than BERT, which is unexpected given that BERT specializes in contextual information, which is important in essays. 

Conclusion:
Automated essay scoring offers an efficient and standardized approach to evaluating written content. Not only does it speed up grading & feedback processes which helps both students and professors, it also allows for fair grading to all, unaffected by bias and subjectivity.

Linear Regression: Not useful for this topic due to the nature of our dataset.
SVM: Performance could be improved by finetuning hyperparameters but efficacy is great.
Random Forest: While performance is improved a little, efficacy drops massively.

LSTM: Shines in this project because of its ability to model sequential data, capturing the flow and structure in written essays.
BERT: Excels in understanding context bidirectionally due to its transformer architecture, which then provides deep insights into the contextual nature of essays.
Word2Vec: Lays the groundwork for the process by converting essays into vector representations, thereby boosting performance of the other models.

Future Work: 
Run the code to confirm Guarev Pande's Results.
Fine-tune hyperparameters to enhance synergy between the models for better performance.
Implement real-time feedback for model refinement/improvement.
Generalize the model to be able to perform on a wider array of essay genres and writing styles.
