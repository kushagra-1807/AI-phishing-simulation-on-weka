# Phishing Website Detection in Weka

Comparison of six classifiers on the UCI Phishing Websites dataset using 10-fold cross-validation in the Weka Explorer.

## Dataset
Mohammad, R. and McCluskey, L. (2015). Phishing Websites. UCI Machine Learning Repository. https://doi.org/10.24432/C51W2X
11,055 instances (4,898 phishing, 6,157 legitimate), 30 features coded -1, 0, 1. Class attribute: Result.

## Tool
Weka Explorer

## Results
| Algorithm | Accuracy | ROC area |
|---|---|---|
| Random Forest | 97.27% | 0.996 |
| IBk (k = 7) | 97.18% | 0.989 |
| J48 | 95.88% | 0.984 |
| Logistic | 93.99% | 0.987 |
| SMO (RBF) | 93.80% | 0.936 |
| Naive Bayes | 92.98% | 0.981 |

Feature ranking by information gain (InfoGainAttributeEval with Ranker) is in results/weka feature ranking.txt. The top feature is SSLfinal_State (0.499).

## Repeating the experiment
1. Open Weka Explorer and load data/Training Dataset.arff.
2. On the Classify tab, choose a classifier, select Cross-validation with 10 folds, and click Start.
3. For the feature ranking, open Select attributes, choose InfoGainAttributeEval with the Ranker search, and click Start.

Raw output for each run is in results/ and settings screenshots are in screenshots/.
