# ITSA 5501 – DevOps and System Integration Project (Milestone 1)

## Project Overview
This repository demonstrates foundational DevOps and system integration practices using Git and GitHub. The project focuses on organizing infrastructure-related files, implementing version control, using branching strategies, resolving merge conflicts, simulating pull requests, and tagging milestone completion to reflect a real-world collaborative workflow.

---

## Repository Structure
ITSA-5501-Project/
├── docker/        # Dockerfiles and container-related configuration
│   └── Dockerfile
├── k8s/           # Kubernetes YAML manifests
│   └── deployment.yaml
├── iac/           # Infrastructure as Code scripts
│   └── main.tf
├── .gitignore     # Files and folders excluded from version control
└── README.md      # Project documentation
---

## Git Workflow

### Branching Strategy
- **main**: Primary branch containing stable and production-ready code
- **experiment**: Feature branch used for testing and experimental changes

### Workflow Steps
1. Initialize a local Git repository and connect it to GitHub
2. Create an `experiment` branch for isolated development
3. Commit changes frequently with descriptive messages
4. Make parallel changes on both `main` and `experiment` branches
5. Merge the `experiment` branch into `main`
6. Resolve merge conflicts manually when they occur
7. Simulate a Pull Request using GitHub
8. Tag milestone completion using semantic versioning (`v1.0`)

### Merge Conflict Resolution
A merge conflict occurred in the `README.md` file when both branches introduced changes. The conflict was resolved manually by keeping relevant content from both branches, demonstrating proper conflict resolution practices.

---

## Tools Used
- **Git** – Version control and branch management
- **GitHub** – Remote repository hosting, pull requests, and tagging
- **Visual Studio Code** – Integrated development environment
- **Docker** – Containerization (placeholder implementation)
- **Kubernetes** – Container orchestration (placeholder configuration)
- **Infrastructure as Code (IaC)** – Automation foundation (placeholder using tools such as Terraform)

---

## Contribution Guidelines
1. Create a new branch for each feature or enhancement
2. Commit changes with clear and meaningful messages
3. Push branches to GitHub
4. Create a Pull Request for review
5. Resolve conflicts before merging into `main`

---

## Milestone Tag
Milestone 1 completion is marked with the following Git tag: v1.0 – Milestone 1 complete
