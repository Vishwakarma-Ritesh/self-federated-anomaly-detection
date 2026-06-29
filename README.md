# Self-Federated Anomaly Detection

This repository contains materials related to the Self-Federated Anomaly Detection (SFAD) project, including a visual diagram and the accompanying research paper.

## Contents<img width="1536" height="1024" alt="diagram" src="https://github.com/user-attachments/assets/5403ab26-6c27-42a2-86a6-afeef778d20c" />


- [diagram.png](diagram.png) — architecture / workflow diagram for the system
- [Research paper SFAD system.pdf](Research%20paper%20SFAD%20system.pdf) — reference paper for the project

# Self Federated Anomaly Detection System for Cloud Infrastructure (SFAD)

<p align="center">
  <b>Open Contribution • Cloud Infrastructure Mentorship • Security Architecture Guidance</b>
</p>

<p align="center">
A community contribution where I mentored final-year engineering students from D. Y. Patil / RAIT in building a production-style cloud-native anomaly detection system.
</p>

---

## Table of Contents

* Project Overview
* Problem Statement
* Key Features
* Architecture
* Components
* Tech Stack
* My Contribution
* Project Outcome
* Key Learnings

---

# Project Overview

Modern cloud infrastructures generate massive telemetry data from distributed workloads such as:

* Virtual Machines
* Containers
* Servers
* Applications
* Network Systems

This telemetry includes:

* CPU usage
* Memory usage
* Disk I/O
* Network traffic
* Application logs

Monitoring such large-scale infrastructure manually becomes difficult and inefficient.

The **Self Federated Anomaly Detection System for Cloud Infrastructure (SFAD)** is an intelligent cloud-native platform designed to:

* Detect infrastructure anomalies in real time
* Identify root causes
* Trigger automated remediation
* Improve infrastructure security
* Enable observability and monitoring

This system combines **Machine Learning, Security Engineering, Cloud Infrastructure, and DevOps practices** to create a self-healing infrastructure model.

---

# Problem Statement

Traditional monitoring systems mostly rely on static threshold alerts.

Example:

* CPU > 90% → Alert
* Memory > 85% → Alert

Problems with traditional systems:

* High false positives
* Unknown attack patterns remain undetected
* Manual incident response
* Slow Mean Time to Detection (MTTD)
* Poor root cause visibility

The objective of SFAD was to build a platform capable of:

✅ Real-time anomaly detection
✅ Automated recovery actions
✅ Secure isolation of compromised nodes
✅ Scalable cloud deployment
✅ Improved security posture

---

# Key Features

## 1. Hybrid ML-Based Detection

The system combines two anomaly detection models:

### Isolation Forest

Used for infrastructure anomaly detection:

* CPU spikes
* Memory leakage
* Disk saturation
* Network anomalies

### Autoencoder Neural Network

Used for behavioral anomaly detection from:

* Logs
* Error patterns
* Hidden abnormal activity

Both outputs are combined using **decision fusion** for better accuracy.

---

## 2. Federated Learning

Instead of centralized training, SFAD uses **Federated Learning**.

Benefits:

* Better privacy
* No raw telemetry sharing
* Distributed model updates
* Improved scalability

---

## 3. Zero Trust Security (Cyber Jail)

Security follows:

> Never Trust, Always Verify

Suspicious workloads are:

* Detected
* Validated
* Isolated
* Quarantined

This isolation mechanism is called **Cyber Jail**.

Example flow:

Threat Detected → Security Validation → Quarantine → Block Access

---

## 4. Automated Remediation

After anomaly detection, the system can automatically perform recovery actions.

Examples:

### Memory Leak

* Restart service

### DDoS Attack

* Reroute traffic
* Scale load balancer

### CPU Starvation

* Throttle low-priority workloads

This enables **self-healing infrastructure behavior**.

---

## 5. Observability Dashboard

Dashboard provides:

* Live metrics
* Alerts
* Incident reports
* Root cause visibility
* Threat analysis

This improves production monitoring and operational visibility.

---

# Architecture

```text
Cloud Infrastructure Layer
(VMs / Containers / Servers / Applications)
                    │
                    ▼
Edge Client Layer
(CPU, Memory, Disk, Network, Logs Collection)
                    │
                    ▼
Inference Engine Layer
(Isolation Forest + Autoencoder + RCA)
                    │
                    ▼
Security Layer
(Zero Trust + Threat Analysis + Cyber Jail)
                    │
                    ▼
Automated Remediation Layer
(Restart / Scale / Block / Reroute)
                    │
                    ▼
Observability Dashboard
(Metrics / Logs / Alerts / Reports)
```

---

# Components

## 1. Cloud Infrastructure Layer

This is the source of telemetry.

Resources include:

* Virtual machines
* Containers
* Servers
* Applications

These continuously generate operational data.

---

## 2. Edge Client Layer

Collectors gather:

* CPU usage
* Memory usage
* Disk I/O
* Network traffic
* Logs

This telemetry is forwarded to the inference engine.

---

## 3. Inference Engine Layer

This is the intelligence layer.

Responsibilities:

* Process telemetry
* Detect anomalies
* Perform analysis
* Generate predictions
* Trigger alerts

---

## 4. Security Layer

Implements:

* Zero Trust validation
* Threat analysis
* Access control
* Node isolation

Compromised workloads are quarantined using **Cyber Jail**.

---

## 5. Automated Remediation Layer

Makes the infrastructure self-healing.

Actions include:

* Restart service
* Scale resources
* Block access
* Reroute traffic

---

## 6. Observability Dashboard

Used by engineers to monitor:

* Alerts
* Metrics
* Incidents
* Root cause reports

---

# Tech Stack

## Backend

* Python
* FastAPI

## Machine Learning

* Isolation Forest
* Autoencoder
* Federated Learning

## Security

* Zero Trust Architecture
* Cyber Jail
* Threat Isolation

## Observability

* Streamlit
* Plotly

## Cloud Concepts

* Telemetry Pipelines
* Distributed Systems
* Monitoring
* Reliability Engineering

---

# My Contribution

I contributed to this project as a **Cloud Infrastructure & DevOps Mentor**.

My role was to help students bridge the gap between academic implementation and real-world production engineering.

## 1. Cloud Infrastructure Architecture

Guided students in designing scalable cloud architecture.

Covered:

* Layered architecture
* Distributed systems
* Scalability planning
* Production design patterns

---

## 2. Security Architecture Guidance

Mentored them on:

* Zero Trust Security
* Threat isolation
* Secure communication
* Access control design

This directly influenced the **Cyber Jail** implementation.

---

## 3. DevOps & Deployment Best Practices

Introduced production deployment concepts:

* CI/CD pipelines
* Containerized workloads
* Infrastructure automation
* Release strategy
* Rollback planning

---

## 4. Observability & Monitoring

Taught production-grade monitoring concepts:

* Telemetry collection
* Dashboards
* Alerts
* Incident visibility
* Root cause analysis

---

## 5. Industry-Level Engineering Thinking

Helped students think like engineers solving real infrastructure problems.

Mentored them on:

* Scalability tradeoffs
* Reliability engineering
* Fault isolation
* Production readiness

---

# Project Outcome

This contribution helped students:

* Understand cloud infrastructure
* Learn security-first architecture
* Connect research with industry
* Build a production-oriented system

Key achievements:

* ~94% anomaly detection accuracy
* Reduced detection time to seconds
* Automated remediation workflow
* Improved security posture

---

# Key Learnings

This project demonstrated how **AI + Cloud Infrastructure + Security + DevOps** can work together to build intelligent, self-healing systems.

It also reinforced the importance of:

* Production thinking
* Security-first design
* Observability
* Infrastructure reliability

---

# Personal Note

As a DevOps Engineer, I strongly believe in contributing to student and community projects that bridge the gap between **academic learning and real-world engineering practices**.

Helping students understand **cloud infrastructure, security, DevOps, and production architecture** at a practical level is something I genuinely value.
