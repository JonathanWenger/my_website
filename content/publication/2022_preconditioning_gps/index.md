---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Preconditioning for Scalable Gaussian Process Hyperparameter Optimization"
authors: ["admin", "Geoff Pleiss", "Philipp Hennig", "John P. Cunningham", "Jacob R. Gardner"]
date: 2022-01-28T10:00:00+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2022-01-28T06:00:00+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "International Conference on Machine Learning"
publication_short: "ICML (oral, 2.1%)"

abstract: "Gaussian process hyperparameter optimization requires linear solves with, and log-determinants of, large kernel matrices. Iterative numerical techniques are becoming popular to scale to larger datasets, relying on the conjugate gradient method (CG) for the linear solves and stochastic trace estimation for the log-determinant. This work introduces new algorithmic and theoretical insights for preconditioning these computations. While preconditioning is well understood in the context of CG, we demonstrate that it can also accelerate convergence and reduce variance of the estimates for the log-determinant and its derivative. We prove general probabilistic error bounds for the preconditioned computation of the log-determinant, log-marginal likelihood and its derivatives. Additionally, we derive specific rates for a range of kernel-preconditioner combinations, showing that up to exponential convergence can be achieved. Our theoretical results enable provably efficient optimization of kernel hyperparameters, which we validate empirically on large-scale benchmark problems. There our approach accelerates training by up to an order of magnitude."

# Summary. An optional shortened abstract.
summary: ""

tags: ["machine learning", "numerical analysis", "preconditioning", "gaussian processes"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
- name: arXiv
  url: https://arxiv.org/abs/2107.00243 
- name: Proceedings
  url: https://proceedings.mlr.press/v162/wenger22a.html

url_pdf: https://arxiv.org/pdf/2107.00243.pdf
url_code: https://github.com/cornellius-gp/gpytorch
# url_dataset:
url_poster: poster.pdf
# url_project:
url_slides: talk.pdf
# url_source:
# url_video: 

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Preconditioning reduces bias and variance in the stochastic approximations of the log-marginal likelihood and its derivatives."
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
