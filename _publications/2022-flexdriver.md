---
title: "FlexDriver: A Network Driver for Your Accelerator"
collection: publications
permalink: /publications/2022-flexdriver
excerpt: ''
date: 2022-03-04
venue: "ASPLOS '22: ACM International Conference on Architectural Support for Languages and Operating Systems"
preprint: '/files/flexdriver-preprint-asplos22.pdf'
paperurl: 'https://dl.acm.org/doi/10.1145/3503222.3507776'
slides: '/files/flexdriver-asplos22-slides.pdf'
authors: Haggai Eran, Maxim Fudim, Gabi Malka, Gal Shalom, Noam Cohen, Amit Hermony, Dotan Levi, Liran Liss, Mark Siblerstein
youtube:
  talk: 2WPFvEMvjzg
awards: IEEE MICRO Top Picks 2023 honorable mention
---

We propose a new system design for connecting hardware and
FPGA accelerators to the network, allowing the accelerator to directly
control commodity Network Interface Cards (NICs) without
using the CPU. This enables us to solve the key challenge of leveraging
existing NIC hardware offloads such as virtualization, tunneling,
and RDMA for accelerator networking. Our approach supports a
diverse set of use cases, from direct network access for disaggregated
accelerators to inline-acceleration of the network stack, all
without the complex networking logic in the accelerator.

To demonstrate the feasibility of this approach, we build **FlexDriver (FLD)**,
an on-accelerator hardware module that implements
a NIC data-plane driver. Our main technical contribution is a mechanism
that compresses the NIC control structures by two orders
of magnitude, allowing FLD to achieve high networking scalability
with low die area cost and no bandwidth interference with the
accelerator logic.

The prototype for NVIDIA Innova-2 FPGA SmartNICs showcases
our design’s utility for three different accelerators: a disaggregated
LTE cipher, an IP-defragmentation inline accelerator, and an IoT
cryptographic-token authentication offload. These accelerators
reach 25 Gbps line rate and leverage the NIC for RDMA processing,
VXLAN tunneling, and traffic shaping without CPU involvement.