---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "On the Disconnect Between Theory and Practice of Overparametrized Neural Networks"
authors: ["admin", "Felix Dangel", "Agustinus Kristiadi"]
date: 2023-20-01T10:00:00+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2022-06-01T06:00:00+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: "arXiv preprint"
publication_short: "arXiv preprint"

abstract: "The infinite-width limit of neural networks (NNs) has garnered significant attention as a theoretical framework for analyzing the behavior of large-scale, overparametrized networks. By approaching infinite width, NNs effectively converge to a linear model with features characterized by the neural tangent kernel (NTK). This establishes a connection between NNs and kernel methods, the latter of which are well understood. Based on this link, theoretical benefits and algorithmic improvements have been hypothesized and empirically demonstrated in synthetic architectures. These advantages include faster optimization, reliable uncertainty quantification and improved continual learning. However, current results quantifying the rate of convergence to the kernel regime suggest that exploiting these benefits requires architectures that are orders of magnitude wider than they are deep. This assumption raises concerns that practically relevant architectures do not exhibit behavior as predicted via the NTK. In this work, we empirically investigate whether the limiting regime either describes the behavior of large-width architectures used in practice or is informative for algorithmic improvements. Our empirical results demonstrate that this is not the case in optimization, uncertainty quantification or continual learning. This observed disconnect between theory and practice calls into question the practical relevance of the infinite-width limit. "

# Summary. An optional shortened abstract.
summary: ""

tags: ["neural tangent kernel", "neural networks", "gaussian processes"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
- name: arXiv
  url: https://arxiv.org/abs/2310.00137
#  - name: Proceedings
#    url:

url_pdf: https://arxiv.org/pdf/2310.00137.pdf
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
  caption: "Infinitely-wide neural networks in theory and their finite-width approximations in practice make learn significantly different functions."
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
