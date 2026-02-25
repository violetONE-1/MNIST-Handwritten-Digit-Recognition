# MNIST-Handwritten-Digit-Recognition

Motivation and Objective                                                       The initial objective of this project was to bridge the gap between theroy and practice of CNNs. Upon benchmarking my model against the official reference implementation, a significant architectural variance was identified:the integration of a Dropout layer. To evaluate the efficacy of Dropout as a regularization technique in mitigating overfitting, I developed a comparative study.


Experimental Design
To isolate the impact of Dropout, I designed a controlled experiment using two model variants:
*Baseline Model: A high-capacity CNN with a 1024-unit fully connected layer, intentionally designed without regularization to observe potential overfitting.
*Regularized Model: The same architecture with the addition of a nn.Dropout(p=0.5) layer.
Both models were trained on the MNIST dataset using the Adam optimizer and identical hyperparameters to ensure a valid comparative analysis.


Quantitative Analysis
