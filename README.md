📘 ITSA‑5501 – DevOps and System Integration
Project

## 🧩 Milestone 1 – Git Workflow & Version Control
Overview
Milestone 1 focused on establishing a proper Git workflow using branching, merging, conflict resolution, pull requests, tagging, and repository documentation. This phase established the foundation of version control best practices for the project.

🔧 Completed Tasks (Milestone 1)
1. Repository Initialization

- A new Git repository was created for the project.
- Initial commits included project setup and base folder structure.
- Commit messages followed clear, descriptive wording to reflect changes accurately.

2. Branching Strategy

- A new branch named experiment was created.
- Several commits were added to simulate isolated feature development.
- Demonstrated switching branches and maintaining clean version history.

3. Merge & Conflict Resolution

- The experiment branch was merged into main.
- Conflicts were intentionally created and successfully resolved.
- Screenshots documented:
    Conflict appearance
    Manual file editing
    git add and git commit steps
    Clean merge



4. Pull Request Simulation

A PR was created on GitHub to simulate collaborative workflow.
Since changes were merged locally already, GitHub showed no diff — confirming proper merge.

5. Tagging & Release Marking

A tag was added to mark Milestone 1 completion.


## 🚀 Milestone 2 – Multi‑Container Deployment with Docker Compose
Milestone 2 focuses on multi‑container application deployment using Docker, Docker Compose, service networking, Prometheus configuration, and container scaling.

📂 Updated Project Structure (After Milestone 2)
ITSA-5501_Project_Fatima/
│
├── docker/
│   └── docker-compose.yml
│
├── frontend/
│   └── index.html
│
├── prometheus.yml
│
├── iac/
│   └── main.tf
│
├── k8s/
│   └── deployment.yaml
│
├── .gitignore
└── README.md


## 🌐 Milestone 2 Details

1. Frontend Setup
A frontend folder was created with an index.html page describing a vacation destination, satisfying the requirement to create a static webpage served through Nginx.

2. Docker Compose – Multi‑Container Configuration
A complete docker-compose.yml was created under the /docker folder containing the following services:
🟦 Services Included
    frontend – NGINX serving HTML
    user-db – MongoDB with persistent user_data volume
    product-db – PostgreSQL with persistent product_data volume
    cache – Redis
    prometheus – Monitoring service exposed on port 9091

🟦 Networking
All services share a custom internal network: app-network


3. Prometheus Configuration
A prometheus.yml file was added at the project root, containing:
    scrape_interval: 15s
    Prometheus job targeting: localhost:9090

4. Running Containers
The entire stack was started using:
    docker-compose up -d

All containers were verified using:
    docker ps

5. Verifying Services
✔ Frontend
    http://localhost:9090
✔ Prometheus Dashboard
    http://localhost:9091


6. Scaling the Frontend Service
As required by the milestone, the frontend was scaled to three instances:
    docker-compose up --scale frontend=3 -d

Verification via:
    docker ps

The output correctly showed:
    frontend‑1
    frontend‑2
    frontend‑3

This fulfills the container scaling requirement. 