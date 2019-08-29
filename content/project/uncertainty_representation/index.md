---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "On Probability Calibration and Overconfidence in Image Classification"
summary: "Accurate representation of uncertainty in classification problems can be as critical as high prediction accuracy in computer vision, e.g. in safety-critical applications. While Bayesian methods provide a principled approach to modelling uncertainty, many classifiers do not represent uncertainty well due to model misspecification or overfitting to training data. We introduce concepts of over- and underconfidence and  demonstrate a theoretical connection to probability calibration."
authors: [admin]
tags: ["computer-vision", "classification", "uncertainty-representation"]
categories: []
date: 2019-08-29T16:27:47+02:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Segmented scenery of Tübingen from the cityscapes data set [[Cordts2016](https://doi.org/10.1109/CVPR.2016.350)] illustrating a classification task in a safety-critical application, where an accurate notion of uncertainty is needed."
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

# url_code: ""
# url_pdf: ""
# url_slides: ""
# url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---


# Introduction

The classification of objects in images is a very common and important problem in computer vision. Take for example an autonomous robot trying to navigate an unknown environment. The robot needs to be able to tell whether it can safely move in a certain direction or interact with an object without causing harm. Another application is in the medical realm. Step by step automated systems are introduced to interpret images from MRI scans or mammograms for example. Naturally, very high accuracy is required in important decisions such as whether a patient faces a cancer diagnosis.

{{< figure src="/img/projects/uncertainty_representation/ribli_mammography.jpg" title="Lesions detected in mammograms by a convolutional neural network [[Ribli2018](https://doi.org/10.1038/s41598-018-22437-z)]." numbered="true" >}}

## Importance of Prediction Uncertainty

But what can be as critical as achieving high prediction accuracy is to give an accurate representation of the classifier's confidence in its prediction. For example, take a prediction system diagnosing breast cancer based on mammograms. Suppose the system encounters an image very different from the type of images it was trained on. In this case it could be very important to get an expert opinion from a medical doctor. This is only possible with an uncertainty estimate that reflects the system's lack of information about the given image. Recognizing such out-of-distribution samples, where a classifier's prediction is likely not useful is key in image classification.

## Relationship to Active Learning

A good representation of a classifier's uncertainty also allows for practitioners to improve the given model. For example, if a classifier deployed in an autonomous vehicle gives high uncertainty estimates for a particular traffic situation, say a construction site, then it is likely that providing more labelled data of such situations will improve predictive performance. This type of learning strategy is known as active learning[^1]. When a classifier is presented with new unlabelled data it chooses those samples which it deems most informative. One such query strategy is called uncertainty sampling where labels for samples which the model is unsure about are requested.

{{< figure src="/img/projects/uncertainty_representation/active_learning.png" title="Illustration of active learning reprinted from [[CVLAB EPFL](https://cvlab.epfl.ch/research/research-machinelearning/page-123199-en-html/)]." numbered="true" >}}

# Measures of Uncertainty Representation

In order to compare classifiers with respect to their quality of uncertainty representation, we have to define what we mean when saying a classifier represents uncertainty well. Let $(X,Y) \subset \mathcal{X} \times \mathcal{Y}$ be a random variable describing our data and the associated labels. Further let $p(x,y)$ be the joint distribution of $X$ and $Y$. Our task in statistical classification is to find a function $\hat{p}(y \mid x)$ which approximates the ground truth predictive distribution $p(y \mid x)$ as well as possible. We will now introduce ways to measure the capability of our model to represent its uncertainty about a prediction.

## Negative Log-likelihood or Cross entropy

The _negative log-likelihood_ (NLL) is often used when fitting a probabilistic model. Minimizing the NLL is equivalent to performing [maximum likelihood estimation](https://en.wikipedia.org/wiki/Maximum_likelihood_estimation) due to the monotonicity of the logarithm. In the context of deep learning it is also known as [cross entropy](https://en.wikipedia.org/wiki/Cross_entropy) loss, highlighting its connection to information theory. It is defined as follows:

$$H(p, \hat{p}) = \mathbb{E}_p \left [-\log \hat{p} \right ]$$

The negative log-likelihood is minimized when we recover the ground truth predictive distribution, i.e. when $\hat{p}=p$.

## Calibration

When a model outputs a confidence of 80% for each of a given set of predictions, we would expect to be correct about 80% of the time. This notion of the confidence matching the empirical accuracy is called _calibration_. In order to define calibration rigorously let $\hat{y}$ be the class prediction of our model and $\hat{p}$ its associated confidence, then a model is calibrated if and only if

$$\mathbb{E}\left [{1_{\hat{y} = y} \mid \hat{p}}\right ] = \hat{p},$$

i.e. when a model's confidence in a prediction matches its probability of being correct. One way to measure the degree of calibration is to compute the _expected calibration error_ (ECE)[^2]

$$\\text{ECE}\_q = \mathbb{E} [ | \hat{p} - \mathbb{E} [1_{\hat{y} = y} \mid \hat{p}  ] |^q ]^\{\frac{1}{q}\}$$

for $1 \leq q < \infty$ and the _maximum calibration error_ (MCE)

$$\\text{ECE}\_\{\infty\} = \max\_\{p \in [0,1]\} | p - \mathbb{E} [1\_{\hat{y} = y} \mid \hat{p} = p ] |.$$

In a safety-critical application, it might be necessary to enforce a low MCE. A concise way to visualize the degree of calibration of a model are so called _reliability diagrams_[^3].

{{< figure src="/img/projects/uncertainty_representation/nocal_sharp.png" title="Example of a reliability diagram showing an uncalibrated classifier and its confidence histogram on a test set." numbered="true" >}}

## Sharpness

While calibration is a important property it does not suffice. In fact it is trivial to construct a calibrated classifier, if the marginal class probabilities are known. Suppose we are faced with a binary classification problems where both classes are equally likely to occur. Then a classifier which guesses a class randomly and always predicts 50% confidence is calibrated, but useless. Therefore we introduce the _sharpness_ of a model as

$$\text{sharp}(f) = \mathbb{Var}\left \[{\hat{p}}\right \].$$

It describes how close the confidence estimates of our model are to 0 and 1.

## Over- and Underconfidence

Finally, we will examine the notions of over- and underconfidence[^4]. Let $\text{conf}(f,x) \in [0,1]$ be the confidence score output by a model $f$ at $x$. We define the _overconfidence_ of $f$ as the expected confidence on the misclassified samples

$$o(f) = \mathbb{E}[\text{conf}(f,x) \mid \hat{y} \neq y]$$

and analoguously _underconfidence_ as the expected uncertainty on the correctly classified samples

$$u(f) = \mathbb{E}[\text{unc}(f,x) \mid \hat{y} = y] = \mathbb{E}[{1 - \text{conf}(f,x) \mid \hat{y} = y}].$$

Note that these quantities are by definition independent of accuracy of a model. We are particularly interested in overconfidence from the viewpoint of active learning, since if overconfidence is low, than our notion of confidence corresponds well to samples we classify incorrectly. In an uncertainty querying approach we would then request samples which are likely to improve our predictions in the future.


# Relationship between Overconfidence and Calibration

As it turns out the above notions are related. We will now present some theoretical results linking them. We hope to develop an approach to decrease overconfidence of a classifier by leveraging existing techniques for calibration.

Assume $\text{conf}(f,x) = \hat{p}$, then the following relationship between over- / underconfidence and the expected calibration error holds

$$|o(f)P(\hat{y} \neq y) -u(f)P(\hat{y} = y) | \leq \text{ECE}_p \leq \text{ECE}_q$$

for $1 \leq p < q \leq \infty$. This result is intriguing since it links the notion of probability calibration to over- and underconfidence. There are various algorithms (Platt scaling, Isotonic Regression, Bayesian Binning by Quantiles, Temperature Scaling, ...) which calibrate a given model. This theorem tells us that calibrating a model _fixes the ratio between over- and underconfidence_. In the case of perfect calibration the ratio is given by the _odds of a correct prediction_. However it does not yet point to a way of reducing them jointly.

<!---
The next result links sharpness to over- and underconfidence.

This points to a way of reducing both overconfidence and underconfidence jointly.


# (Regularized) Calibration

--->

[^1]: Burr Settles. _Active learning literature survey_. In: University of Wisconsin, Madison 52.55-66 (2010)
[^2]: Naeini, M. P., Cooper, G. F. & Hauskrecht, M. _Obtaining Well Calibrated Probabilities Using Bayesian Binning_ in Proceedings of the Twenty-Ninth AAAI Conference on Artificial Intelligence, (AAAI Press, 2015)
[^3]: DeGroot, M. H. & Fienberg, S. E. The Comparison and Evaluation of Forecasters. Journal of the Royal Statistical Society. Series D (The Statistician) (1983)
[^4]: Mund, D., Triebel, R. & Cremers, D. _Active online confidence boosting for efficient object classification_ in 2015 IEEE International Conference on Robotics and Automation (ICRA) (2015)
