# FairPut — Fair Machine Learning Output Framework

[Framework Case Study](https://colab.research.google.com/drive/1uxSP5_CuhxjjhcT_iIeL6lsmx1gwO5B6)

This is a holistic approach to implement fair outputs at the individual and group level.

FairPut is a light open framework that describes a preferred process at the end of the machine learning pipeline to enchance model fairness. Developers and researchers first follow the normal table processing, table exploration, feature processing, feature extraction, and model validation steps to obtain the **best possible model** to maximise a certain metric like sales or profit. The FairPut methodology follows on from this initial process. The aim is to simultaneously enhance model interpretability, robustness, and fairness while maintaining a reasonable level of accuracy. FairPut unifies various recent machine learning constructs in a practical manner. This method is model agnostic, but this particular development instance uses LightGBM.

#### **1. [Model Explainability](https://colab.research.google.com/drive/1uxSP5_CuhxjjhcT_iIeL6lsmx1gwO5B6#scrollTo=pXftn6tIdi5f&line=1&uniqifier=1)**
---------------
*	Model Respecification 
       * Protected Values Prediction
       * Model Constraints
       * Hyperparameter Modelling
       * Interpretable Model
       * Global Explanations
       * Monotonicity Feature Explanations
*	Quantitative Validation 
       * Level Two Monotonicity
       * Relationship Analysis
       * Partial Dependence (LV1) Monotonicity
       * Feature Interactions
       * Metrics and Cut-off
#### **2. [Model Robustness](https://colab.research.google.com/drive/1uxSP5_CuhxjjhcT_iIeL6lsmx1gwO5B6#scrollTo=cGreStojd5oc)**
---------------
  *	Residual Deviation
  *	Residual Explanations
  *	Benchmark Competition
  *	Adversarial Attack

#### **3. [Regulatory Fairness](https://colab.research.google.com/drive/1uxSP5_CuhxjjhcT_iIeL6lsmx1gwO5B6#scrollTo=HGLUFEIBbC0s)**
---------------
  *	Group
      *  Disparate Error Analysis
            * Parity Indicators
            * Fair Lending Measures
      *  Model Agnostic Processing
            * Reweighing Preprocessing
            * Disparate Impact Preprocessing
            * Calibrate Equalized Odds
      *  Feature Decomposition
  *	Individual
      *  Reasoning
          * Individual Disparity
          * Reasoning Codes
      *  Example Base
            * Prototypical
            * Counterfactual
            * Contrastive


If you end up using any of the novel techniques, or the framework as a whole, you can cite the following. 

BibTeX entry:

```
@software{fairput,
  title = {{FairPut}: Fair Machine Learning Output Framework.},
  author = {Snow, Derek},
  url = {https://github.com/firmai/fairput/},
  version = {1.15},
  date = {2020-03-31},
}
```

What Questions Do We Attempt to Answer?
------------

1. Can the model predict the outcome using just protected values? (Protected Value Prediction)
1. Is the model monotonic and are variables randomly selected? (Model Constraints, LV1 & LV2 Monotonicity)
1. Is the model explainable? (Model Selection, Feature Interactions)
1. Can you explain the predictions globally and locally? (SHAP)
1. Does the model perform well? (Metrics)
1. What indivuals have received the most and least accurate predictions? (Residual Deviation)
1. Can you point to the feature responsible for large individual residuals? (Residual Explanations)
1. What feature values could potentially be outliers due to their misprediction? (Residual Explanations)
1. Do some models perform better at predicting the outcomes for a certain type of individual? (Benchmark Competition)
1. Can the model outcome be changed by artificially perturbing certain values of interest? (Adverserial Attack)
1. Do certain groups suffer relative to others as measured through group statistics? (Parity Indicators, Fair Lending Measures)
1. Can various data and prediction processing techniques improve these group statistics? (Model Agnostic Processing)
1. What features are driving the structural differences between groups controlling for demographic factors? (Feature Decomposition)
1. What inviduals have received the most unfair prediction or treatment by the model? (Individual Disparity)
1. Why did the model decide to predict a specific outcome for a particular individual or sub-group of individuals? (Reasoning Codes)
1. What indviduals are most similar to those receiving unfair treatment, were these indivduals treated similary? (Prototypical)
1. What individual is the closest related instance to a sample individual but has a different predicted outcome? (Counterfactual)
1. What is the minimal feature pertubation necessary to switch an individual's prediction to another category? (Contrastive)
1. What is the maximum perturbation possible while the model prediction remains the same? (Contrastive)





