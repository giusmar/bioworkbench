# bioworkbench
Repository with Dockerfiles and Docker Compose for a bioinformatics workbench.

## Overview
This repository organizes various Docker containers with specific versions of bioinformatics tools.
Each folder corresponds to a single tool, where you can place input files and retrieve output files.

## Usage Guide

### 1. Clone the repository

```bash
git clone https://github.com/giusmar/bioworkbench.git
```

### 2. Navigate to the folder and start the containers

```bash
cd bioworkbench
docker compose up -d
```

### 3. Execute a tool

```bash
docker exec fastp fastp --help
docker exec subread featuresCount --help
docker exec star STAR --version
```

### 4. Shut down the containers

```bash
docker compose down
```

### 5. Restart previously built containers

When you need to reuse docker container, you can simply rebuild already downloaded docker images with:

```bash
cd bioworkbench
docker compose up -d
```
