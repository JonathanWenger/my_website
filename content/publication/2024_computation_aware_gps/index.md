---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Computation-Aware Gaussian Processes: Model Selection And Linear-Time Inference"
authors: ["admin", "admin", "Kaiwen Wu", "Philipp Hennig", "Jacob R. Gardner", "Geoff Pleiss", "John P. Cunningham"]
date: 2024-12-9T10:00:00+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2024-11-01T06:00:00+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "Advances in Neural Information Processing Systems"
publication_short: "NeurIPS"

abstract: "Model selection in Gaussian processes scales prohibitively with the size of
the training dataset, both in time and memory. While many approximations exist,
all incur inevitable approximation error. Recent work accounts for this error
in the form of computational uncertainty, which enables -- at the cost of
quadratic complexity -- an explicit tradeoff between computation and precision.
Here we extend this development to model selection, which requires significant
enhancements to the existing approach, including linear-time scaling in the
size of the dataset. We propose a novel training loss for hyperparameter
optimization and demonstrate empirically that the resulting method can
outperform SGPR, CGGP and SVGP, state-of-the-art methods for GP model
selection, on medium to large-scale datasets. Our experiments show that model
selection for computation-aware GPs trained on 1.8 million data points can be
done within a few hours on a single GPU. As a result of this work, Gaussian
processes can be trained on large-scale datasets without significantly
compromising their ability to quantify uncertainty -- a fundamental
prerequisite for optimal decision-making."

# Summary. An optional shortened abstract.
summary: ""

tags: ["Gaussian processes", "Variational Inference", "Probabilistic Numerics", "Numerical Analysis"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
- name: arXiv
  url: https://arxiv.org/abs/2411.01036
#  - name: Proceedings
#    url:

url_pdf: https://arxiv.org/pdf/2411.01036.pdf
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
  caption: "Computation-aware Gaussian process posterior with learned sparse actions after training."
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
