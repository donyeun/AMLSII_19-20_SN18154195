# APPLIED MACHINE LEARNING SYSTEM II ELEC0135 19/20
In this repository, we present our attempt to solve SemEval 2017 Competition Task 4: Twitter Sentiment Analysis. Based on recurrent neural network (RNN), precisely long short-term memory (LSTM), our approach focused on the first two sub-tasks within the competition, namely 3-point scale tweet classification and topic-based tweet sentiment classification. We picked a series of text preprocessing pipeline and pre-trained word embedding that adhere to the use of informal language tone within the Twitter environment, with the possible presence of misspelt and elongated words, as well as the use of emoticons. Although we were not officially participating, our system would have been placed 7th and 15th in the competition for the two sub-tasks, with reported average recall of 0.659 and 0.782 for task A and B, respectively.

## Structure of repository
    .
    ├── config.yaml                  # All the configuration variables such as train-test dataset ratio, etc
    ├── requirements.txt             # The required Python libraries
    ├── src/
    │   ├── original.ipynb           # The original code before being splitted into three sections
    │   ├── data_preprocessing.ipynb # Code to perform Data Preprocessing
    │   ├── train_model.ipynb        # Code to execute training phase
    │   ├── test_model.ipynb         # Code to test the resulted model from training phase
    ├── report/                      # Latex and pdf report files
    ├── data/
    │   ├── processed/               # The cropped dataset
    │   ├── external/                # The original dataset from the competition
    ├── models/
    │   ├── model_task_a.tut         # Saved/frozen model and hyperparameters for task A
    │   ├── model_task_b.tut         # Saved/frozen model and hyperparameters for task B
    │   ├── row_num.field            # Saved ROW_NUM data made with TorchText
    │   ├── sentiment.field          # Saved SENTIMENT data made with TorchText
    └── └── text.field               # Saved TEXT data made with TorchText

    
## How to Run the Code
To run the code, navigate to `/src/` folder and run `main.ipynb` in Google Colab environment (https://colab.research.google.com/). This will run the entire project pipeline, from data analytics, training and testing phase. To execute only the testing/inference mode, run `test_model.ipynb` notebook. Due to computational resource limitation, we highly depend on the service provided by Google Colab. Change the `TASK_NUMBER` variable at the top to either `A` or `B` accordingly to switch between the two sub-tasks.
