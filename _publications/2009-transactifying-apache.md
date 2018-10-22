---
title: "Transactifying Apache's Cache Module"
collection: publications
permalink: /publications/2009-transactifying-apache
excerpt: ''
date: 2009-05-04
venue: "SYSTOR '09, Proceedings of SYSTOR 2009: The Israeli Experimental Systems Conference"
paperurl: 'https://dl.acm.org/authorize?N661716'
#citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
authors: Haggai Eran, Ohad Lutzky, Zvika Guz, Idit Keidar
---

Apache is a large-scale industrial multi-process and multithreaded application,
which uses lock-based synchronization. We report on our experience in modifying
Apache's cache module to employ transactional memory instead of locks, a
process we refer to as transactification; we are not aware of any previous
efforts to transactify legacy software of such a large scale. Along the way, we
learned some valuable lessons about which tools one should use, which parts of
the code one should transactify and which are better left untouched, as well as
on the intricacy of commit handlers. We also stumbled across weaknesses of
existing software transactional memory (STM) toolkits, leading us to identify
desirable features they are currently lacking. Finally, we present performance
results from running Apache on a 32-core machine, showing that, there are
scenarios where the performance of the STM-based version is close to that of
the lock-based version. These results suggest that there are applications for
which the overhead of using a software-only implementation of transactional
memory is insignificant.
