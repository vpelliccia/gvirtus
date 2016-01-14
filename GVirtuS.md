## Abstract ##

The challenge for exascale computing is enforced by the many core technology involving general purpose CPUs and specialized devices as GPUs.

This kind of accelerators, due to their wide market footprint, have currently achieved one of the best core/cost rate even taking into account power consumption and heat dissipation.

The dominating resource sharing platforms based on computing grids, are migrating to Cloud computing based infrastructures. With an easy interface, high-level services, and on-demand provision of computing resources, compute Clouds are attracting more users to join their realm.

This document describes the generic virtualization service GVirtuS (Generic Virtualization Service), implemented as a framework for split-driver abstraction components development.

In order to provide tools for elastic-science leveraging on high performance private and public computing clouds commodities, we focused our attention on GPU virtualization, but not limiting GVirtuS to this kind of applications.


## Introduction ##

Scientific computing has experienced on general-purpose graphics processing units using massive multi core processors available on graphics devices for texture processing in order to accelerate data parallel computing tasks.

From a data flow point of view, data are processed in a parallel way on GPUs and the instruction set kernel operating on those data are sent to the accelerating hardware, processed on the device and then sent back to the general purpose CPU.

One the most successful GPU based system is provided by nVIDIA and relies on the CUDA programming paradigm supporting high level languages tools.

An active research field is currently focused on suitably exploiting special purpose processors as accelerators for general-purpose scientific computations.

Actually, multicore processor is not only a solution for CPU speed but also reduces the power consumption because several cores in a lower frequency together generate less heat dissipation than one core with their total frequency.

The increasing number of CPUs cores on chip has driven the development and spreading of the cloud computing, leveraging on consolidated technologies such as, but not limited to, grid computing and virtualization.

In recent years the use of grid computing in high performance demanding applications in e-science has become a common issue. Cloud environments are primarily built on top of multicore technologies. However, to fully exploit the computational capacity and the other advantages of multicores, a lot of novel techniques must be proposed and investigated. Elastic computer power and storage provided by a cloud infrastructure are attractive for high performance scientific and engineering computing, but is still limited by poor communication performance and lack of support in using GPUs within a virtual machine instance.

Cloud computing offers an appealing elastic infrastructure, but whether and how it can provide the effective high performances required by most e-science applications is still a research issue.

Especially in the field of parallel computing applications, virtual clusters instanced on cloud infrastructures suffers from the poorness of message passing performances between virtual machine instances running on the same real machine and also from the impossibility to access hardware specific accelerating devices as GPUs.