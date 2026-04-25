# 🚀 EKS ArgoCD GitOps Project

Provisioning an Amazon EKS cluster with Terraform and deploying applications using ArgoCD for GitOps-based continuous delivery.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Step-by-Step Walkthrough](#step-by-step-walkthrough)
- [Cleanup](#cleanup)

---

## Overview

This project demonstrates a complete GitOps workflow on AWS using:

- **Terraform** — Infrastructure as Code to provision the EKS cluster, VPC, subnets, IAM roles, and node groups
- **Amazon EKS** — Managed Kubernetes cluster running on AWS (Kubernetes v1.31)
- **ArgoCD** — GitOps continuous delivery tool that syncs Kubernetes manifests from a Git repository to the cluster
- **kubectl** — Kubernetes CLI for interacting with the cluster
- **AWS EC2** — Worker nodes running Amazon Linux 2023 (t3.medium instances)

The infrastructure consists of 25 AWS resources provisioned automatically via Terraform, including a custom VPC, public and private subnets, NAT gateways, internet gateway, route tables, IAM roles, the EKS control plane, and a managed node group.

---

## Architecture
