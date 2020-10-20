---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Probabilistic Linear Solvers for Machine Learning"
authors: ["admin", "Rudolph Triebel", "Hedvig Kjellström"]
date: 2020-10-20T16:55:42+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2020-10-20T06:11:48+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "arXiv"
publication_short: ""

abstract: "Many applications for classification methods not only require high accuracy but also reliable estimation of predictive uncertainty. However, while many current classification frameworks, in particular deep neural network architectures, provide very good results in terms of accuracy, they tend to underestimate their predictive uncertainty. In this paper, we propose a method that corrects the confidence output of a general classifier such that it approaches the true probability of classifying correctly. This classifier calibration is, in contrast to existing approaches, based on a non-parametric representation using a latent Gaussian process and specifically designed for multi-class classification. It can be applied to any classification method that outputs confidence estimates and is not limited to neural networks. We also provide a theoretical analysis regarding the over- and underconfidence of a classifier and its relationship to calibration. In experiments we show the universally strong performance of our method across different classifiers and benchmark data sets in contrast to existing classifier calibration techniques."

# Summary. An optional shortened abstract.
summary: ""

tags: ["gaussian-processes", "non-parametric", "classification"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: https://arxiv.org/pdf/1906.04933.pdf
url_code: https://github.com/JonathanWenger/pycalib
# url_dataset:
# url_poster:
# url_project:
url_slides: nonparametric_calibration_talk.pdf
# url_source:
# url_video:

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
