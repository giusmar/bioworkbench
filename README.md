# bioworkbench
Repository with dockefile and docker compose for a bioinformatic workbench

## How to use

This repository aims to organize different docker container with specific verions of tools.
Every folder refers to a single tool where you can put input file and take output file.

## Installation steps

1) First step: clone the repository

```bash
git clone https://github.com/giusmar/bioworkbench.git
```

2) Move in the folder and run docker compose

```bash
cd bioworkbench; docker compose up -d
```

3) Execute a tool

```bash
docker exec fastp fastp --help
docker exec subread featuresCount --help
docker exec star STAR --version
```

4) Shut down docker container

```bash
docker compose down
```

When you need to reuse docker container, you can simply rebuild already downloaded docker images with:

```bash
cd bioworkbench; docker compose up -d
```
