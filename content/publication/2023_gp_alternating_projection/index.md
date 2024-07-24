---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Large-Scale Gaussian Processes via Alternating Projection"
authors: ["Kaiwen Wu", "admin", "Haydn Jones", "Geoff Pleiss", "Jacob R. Gardner"]
date: 2024-05-02T10:00:00+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2023-10-26T06:00:00+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "International Conference on Artificial Intelligence and Statistics (AISTATS)"
publication_short: "AISTATS"

abstract: "Gaussian process (GP) hyperparameter optimization requires repeatedly solving linear systems with n×n kernel matrices. To address the prohibitive O(n^3) time complexity, recent work has employed fast iterative numerical methods, like conjugate gradients (CG). However, as datasets increase in magnitude, the corresponding kernel matrices become increasingly ill-conditioned and still require O(n^2) space without partitioning. Thus, while CG increases the size of datasets GPs can be trained on, modern datasets reach scales beyond its applicability. In this work, we propose an iterative method which only accesses subblocks of the kernel matrix, effectively enabling mini-batching. Our algorithm, based on alternating projection, has O(n) per-iteration time and space complexity, solving many of the practical challenges of scaling GPs to very large datasets. Theoretically, we prove our method enjoys linear convergence and empirically we demonstrate its robustness to ill-conditioning. On large-scale benchmark datasets up to four million datapoints our approach accelerates training by a factor of 2× to 27× compared to CG."

# Summary. An optional shortened abstract.
summary: ""

tags: ["hyperparameter optimization", "alternating projection", "gaussian processes"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
- name: arXiv
  url: https://arxiv.org/abs/2310.17137
#  - name: Proceedings
#    url:

url_pdf: https://arxiv.org/pdf/2310.17137.pdf
# url_code: 
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
  caption: "Illustration of alternating projection onto the subspace spanned by the kernel functions centered at the first two datapoints."
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
