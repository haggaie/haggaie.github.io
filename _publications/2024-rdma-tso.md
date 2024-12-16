---
title: "Semantics of Remote Direct Memory Access: Operational and Declarative Models of RDMA on TSO Architectures"
collection: publications
permalink: /publications/2024-rdma-tso
excerpt: ''
date: 2024-10-08
venue: "OOPSLA 2024, Proc. ACM Program. Lang. 8, OOPSLA2"
paperurl: 'https://dl.acm.org/doi/10.1145/3689781'
authors: Guillaume Ambal, Brijesh Dongol, Haggai Eran, Vasileios Klimis, Ori Lahav, Azalea Raad
youtube:
  talk:
    id: qnL958srgjA
    start: 24390
---

Remote direct memory access (RDMA) is a modern technology enabling networked machines to exchange information without involving the operating system of either side, and thus significantly speeding up data transfer in computer clusters. While RDMA is extensively used in practice and studied in various research papers, a formal underlying model specifying the allowed behaviours of concurrent RDMA programs running in modern multicore architectures is still missing. This paper aims to close this gap and provide semantic foundations of RDMA on x86-TSO machines. We propose three equivalent formal models, two operational models in different levels of abstraction and one declarative model, and prove that the three characterisations are equivalent. To gain confidence in the proposed semantics, the more concrete operational model has been reviewed by NVIDIA experts, a major vendor of RDMA systems, and we have empirically validated the declarative formalisation on various subtle litmus tests by extensive testing. We believe that this work is a necessary initial step for formally addressing RDMA-based systems by proposing language-level models, verifying their mapping to hardware, and developing reasoning techniques for concurrent RDMA programs.

You may find more details about the project, including the [extended version](https://www.soundandcomplete.org/papers/OOPSLA2024/RDMA/rdma-extended.pdf) of the paper and its artifacts [here](https://www.soundandcomplete.org/papers/OOPSLA2024/RDMA/).