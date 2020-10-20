---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Probabilistic Linear Solvers for Machine Learning"
authors: ["admin", "Philipp Hennig"]
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
publication: "Advances in Neural Information Processing Systems"
publication_short: "NeurIPS"

abstract: "Linear systems are the bedrock of virtually all numerical computation. Machine learning poses specific challenges for the solution of such systems due to their scale, characteristic structure, stochasticity and the central role of uncertainty in the field. Unifying earlier work we propose a class of probabilistic linear solvers which jointly infer the matrix, its inverse and the solution from matrix-vector product observations. This class emerges from a fundamental set of desiderata which constrains the space of possible algorithms and recovers the method of conjugate gradients under certain conditions. We demonstrate how to incorporate prior spectral information in order to calibrate uncertainty and experimentally showcase the potential of such solvers for machine learning."

# Summary. An optional shortened abstract.
summary: ""

tags: ["probabilistic-numerics", "linear-algebra", "machine-learning"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
links:
 - name: Proceedings
   url: https://papers.nips.cc/

url_pdf: https://arxiv.org/pdf/2010.09691.pdf
url_code: https://github.com/JonathanWenger/probabilistic-linear-solvers-for-ml
# url_dataset:
# url_poster:
# url_project:
url_slides: probabilistic_linear_solvers_talk.pdf
# url_source:
url_video: https://www.youtube.com/watch?v=3_1JE91g_3E&list=PL05umP7R6ij0pTCyaKny5V4iBs3739f4z&index=6

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Structured kernel matrix."
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
