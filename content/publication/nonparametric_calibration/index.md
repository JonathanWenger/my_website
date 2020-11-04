---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Non-Parametric Calibration for Classification"
authors: ["admin", "Hedvig Kjellström", "Rudolph Triebel"]
date: 2020-06-02T16:44:42+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2019-08-29T06:11:48+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "Proceedings of the 23rd International Conference on Artificial Intelligence and Statistics (AISTATS)"
publication_short: "AISTATS"

abstract: "Many applications of classification methods not only require high accuracy but also reliable estimation of predictive uncertainty. However, while many current classification frameworks, in particular deep neural networks, achieve high accuracy, they tend to incorrectly estimate uncertainty. In this paper, we propose a method that adjusts the confidence estimates of a general classifier such that they approach the probability of classifying correctly. In contrast to existing approaches, our calibration method employs a non-parametric representation using a latent Gaussian process, and is specifically designed for multi-class classification. It can be applied to any classifier that outputs confidence estimates and is not limited to neural networks. We also provide a theoretical analysis regarding the over- and underconfidence of a classifier and its relationship to calibration, as well as an empirical outlook for calibrated active learning. In experiments we show the universally strong performance of our method across different classifiers and benchmark data sets, in particular for state-of-the art neural network architectures."

# Summary. An optional shortened abstract.
summary: ""

tags: ["calibration", "non-parametric", "gaussian processes", "classification"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
 - name: arXiv
   url: https://arxiv.org/abs/1906.04933
 - name: Proceedings
   url: http://proceedings.mlr.press/v108/wenger20a.html

url_pdf: https://arxiv.org/pdf/1906.04933.pdf
url_code: https://github.com/JonathanWenger/pycalib
# url_dataset:
# url_poster:
# url_project:
# url_slides: nonparametric_calibration_talk.pdf
# url_source:
url_video: https://slideslive.com/38929965/nonparametric-calibration-for-classification

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Multi-class calibration using a latent Gaussian process."
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
