---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "On the Disconnect Between Theory and Practice of Neural Networks: Limits of the NTK Perspective"
authors: ["admin", "Felix Dangel", "Agustinus Kristiadi"]
date: 2023-09-01T10:00:00+02:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2023-09-01T06:00:00+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["3"]

# Publication name and optional abbreviated publication name.
publication: "arXiv preprint"
publication_short: "arXiv preprint"

abstract: "The neural tangent kernel (NTK) has garnered significant attention as a theoretical framework for describing the behavior of large-scale neural networks. Kernel methods are theoretically well-understood and as a result enjoy algorithmic benefits, which can be demonstrated to hold in wide synthetic neural network architectures. These advantages include faster optimization, reliable uncertainty quantification and improved continual learning. However, current results quantifying the rate of convergence to the kernel regime suggest that exploiting these benefits requires architectures that are orders of magnitude wider than they are deep. This assumption raises concerns that architectures used in practice do not exhibit behaviors as predicted by the NTK. Here, we supplement previous work on the NTK by empirically investigating whether the limiting regime predicts practically relevant behavior of large-width architectures. Our results demonstrate that this is not the case across multiple domains. This observed disconnect between theory and practice further calls into question to what degree NTK theory should inform architectural and algorithmic choices."

# Summary. An optional shortened abstract.
summary: ""

tags: ["neural tangent kernel", "neural networks", "deep learning", "continual learning", "gaussian processes"]
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
  caption: "Infinitely-wide neural networks in theory and their finite-width approximations in practice learn significantly different functions."
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
