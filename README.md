# Work In Progress

> **This document is a draft, as we are testing the code/infra on distributed inference/training. Feel free to pull the containers through. Stay tuned for updates**
# Simplified Deployment of Private AI Infrastructure with x86 Compute, Kubernetes, and NVIDIA GPUs

This repository provides a streamlined solution for deploying large-scale private AI infrastructure using x86 architecture, Kubernetes, and NVIDIA GPUs. It is designed for developers, researchers, and organizations looking to efficiently set up and manage AI infrastructure on Nvidia GPUs and Ethernet/RoCE Fabric. 

## Key Features
- **Simple Installation**: Easy-to-use installation scripts to consolidate the OS, networking, and software stack for seamless deployment.
- **Distributed Training or Distributed Inference**: Can run both Training/Inference ML/AI/LLM workloads on the  ecosystem.
- **Performance Test Tools/Custom Containers**: Perform basic performance tests on the compute and networking fabric.
- **Kubernetes Integration**: Leverage Kubernetes for scalable orchestration of AI workloads across multiple nodes.
- **NVIDIA GPU Support**: Optimized for hardware acceleration with NVIDIA GPUs, enhancing performance for AI/ML models.
- **x86 Compute**: Fully compatible with x86 architecture, offering flexibility in hardware choices.
- **Scalability**: Easily scale AI workloads based on demand, without compromising performance or resource management.
- **Customizable**: Modular setup to tailor deployment to specific AI project needs.
- **Private**: All data stays on-prem, with no reliance on cloud services.

## Core Components
- x86/64 with Ubuntu
- NVIDIA GPUs
- Container Ecosystem
- Kubernetes
- NVIDIA GPU Operator
- NVIDIA Network Operator
- Calico
- Kubespray
- NFS for storage
- Mellanox RDMA-capable NICs
- GPUDirect RDMA
- NCCL
- RoCEv2
- MPI
- LWS
- IBPerf
- NCCL Tests
- Low-level monitoring with Intel PCM

## Work in Progress
- Network QoS template for lossless Ethernet

Whether you're running machine learning, deep learning, or other AI applications, this repo simplifies the process of setting up powerful private AI infrastructure.
