# APS1070 Project - Anomaly Detection Algorithm using Gaussian Mixture Model
-	Use of Panda: pd.concat; pd.DataFrame
-	Use of Numpy: pd.merge; np.arange
-	Use of matplotlib.pyplot: plt.plot; matplotlib.gridspec (bar and line plot); plt.Circle
-	Use of sklearn:
sklearn.model_selection - train_test_split
sklearn.mixture.GaussianMixture; gm.score_samples (likelihood score)
sklearn.metrics - roc_auc_score - f1_score - precision_score - recall_score
-	Use of seaborn: sns.histplot
-	Python Basics: .iloc; .loc; map(lambda p: ‘formula of p’); .tolist

Part 1 - Data Cleaning and Visualization
-	Work with the Thyroid Disease dataset which contains 6 clinical attributes to determine whether a patient referred to the clinic is hypothyroid.
-	Split the dataset into training (70%), validation (15%) and testing set (15%)

Part 2 - Single feature model with one Gaussian (n_components = 1)
-	Find the best 3 features to distinguish hypothyroid patients from not-hypothyroid patients based on the AUC of the validation set.
-	Fitting Gaussian Mixture Mode using these 3 features. (make prediction by model's scores * tr)
-	Compute AUC and F1 score for fitting a Gaussian only on not-hypothyroid patients.

Part 3 - Multiple feature model with one Gaussian (n_components = 1)
-	Using scatterplots of the features to find outliers of the non-hypothyroid groups to see if the one-Gaussian model is proper.
-	If the graph shows concentrated in a single region near the origin, one-Gaussian model is proper. If the graph shows sign of multiple distinct groups, using multi-Gaussian model is needed.

Part 4 - Single feature model with two Gaussian distributions (n_components = 2)
-	Fit two Gaussian models on hypothyroid and non-hypothyroid groups as G1 and G2 with one feature only.
-	Compute the score_sample of G1 and G2 as S1 and S2.
-	Tuning optimal c that maximizes validation set F1 Score for a model such that if S1 < c *S2 the patient is classified as hypothyroid

Part 5 - Multivariate and Mixture of Gaussians Distribution
-	Build 10 models with different combinations of features, Single/Multiple GMM on hypo/non-hypo patient groups using the same rule as part 4.
-	Calculate F1 score, AUC and the optimal c in part 4 for each model.

Part 6 - Evaluating performance on test set
-	Report the F1 Score, Precision and Recall on the test set.
