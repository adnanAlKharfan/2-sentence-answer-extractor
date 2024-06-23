# 2-Sentence Answer Extractor

 Deep learning model that extracts answer from two sentences.

## Note

I ran the code on Google Colab and forgot to create the `requirements.txt` file. Please install the necessary dependencies manually.

## Features

- Preprocesses the data 
- Trains a neural network model to extract answers from two sentences
- Evaluates the model and visualizes the results

## Dataset

The bAbI dataset is a set of 20 tasks designed to test text understanding and reasoning. Each task has a specific focus, such as basic deduction, induction, counting, or pathfinding. For this project, we use task 1: Single Supporting Fact, which involves reading two sentences and answering a question based on them.

### Download and Extraction

The dataset is downloaded from the S3 storage and extracted using the following commands in the notebook:

```python
!wget https://s3.amazonaws.com/text-datasets/babi_tasks_1-20_v1-2.tar.gz
!tar -xzvf babi_tasks_1-20_v1-2.tar.gz
```

### Dataset Structure

The dataset contains several text files, each corresponding to a specific task. For task 1, the files used are:

- qa1_single-supporting-fact_train.txt
- qa1_single-supporting-fact_test.txt

Each line in these files represents a sequence of sentences or a question-answer pair. Sentences are labeled with a line number, while questions are followed by an answer and a list of supporting sentences.

### Example

- Mary moved to the bathroom.
- John went to the hallway.
- Where is Mary? bathroom

## Expermint Result

- Training Accuracy: 74%, Validation Accuracy: 67%.
- Training Loss: 0.7815, Validation Loss: 0.9786.

### Predict Result:

- Daniel moved to the bathroom.
- Mary journeyed to the garden.
- Where is Daniel?
- predication: `bathroom`


## Getting Started

### Prerequisites

- Python 3.x
- Required libraries: `numpy`, `keras`, `matplotlib`

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests or if you have any ideas to improve the accuracy.

## Contact

For any inquiries or support, please contact [Adnan AlKharfan](https://github.com/adnanAlKharfan).
   
