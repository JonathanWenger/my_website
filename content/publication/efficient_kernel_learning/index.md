---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Reducing the Variance of Gaussian Process Hyperparameter Optimization with Preconditioning"
authors: ["admin", "Geoff Pleiss", "Philipp Hennig", "John P. Cunningham", "Jacob R. Gardner"]
date: 2021-07-01T10:00:00+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2021-07-01T06:00:00+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: "Gaussian processes remain popular as a flexible and expressive model class, but the computational cost of kernel hyperparameter optimization stands as a major limiting factor to their scaling and broader adoption. Recent work has made great strides combining stochastic estimation with iterative numerical techniques, essentially boiling down GP inference to the cost of (many) matrix-vector multiplies. Preconditioning -- a highly effective step for any iterative method involving matrix-vector multiplication -- can be used to accelerate convergence and thus reduce bias in hyperparameter optimization. Here, we prove that preconditioning has an additional benefit that has been previously unexplored. It not only reduces the bias of the $\\log$-marginal likelihood estimator and its derivatives, but it also simultaneously can reduce variance at essentially negligible cost. We leverage this result to derive sample-efficient algorithms for GP hyperparameter optimization requiring as few as $\\mathcal{O}(\\log(\\varepsilon^{-1}))$ instead of $\\mathcal{O}(\\varepsilon^{-2})$ samples to achieve error $\\varepsilon$. Our theoretical results enable provably efficient and scalable optimization of kernel hyperparameters, which we validate empirically on a set of large-scale benchmark problems. There, variance reduction via preconditioning results in an order of magnitude speedup in hyperparameter optimization of exact GPs."

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
#  - name: Proceedings
#    url:

url_pdf: https://arxiv.org/pdf/2107.00243.pdf
url_code: https://github.com/cornellius-gp/gpytorch
# url_dataset:
# url_poster:
# url_project:
# url_slides: 
# url_source:
# url_video: 

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Bias and variance reduction in the log-marginal likelihood and its derivatives via preconditioning."
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
