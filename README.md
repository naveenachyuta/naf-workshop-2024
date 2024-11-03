# Network Monitoring for Beginners: Getting Started with TPG stack Workshop

This repository contains the necessary files and instructions that will used for NAF (network automation forum) 2024 workshop on collecting metrics from network devices using the Telegraf, Prometheus, and Grafana (TPG) stack.

## Overview

Learn how to collect, store, and visualize network metrics using:
- Telegraf: Data collection agent
- Prometheus: Time series database and monitoring system
- Grafana: Visualization and analytics platform

## Workshop Demo

### 1. Click on "Create Codespaces on main" to launch a development environment

### 2. Network Simulation Setup

We use ContainerLab to simulate the network environment.

```bash
# Deploy the network topology
sudo containerlab deploy -t clab.yaml
```

### 3. TPG Stack Deployment

Deploy the monitoring stack using Docker Compose:

```bash
# Start the TPG stack
docker compose -f docker-compose-sample.yaml up
```

### 3. Port Configuration

To access the various UIs, configure the following ports in VS Code's ports section:

| Service | Port | Description |
|---------|------|-------------|
| Prometheus | 9090 | Metrics storage and querying |
| Alert Manager | 9093 | Alerting interface |
| Grafana | 3000 | Visualization dashboard |
