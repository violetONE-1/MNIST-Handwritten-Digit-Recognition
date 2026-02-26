# MNIST-Handwritten-Digit-Recognition

Motivation and Objective                                                       The initial objective of this project was to bridge the gap between theroy and practice of CNNs. Upon benchmarking my model against the official reference implementation, a significant architectural variance was identified:the integration of a Dropout layer. To evaluate the efficacy of Dropout as a regularization technique in mitigating overfitting, I developed a comparative study.


Experimental Design
To isolate the impact of Dropout, I designed a controlled experiment using two model variants:
*Baseline Model: A high-capacity CNN with a 512-unit fully connected layer, intentionally designed without regularization to observe potential overfitting.
*Regularized Model: The same architecture with the addition of a nn.Dropout(p=0.5) layer.
Both models were trained on the MNIST dataset using the Adam optimizer and identical hyperparameters to ensure a valid comparative analysis.


Quantitative Analysis
The experimental data confirmed that while increasing hidden layer units improves model capacity, it simultaneously elevates the risk of overfitting.
*Without Dropout: The model showed high variance in validation accuracy and signs of "memorizing" the training set.
*With Dropout: The inclusion of a stochastic Dropout layer forced the network to learn more robust features, leading to a smoother convergence and a stable 0.5% - 1.0% increase in final test accuracy.
