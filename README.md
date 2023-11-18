# SummarizeIt: NLP-Driven Insights into Medical Abstracts

Welcome to SummarizeIt, the NLP-powered tool that is reshaping how medical researchers review literature. By classifying sentences into categories such as objectives, methods, results, and conclusions, SummarizeIt enables quick skimming and deeper dives into research papers, enhancing productivity and understanding.

## Introduction

Drawing inspiration from the pivotal 2017 research presented in 'PubMed 200k RCT', SummarizeIt leverages deep learning to parse and categorize complex medical text. The result? A nuanced tool that empowers researchers to efficiently navigate and extract value from extensive medical literature.

## Dataset Overview

Our models are trained using the [PubMed 200k RCT dataset](https://github.com/Franck-Dernoncourt/pubmed-rct), a robust collection of randomized controlled trials. Key features include:

- **PubMed 20k RCT**: A focused subset for targeted analysis.
- **Number Replacement**: In some variants, numbers are replaced with '@' to ensure the model isn't biased by specific numerical data.

### Visualizing the Data

Understanding the makeup of our dataset is crucial. The count plot below illustrates the distribution of sentence types, which informs our model training:

![Dataset Sentence Role Distribution](images/count%20plot.png)

*Distribution of sentence roles within the dataset, highlighting the variety of data our models are trained on.*

## Model Development Journey

Embarking on a journey through machine learning, we explored various architectures, each with its own strengths:

- Naive Bayes Model – Our starting point, achieving 72% accuracy.
- Conv1D Model – Enhanced pattern recognition brought us to 78% accuracy.
- Universal Sentence Encoder – Leveraged pre-trained models for a solid 75% accuracy.
- Character-Level Conv1D – Diving deeper into textual nuances, reaching 73% accuracy.
- Hybrid Token-Character Models – Combining multiple data representations to improve to 76% accuracy.
- Position-Enhanced Models – Incorporating sentence position for a significant leap to 81% accuracy.
- BERT-Embedded Model – The pinnacle of our efforts, integrating state-of-the-art BERT embeddings to achieve a remarkable 88% accuracy.

### Comparative Model Performance

This graph presents a comparative view of our models, showcasing the iterative improvement in performance metrics:

![Model Performance Comparison](images/modeling%20results.png)

*Comparative analysis of model performance, guiding our focus towards the most effective architectures.*

### F1 Score Breakdown

F1 scores provide a balance between precision and recall. Here's how our models stack up:

![F1 Score Comparison](images/f1%20score%20images.png)

*F1 scores of different models, demonstrating the balanced performance of our best model.*

## Our Best Model

In the end, the BERT-Embedded Model emerged as our champion, setting a new standard for accuracy in sentence classification.

### Architecture of Our Champion Model

Take a look at the structure of our most effective model:

![Best Performing Model Architecture](images/final%20model.png)

*A detailed look at the BERT-Embedded Model that outperformed the rest.*

### Exploring Other Architectures

We didn't stop at the first success; we explored further:

![Additional Model Architectures](images/final%20model%201.png)

*Exploratory models that contributed to our understanding and final design.*

## SummarizeIt in Action

Here's a glimpse of what SummarizeIt can do:

![Application Output Example](images/app%20output.png)

*A snapshot of the SummarizeIt tool categorizing sentences from a medical abstract.*

## Technical Stack

Building SummarizeIt required a diverse set of tools, including:

- **TensorFlow**: The backbone of our deep learning models.
- **TensorFlow Text and TensorFlow Hub**: For processing and embedding sophisticated text data.
- **Scikit-Learn**: Our go-to for model metrics and data preprocessing.
- **Matplotlib**: For all our visualization needs.
- **NumPy and Pandas**: For handling data structures and numerical operations.
- **spaCy**: The NLP powerhouse behind our text analysis.

## Conclusion and Invitation

SummarizeIt represents a leap forward in combining AI with medical research, streamlining the review of literature. We're excited to invite the community to engage with us—whether it's feedback, questions, or collaborative efforts.

---
