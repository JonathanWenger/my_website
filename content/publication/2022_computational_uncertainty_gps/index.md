---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Posterior and Computational Uncertainty in Gaussian Processes"
authors: ["admin", "Geoff Pleiss", "Marvin Pförtner", "Philipp Hennig", "John P. Cunningham"]
date: 2022-06-01T10:00:00+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2022-06-01T06:00:00+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "Advances in Neural Information Processing Systems"
publication_short: "NeurIPS"

abstract: "Gaussian processes scale prohibitively with the size of the dataset. In response, many approximation methods have been developed, which inevitably introduce approximation error. This additional source of uncertainty, due to limited computation, is entirely ignored when using the approximate posterior. Therefore in practice, GP models are often as much about the approximation method as they are about the data. Here, we develop a new class of methods that provides consistent estimation of the combined uncertainty arising from both the finite number of data observed and the finite amount of computation expended. The most common GP approximations map to an instance in this class, such as methods based on the Cholesky factorization, conjugate gradients, and inducing points. For any method in this class, we prove (i) convergence of its posterior mean in the associated RKHS, (ii) decomposability of its combined posterior covariance into mathematical and computational covariances, and (iii) that the combined variance is a tight worst-case bound for the squared error between the method's posterior mean and the latent function. Finally, we empirically demonstrate the consequences of ignoring computational uncertainty and show how implicitly modeling it improves generalization performance on benchmark datasets. "

# Summary. An optional shortened abstract.
summary: ""

tags: ["probabilistic numerics", "machine learning", "numerical analysis", "gaussian processes"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
- name: arXiv
  url: https://arxiv.org/abs/2205.15449 
#  - name: Proceedings
#    url:

url_pdf: https://arxiv.org/pdf/2205.15449.pdf
url_code: https://github.com/JonathanWenger/itergp
# url_dataset:
# url_poster:
# url_project:
# url_slides: 
# url_source:
url_video: https://youtu.be/xsXifiz2Zfo

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Computational uncertainty after four iterations of our Algorithm. Computational uncertainty is small in parts of the input space where there is either no data or computation was targeted already."
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
