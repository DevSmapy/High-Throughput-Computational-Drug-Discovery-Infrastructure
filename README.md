# High-Throughput Data Platform for Computational Drug Discovery

> Designed and optimized a large-scale molecular data platform that processed over **100 million molecular records**, automated **HPC-based scientific workflows**, and improved the scalability and reliability of virtual screening pipelines.

**Company**
Syntekabio (2019.03 – 2022.02)

**Role**
Data Engineer

**Research Domain**
Computational Drug Discovery

**Focus Areas**
Large-scale Data Processing · Pipeline Automation · HPC · Database Optimization · Scientific Computing

|                    |                                                     |
| ------------------ | --------------------------------------------------- |
| **Category**       | **Summary**                                         |
| Role               | Data Engineer                                       |
| Domain             | Computational Drug Discovery                        |
| Scale              | 100M+ Molecular Records                             |
| Infrastructure     | HPC Cluster (200+ Nodes)                            |
| Core Contributions | Data Pipeline · Search Engine · Workflow Automation |
| Key Technologies   | Python · PostgreSQL · Linux · RDKit                 |

## Executive Summary

As a Data Engineer on an AI-driven drug discovery team, I built and optimized data-intensive research infrastructure for large-scale virtual screening.

Rather than focusing solely on computational chemistry, my work centered on solving core engineering problems involving massive datasets, distributed computing, and workflow automation.

Key contributions include:

- Designed scalable pipelines capable of processing over **100 million molecular records**
- Developed a custom molecular search engine (IDSCAN V3) to improve search reliability and data integrity
- Automated molecular dynamics (MD) workflows across **200+ HPC nodes**
- Optimized multiprocessing pipelines to significantly reduce large-scale search execution time
- Built robust validation and data quality processes for molecular databases

## Business Context

Virtual screening is a foundational process in computational drug discovery, requiring researchers to search and analyze extremely large molecular databases.

At Syntekabio, the platform managed over **100 million molecular records** gathered from public chemical repositories and internal datasets.

As data volume continued to grow, the legacy workflow encountered several engineering bottlenecks:

- Memory constraints during large-scale data processing
- Suboptimal search performance for scaffold-based molecular retrieval
- Data consistency issues driven by duplicated and structurally similar compounds
- Escalating computational costs for HPC-based molecular simulations

These limitations restricted research throughput and hindered the efficient execution of large-scale computational experiments.

The objective of this project was to rearchitect the data processing pipeline and automate the computational workflow while preserving data integrity and scaling seamlessly.

---
## Engineering Challenges

The platform needed to process massive molecular datasets while maintaining search accuracy and computational efficiency.

As the system scaled, several distinct engineering challenges emerged:

### 1. Large-Scale Data Processing

- Over **100 million molecular records** routinely exceeded available memory capacity.
- Processing the entire dataset sequentially led to prohibitive execution times.
- The pipeline required scalable, distributed processing without sacrificing reproducibility.

### 2. Search Reliability and Data Integrity

- Molecular databases contained duplicated structures, inconsistent identifiers, and structurally similar compounds.
- Traditional string-based comparisons proved insufficient for verifying chemical identity.
- Reliable search results demanded structural validation that went beyond standard database indexing.

### 3. HPC Workflow Management

- Molecular docking and MD simulations generated thousands of independent computational jobs.
- Efficient scheduling and orchestration were essential across **200+ HPC nodes**.
- Manual execution introduced unnecessary operational overhead and a higher rate of job failures.

---
## Architecture

The platform was structured as a scalable data processing pipeline that integrated molecular databases, parallel search engines, HPC infrastructure, and automated post-processing workflows.

The architecture cleanly separated data ingestion, molecular search, distributed computation, and result aggregation into distinct stages, enabling the efficient handling of massive datasets while maintaining data quality and reproducibility.

![[ChatGPT Image 2026년 7월 21일 오후 06_37_04.png]]

> (Architecture Diagram)

### Architecture Highlights

- Processed over **100 million molecular records** reliably
- Parallelized large-scale searches using Python multiprocessing
- Integrated PostgreSQL for structured molecular storage and querying
- Automated HPC-based molecular simulation workflows end-to-end
- Standardized post-processing and validation pipelines

---
## Engineering Decisions

### Chunk-based Processing

Instead of loading the entire molecular database into memory, the pipeline partitioned datasets into manageable chunks of approximately **1,000 records**.

This strategy minimized memory footprints while enabling efficient multiprocessing across independent workloads.

### Multiprocessing for CPU-Intensive Searches

Large-scale scaffold searching proved to be CPU-bound rather than I/O-bound.

Python multiprocessing was implemented to maximize CPU utilization and dramatically improve throughput for structural comparisons.

### Custom Molecular Search Engine

A custom search engine was developed to enhance scaffold retrieval accuracy and eliminate missing search results.

Structural ranking and validation logic were embedded directly into the engine to ensure higher reliability than conventional database queries.

### Multi-Stage Data Validation

Chemical structures were validated against multiple criteria, including structural similarity and molecular property constraints.

This validation pipeline successfully minimized duplicate records and improved overall database consistency prior to downstream analysis.

### Automated HPC Workflows

Computational tasks were automated via robust Python-based workflow scripts.

Simulation execution, post-processing, and result aggregation were made fully reproducible without manual intervention, facilitating large-scale runs across HPC clusters.

---
## Technical Impact

The redesigned platform substantially improved the scalability, maintainability, and reliability of large-scale computational workflows.

### Performance

- Handled datasets comprising over **100 million molecular records**
- Accelerated execution times for large-scale search workflows via multiprocessing
- Enabled seamless, large-scale execution of HPC-based molecular simulations

### Reliability

- Enhanced molecular search consistency through strict structural validation
- Filtered out duplicate and inconsistent molecular records prior to downstream processing
- Standardized computational workflows to guarantee scientific reproducibility

### Engineering

- Increased overall pipeline modularity to accommodate future feature expansion
- Minimized manual operational effort through end-to-end workflow automation
- Established reusable components for large-scale scientific data processing

---
## Key Learnings

This project reinforced several engineering principles that continue to influence how I design data-intensive systems.

### Engineering is About Trade-Offs

Optimizing performance is rarely just about choosing the fastest algorithm. Understanding system bottlenecks, balancing memory consumption, and designing for modular scalability proved to be far more critical.

### Data Quality is System Design

Reliable downstream analysis relies entirely on trustworthy upstream data. Validation and consistency checks must be treated as core engineering responsibilities rather than optional preprocessing steps.

### Automation Drives Reproducibility

Scientific workflows should be fully executable without manual intervention. Automation not only cuts operational overhead but also ensures consistency across repeated computational experiments.

### Scalability Must Be Engineered Early

As datasets expand, architectures built for thousands of records quickly bottleneck at millions. Designing with scalability in mind from day one prevents severe technical debt later on.

---
## Tech Stack

### Data Engineering

- Python
- PostgreSQL
- SQLite
- Multiprocessing

### Infrastructure

- Linux
- HPC Cluster
- Bash

### Scientific Computing

- RDKit
- Open Babel
- AMBER
- GROMACS

### Data Processing

- Pandas
- NumPy

### Development

- Git
- Jupyter Notebook
- VS Code

---
## Conclusion

This project demonstrates my experience to design and implement scalable data platforms for advanced computational research. Although the application domain was AI-driven drug discovery, the engineering challenges—large-scale data processing, workflow automation, HPC utilization, and data quality management—translate directly to modern Data Engineering and Platform Engineering roles.

This experience reinforced my ability to build robust, maintainable, and scalable systems that support data-intensive applications well beyond the life sciences sector.

### Reference

- [LS-align (Bioinformatics)](https://academic.oup.com/bioinformatics/article/34/13/2209/4931393 "null")
- [Murcko Scaffolds (RDKit Documentation)](https://www.rdkit.org/docs/GettingStartedInPython.html%23murcko-decomposition "null")
- [Syntekabio Technology](https://www.syntekabio.com/ "null")