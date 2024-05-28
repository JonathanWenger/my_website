---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Computation-Aware Kalman Filtering and Smoothing"
authors: ["Marvin Pförtner", "admin", "Jon Cockayne", "Philipp Hennig"]
date: 2024-05-14T10:00:00+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2024-05-14T06:00:00+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: "arXiv preprint"
publication_short: "arXiv preprint"

abstract: "Kalman filtering and smoothing are the foundational mechanisms for efficient inference in Gauss-Markov models. However, their time and memory complexities scale prohibitively with the size of the state space. This is particularly problematic in spatiotemporal regression problems, where the state dimension scales with the number of spatial observations. Existing approximate frameworks leverage low-rank approximations of the covariance matrix. Since they do not model the error introduced by the computational approximation, their predictive uncertainty estimates can be overly optimistic. In this work, we propose a probabilistic numerical method for inference in high-dimensional Gauss-Markov models which mitigates these scaling issues. Our matrix-free iterative algorithm leverages GPU acceleration and crucially enables a tunable trade-off between computational cost and predictive uncertainty. Finally, we demonstrate the scalability of our method on a large-scale climate dataset."

# Summary. An optional shortened abstract.
summary: ""

tags: ["Kalman filter", "Rauch-Tung-Striebel smoother", "gaussian processes", "probabilistic numerics"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
- name: arXiv
  url: https://arxiv.org/abs/2405.08971
#  - name: Proceedings
#    url:

url_pdf: https://arxiv.org/pdf/2405.08971.pdf
url_code: https://github.com/marvinpfoertner/ComputationAwareKalman.jl
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
  caption: "Spatio-temporal Gaussian process regression of Earth’s surface temperature using the ERA5 dataset via computation-aware filtering and smoothing."
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
