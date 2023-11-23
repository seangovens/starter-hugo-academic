---
# Documentation: https://wowchemy.com/docs/managing-content/

title: The Space Complexity of Scannable Binary Objects
subtitle: ''
summary: ''
authors:
- Sean Ovens
tags:
- lower bound
- shared memory
- space complexity
- snapshot object
categories: []
date: '2021-07-23'
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
abstract: "Determining a consistent view of the contents of a shared array while its\
  \ components are being modified is a fundamental task in distributed algorithm design.\
  \ Snapshot objects address this problem when read/write registers are components\
  \ of the array. A natural generalization of a snapshot object is a scannable object,\
  \ an object with multiple components that each support Read and some other operations.\
  \ Scannable objects also support the Scan operation, which provides an instantaneous\
  \ view of all the object's components. This raises the question: How many instances\
  \ of objects in some set O are required to implement a scannable object whose components\
  \ are in O In this paper, we consider scannable binary objects, whose components\
  \ are arbitrary 1-bit objects. If each component is a test-and-set object, there\
  \ is a simple implementation using k test-and-set objects. However, when each component\
  \ is non-monotonic (i.e. can change from 0 to 1 and from 1 to 0), we prove that\
  \ more objects are needed. Specifically, when n ≤ 2^k-1 + 2, we show a lower bound\
  \ of n + k - 2 base objects, even for obstruction-free, single-updater implementations.\
  \ When n ≥ 2^k-2, we prove that 2^k-1 base objects are required for obstruction-free,\
  \ single-updater implementations. When 2^k-1 +2 &lt; n &lt; 2^k-2, we show a gradual\
  \ transition between these two lower bounds. We show that there is a lock-free implementation\
  \ of an n-process, scannable binary object with k components from n + k instances\
  \ of 1-bit base objects, nearly matching our lower bound when n łeq 2^k-1 + 2. There\
  \ is a known wait-free, single-updater implementation that uses 2^k base objects,\
  \ nearly matching our lower bound when n ≥ 2^k-2."
publication: 'Proceedings of the 2021 ACM Symposium on Principles of Distributed
  Computing (PODC 2021)'
doi: 10.1145/3465084.3467916
links:
- name: URL
  url: https://doi.org/10.1145/3465084.3467916
---
