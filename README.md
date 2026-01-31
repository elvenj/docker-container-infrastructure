# Docker Container Infrastructure & GCP Artifact Registry

## 📋 Overview
This project demonstrates a complete containerization workflow using **Docker** and **Google Cloud Platform (GCP)**. It implements infrastructure-as-code principles to decouple applications from the underlying infrastructure, treating infrastructure as a managed application.

The project involves building a Node.js application, defining container specifications via Dockerfile, and managing the container lifecycle through **Google Artifact Registry**.

## 🏗 Architecture
The pipeline follows standard DevOps practices for container management:
1.  **Development**: Node.js application creation.
2.  **Containerization**: Defining the build context and layers using `node:lts`.
3.  **Registry Management**: Pushing immutable images to Google Artifact Registry (Europe-West4).
4.  **Deployment**: Pulling and running containers in isolated environments with port mapping.

## 🚀 Key Objectives Achieved
* **Container Build Strategy**: Multi-layer image construction and optimization.
* **Registry Operations**: Authentication and management of private Docker repositories on GCP ().
* **Debugging & Introspection**: Using `docker inspect`, `docker exec`, and log analysis for runtime troubleshooting.
* **Portability**: Validated infrastructure independence by running containers seamlessly across different host environments.

## 🛠 Tech Stack
* **Cloud Provider**: Google Cloud Platform (GCP)
* **Container Engine**: Docker
* **Registry**: Google Artifact Registry
* **Runtime**: Node.js (LTS)
* **CLI Tools**: gcloud SDK, Docker CLI

## 📂 Repository Structure
```bash
├── Dockerfile      # Container specification and build instructions
├── app.js          # Node.js application source code
├── README.md       # Project documentation
└── LICENSE         # MIT License
```

## 🔧 Usage
To run this container locally:

```bash
# Build the image
docker build -t node-app:0.2 .

# Run in background (mapped to port 4000)
docker run -p 4000:80 -d node-app:0.2

# Verify response
curl http://localhost:4000
```

---
*Developed as part of the Cloud Infrastructure & DevOps Portfolio.*
