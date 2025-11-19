Base Models Used by Both Users
Model v1 (Trained by User 1) used a Custom Convolutional Neural Network (CNN) architecture. This model consists of three sequential convolutional and max-pooling blocks (with 32, 64, and 128 filters), a Flatten layer, and two dense layers (128 units and a single-unit sigmoid output) for binary classification.

Model v2 (Trained by User 2) is expected to be an improved version of the CNN architecture, possibly incorporating techniques like Dropout or Data Augmentation as part of the collaboration workflow defined in the assignment steps. (Please insert the specific architectural details of Model v2 here.)

Dataset Descriptions
Both users are working on the Cats vs. Dogs image classification task, but used separate, proprietary datasets that could not be shared.

Dataset 1 (User 1): The initial model (Model v1) was trained on the Cat & Dog Dataset (Tong Python).

Dataset 2 (User 2): The second model and cross-testing were performed on the Dogs vs Cats Redux: Kernels Edition dataset, a well-known binary classification benchmark.

Metrics on Both Datasets
The final metrics were gathered by cross-testing Model v1 on User 2's dataset. (This section requires the full set of metrics from all four required files to be complete, including Model v2 tests.)

Cross-Test: Model v1 on User 2's Dataset (test_v1_user2.json)

When Model v1 (trained by User 1) was tested on User 2's dataset, the results were as follows:

Accuracy: 0.50

Precision: 0.50

Recall: 1.00 (100%)

F1-Score: 0.67

(Insert remaining metrics here, e.g.:)

Cross-Test: Model v2 on User 1's Dataset (test_v2_user1.json)

Accuracy: [Value]

Precision: [Value]

Recall: [Value]

F1-Score: [Value]

Observations on Generalization and Domain Shift
The cross-test of Model v1 on User 2's dataset clearly demonstrates a severe case of domain shift.

The Accuracy of 50% shows that the model performs no better than random guessing on the unseen data from a different source. Crucially, the combination of 100% Recall and 50% Precision suggests the model is heavily biased toward predicting the positive class (likely "dog" in a binary setup).
It successfully captured all actual positive cases (Recall = 1.0), but its overall predictions were only correct half the time (Precision = 0.50), implying it classified every single test image as positive.

This failure in generalization is due to the model learning features specific to Dataset 1 that did not transfer to the image distribution and characteristics of Dataset 2. 
The subsequent development of Model v2 by User 2, with new techniques and training on a different distribution, is necessary to mitigate this domain shift and improve overall model robustness.
