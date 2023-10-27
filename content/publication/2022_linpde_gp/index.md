---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Physics-Informed Gaussian Process Regression Generalizes Linear PDE Solvers"
authors: ["Marvin Pförtner", "Ingo Steinwart", "Philipp Hennig", "admin"]
date: 2022-12-23T10:00:00+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2022-12-23T06:00:00+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: "arXiv preprint"
publication_short: "arXiv preprint"

abstract: "Linear partial differential equations (PDEs) are an important, widely applied class of mechanistic models, describing physical processes such as heat transfer, electromagnetism, and wave propagation. In practice, specialized numerical methods based on discretization are used to solve PDEs. They generally use an estimate of the unknown model parameters and, if available, physical measurements for initialization. Such solvers are often embedded into larger scientific models or analyses with a downstream application such that error quantification plays a key role. However, by entirely ignoring parameter and measurement uncertainty, classical PDE solvers may fail to produce consistent estimates of their inherent approximation error. In this work, we approach this problem in a principled fashion by interpreting solving linear PDEs as physics-informed Gaussian process (GP) regression. Our framework is based on a key generalization of a widely-applied theorem for conditioning GPs on a finite number of direct observations to observations made via an arbitrary bounded linear operator. Crucially, this probabilistic viewpoint allows to (1) quantify the inherent discretization error; (2) propagate uncertainty about the model parameters to the solution; and (3) condition on noisy measurements. Demonstrating the strength of this formulation, we prove that it strictly generalizes methods of weighted residuals, a central class of PDE solvers including collocation, finite volume, pseudospectral, and (generalized) Galerkin methods such as finite element and spectral methods. This class can thus be directly equipped with a structured error estimate and the capability to incorporate uncertain model parameters and observations. In summary, our results enable the seamless integration of mechanistic models as modular building blocks into probabilistic models."

# Summary. An optional shortened abstract.
summary: ""

tags: ["probabilistic numerics", "machine learning", "numerical analysis", "gaussian processes", "partial differential equations", "linear operator equations"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
- name: arXiv
  url: https://arxiv.org/abs/2212.12474
#  - name: Proceedings
#    url:

url_pdf: https://arxiv.org/pdf/2212.12474.pdf
# url_code: https://github.com/JonathanWenger/itergp
# url_dataset:
# url_poster:
# url_project:
# url_slides: 
# url_source:
# url_video: https://youtu.be/xsXifiz2Zfo

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "A physics-informed Gaussian process framework for the solution of linear PDEs."
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
