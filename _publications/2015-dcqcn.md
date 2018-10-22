---
title: "Congestion Control for Large-Scale RDMA Deployments"
collection: publications
permalink: /publications/2015-dcqcn
excerpt: ''
date: 2015-08-17
venue: "SIGCOMM '15, Proceedings of the 2015 ACM Conference on Special Interest Group on Data Communication"
paperurl: 'https://dl.acm.org/authorize?N661704'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
authors: Yibo Zhu, Haggai Eran, Daniel Firestone, Chuanxiong Guo, Marina Lipshteyn, Yehonatan Liron, Jitendra Padhye, Shachar Raindel, Mohamad Haj Yahia, Ming Zhang
---

Modern datacenter applications demand high throughput (40Gbps) and ultra-low
latency (< 10 μs per hop) from the network, with low CPU overhead. Standard
TCP/IP stacks cannot meet these requirements, but Remote Direct Memory Access
(RDMA) can. On IP-routed datacenter networks, RDMA is deployed using RoCEv2
protocol, which relies on Priority-based Flow Control (PFC) to enable a
drop-free network. However, PFC can lead to poor application performance due to
problems like head-of-line blocking and unfairness. To alleviates these
problems, we introduce DCQCN, an end-to-end congestion control scheme for
RoCEv2. To optimize DCQCN performance, we build a fluid model, and provide
guidelines for tuning switch buffer thresholds, and other protocol parameters.
Using a 3-tier Clos network testbed, we show that DCQCN dramatically improves
throughput and fairness of RoCEv2 RDMA traffic. DCQCN is implemented in
Mellanox NICs, and is being deployed in Microsoft's datacenters.
