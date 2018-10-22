---
title: "Flow-based tunneling for SR-IOV using switchdev API"
collection: publications
permalink: /publications/2016-open-vswitch-acceleration
excerpt: ''
date: 2016-02-10
venue: "netdev 1.1, Proceedings of NetDev 1.1: The Technical Conference on Linux Networking"
paperurl: 'https://www.netdevconf.org/1.1/proceedings/papers/Flow-based-tunneling-for-SR-IOV-using-switchdev-API.pdf'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
authors: Ilya Lesokhin, Haggai Eran, Or Gerlitz
---

SR-IOV devices present improved performance for network virtualization, but
pose limitations today on the ability of the hypervisor to manage the network.
For instance, UDP and IP tunnels that are commonly used on the cloud are not
supported today with SR-IOV. Flow based approaches like Open vSwitch and TC are
common in managing virtual machine traffic. Both technologies are not supported
with today’s SR-IOV Linux driver model, which only allows to program MAC or MAC+VLAN 
based forwarding for virtual function traffic. We present a design that
facilitates SR-IOV performance while maintaining flow-based management for both
non-tunneled and VXLAN tunneled flows and uses the switchdev framework to
program the SR-IOV eSwitch. Our prototype uses hardware offloads for most
traffic, and a software fallback for traffic we cannot offload. We expose a
representor netdev for each port in the SR-IOV eSwitch, one per virtual
function and another for the uplink, to enable the management of these ports by
the kernel and also the send and receive packets through the software fallback
path. Our implementation currently uses openvswitch for managing flows. It
should be possible to extend it to other management schemes such as TC. A
flow’s match and actions are reflected to the underlying device using extended
switchdev APIs. For tunneling we also propagate information about the tunnel
FDB, and the kernel routing table and neighbor table.
