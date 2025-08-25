# Book-s
Lab3

#Exercise 1

##Steps:
No single classifier is the best because every dataset is different, and each algorithm has its own strengths and weaknesses.
The size of the dataset matters, a small dataset might make complex models overfit, while simple models may underfit a large dataset. 
If the data has a lot of noise, simpler models usually handle it better since complex models can overfit to random errors. 
Similarly, if the classes are easily separable, linear models are sufficient, but if the patterns are more complex, non-linear models are needed. 

#Exercise 2

The Perceptron fails on the moons dataset because it is a linear classifier, meaning it can only separate data using a straight line (or a hyperplane in higher dimensions). The moons dataset, however, is nonlinearly separable, consisting of two interleaving half-circles, so no straight line can perfectly divide the classes. As a result, the Perceptron is unable to correctly classify many points, leading to a low accuracy on this dataset.

#Excercise 3

C=0.01 (underfitting)
•	Smooth, almost linear boundary
•	May misclassify points at class edges
•	Accuracy might be slightly lower

C=1 (good generalization)
•	Boundary adapts to data moderately
•	Often gives highest test accuracy

C=100 (overfitting)
•	Boundary follows training points closely
•	May perfectly classify training but slightly worse on test if there’s noise

#Exercise 4

The Support Vector Machine (SVM) uses the parameter C to balance how strict the model is when drawing its decision boundary. With C = 1.0, the model is more flexible and allows some mistakes so that it can keep a wider margin between classes, which helps prevent overfitting. But when C is increased to 100, the model becomes stricter, trying to classify almost every training point correctly. This creates a much narrower margin because the boundary shifts closer to the training data. While this can boost accuracy on the training set, it also increases the chance of overfitting, which means the model might not perform well on new, unseen data.

#Exercise 5

 Moons dataset:
•	Low gamma - smooth boundary, may underfit.
•	Medium gamma - fits nicely.
•	High gamma - overfits training data.

 Iris dataset:
•	Linear SVM works well because petal features are almost linearly separable.
•	RBF SVM also works, but a linear kernel is simpler and sufficient

#Exercise 6

Using Gini with max_depth=4, the tree gives an accuracy of around 0.95.
Using Entropy with the same depth, the accuracy is similar.

#Exercise 8

 k=1: Model memorizes training data, high variance, overfitting - might misclassify test points slightly.
 k=5: Good balance, moderate bias and variance - usually best generalization.
 k=10: Model averages over more neighbors, smoother boundaries, underfitting if too large - may ignore local patterns.

#Exercise 9

Classifier	      Linear vs Nonlinear	Discussion
Perceptron	      Linear	            Works best on linearly separable data, struggles on nonlinear
Logistic Reg     	Linear	            Linear decision boundary, sensitive to feature scaling
SVM (RBF)	        Nonlinear	          Can handle nonlinear data via kernel trick
Decision Tree	    Nonlinear	          Can model complex patterns, may overfit
Random Forest	    Nonlinear	          Ensemble of trees, reduces overfitting, robust
KNN              	Both	Flexible      works well with local patterns; choice of k and distance matters


#Questions

Regularization prevents overfitting by keeping the model simple. It adds a small penalty to big weights, so the model focuses on the main patterns instead of memorizing noise in the training data.
Ensembles vs. simple models: Simple models are easy to understand and work well on small or clean data. Ensembles combine many models to improve accuracy and reduce errors, but they are harder to interpret. Use ensembles when you care more about performance than simplicity.





