---
# Documentation: https://wowchemy.com/docs/managing-content/

title: Strongly Linearizable Implementations of Snapshots and Other Types
subtitle: ''
summary: ''
authors:
- Sean Ovens
- Philipp Woelfel
tags:
- distributed algorithms
- snapshots
- shared memory
- lock-freedom
- strong linearizability
- aba
categories: []
date: '2019'
# lastmod: 2022-10-28T14:00:09-04:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
publishDate: ''
publication_types:
- '1'
abstract: Linearizability is the gold standard of correctness conditions for shared
  memory algorithms, and historically has been considered the practical equivalent
  of atomicity. However, it has been shown that replacing atomic objects with linearizable
  implementations can affect the probability distribution of execution outcomes in
  randomized algorithms. Thus, linearizable objects are not always suitable replacements
  for atomic objects. A stricter correctness condition called strong linearizability
  has been developed and shown to be appropriate for randomized algorithms in a strong
  adaptive adversary model[16].We devise several new lock-free strongly linearizable
  implementations from atomic registers. In particular, we give the first strongly
  linearizable lock-free snapshot implementation that uses bounded space. This improves
  on the unbounded space solution of Denysyuk and Woelfel[14]. As a building block,
  our algorithm uses a lock-free strongly linearizable ABA-detecting register. We
  obtain this object by modifying the wait-free linearizable ABA-detecting register
  of Aghazadeh and Woelfel [5], which, as we show, is not strongly linearizable.Aspnes
  and Herlihy[8] identified a wide class of types that have wait-free linearizable
  implementations. These types require that any pair of operations either commute,
  or one overwrites the other. Aspnes and Herlihy gave a general wait-free linearizable
  implementation of such types, employing an atomic snapshot object. We show that
  this implementation is strongly linearizable, proving that all types in this class
  have a lock-free strongly linearizable implementation from atomic registers.
publication: 'Proceedings of the 2019 ACM Symposium on Principles of Distributed
  Computing'
doi: 10.1145/3293611.3331632
links:
- name: URL
  url: https://doi.org/10.1145/3293611.3331632
---
