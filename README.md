# semantic-classification
Discover the nuances of LSTM and BiLSTM with various data configurations in this study. We analyze models using preprocessed and raw data, with and without dropout layers, with sparse and dense vector representations offering insights into neural network behaviors.

The below are the results we got as we performed different configurations for our model.

<img width="1006" alt="Screenshot 2024-01-07 at 1 37 45 AM" src="https://github.com/sohan2000/semantic-classification/assets/38259195/1c19441d-3ccf-41bc-bc7a-beb7bfe1bfca">


### Sparse Representation Analysis:
LSTMs give consistent poor performance with sparse vectors, whereas BiLSTM adjust well to sparsity. 
Pre-processing seems to have no effect on classification with sparse vectors.
Dropout shows negative effect on LSTMs and positive effect on BiLSTMs.

### Dense Representation Analysis:
LSTM shows varied behaviour with changes in configuration, whereas BiLSTM seems more robust in nature.
Preprocessing shows a significant drop in performance with LSTMs and a small drop one with BiLSTMs.
Dropout give performance gain in case of LSTMs. 
Combination of preprocessing and dropout benefits BiLSTMs.

### Conclusion:
With raw text, LSTM performance is directly proportional to the data sparsity.  With processed text,  LSTM performance is inversely proportional to the data sparsity.
BiLSTMs performance is inversely proportional to data sparsity in every case except for when pre-processing and dropout are applied together.
Although dropout is a regularization technique meant to improve performance of neural nets, it doesn’t always help. 
Poor results with pre-processing shows that important context information is being removed.
LSTMs are more sensitive to data sparsity than Bi-LSTMs.
