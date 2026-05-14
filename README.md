# Mastering the Intricacies of DevOps

A structured, hands-on journey into DevOps — focused on internal mechanics, operational clarity, and production-grade workflows.

---

## Introduction

This repository starts with documenting a deep exploration of Docker — not just at the command level, but at the architectural level.

The goal is to understand:

- How containers actually work under the hood
- How image layers are constructed and reused
- How networking and storage are implemented
- How Docker integrates into real-world DevOps pipelines

This project follows a disciplined learning loop:

**Concept → Practical Implementation → Internal Breakdown → Documentation**

Every topic is studied, executed, analyzed, and recorded with intent.

---

## Unit 1: Docker Foundations and Advanced Practice

### Repository Learning Modules

**1.1** [Basics of Docker](./basicsdocker.pdf)

**1.2** [Continuation on My Progress on Docker](./Continuation%20on%20my%20progress%20on%20docker.pdf)

**1.3** [Docker Intermediates](./Docker%20intermediates.pdf)

**1.4** [Docker Practice and Advanced Work – Part 1](./Docker%20Practice%20and%20Advanced%20work-part%201.pdf)

**1.5** [Advanced Docker and Complete Practice – Part 2](./Advanced%20Docker%20and%20complete%20practice%20Part-2.pdf)

**1.6** [Advanced Docker and Final Practice](./Advanced%20Docker%20and%20final%20practice.pdf)

**1.7** [Mistakes Done and Learnings Made](./Mistakes%20done%20and%20learnings%20made.pdf)

**1.8** [Complete Practice of Docker with many scenarios (Part 1)](Complete%20Practice%20of%20Docker%20with%20many%20scenarios%20part1.pdf)

**1.9** [Docker Scenario Based Questions (Part 2)](./Docker%20Scenario%20Based%20questions%20part-2.pdf)

---

### Core Technical Domains Covered

#### Image Engineering

- Layer architecture and overlay filesystem
- Copy-on-write mechanism
- Build cache invalidation
- Tag mutability vs digest immutability
- Multi-stage builds

#### Networking

- Default vs user-defined bridge networks
- Docker embedded DNS
- Port publishing internals
- Host to Container communication
- Container to Container communication

#### Storage

- Named volumes
- Bind mounts
- Mount masking behavior
- Persistent data lifecycle
- Separation of image, container layer, and volume

#### Registry & Distribution

- Docker Hub vs GHCR
- Registry namespaces
- Token-based authentication
- Versioned image publishing
- Semantic versioning strategy

---

### Internal Understanding Developed

- How the Docker daemon handles image pulls and layer caching
- How namespaces and cgroups isolate container processes
- How overlay filesystems stack read-only layers with a writable layer
- How port binding routes traffic from host to container
- How volumes persist data independently of container lifecycle
- How multi-stage builds reduce final image size

---

### Practical Systems Built

- Custom image construction using multi-stage Dockerfiles
- MySQL container deployment with named volume persistence
- User-defined bridge network with inter-container DNS resolution
- Bind mount setup for live source code reflection
- Image tagging, versioning, and publishing to GHCR
- Final Armageddon deployment combining ENV, VOLUME, EXPOSE, semantic tagging, and registry push
- Debugging and iterating on broken builds — documented in the Mistakes and Learnings module

---

## Unit 2: Orchestration with Docker Compose, Networking and Swarm

### Introduction

With a solid understanding of individual containers, the next step is orchestration — managing multiple interconnected services as a single system.

This unit covers two layers of orchestration:

- **Docker Compose** — declarative multi-container management for local and single-host environments
- **Docker Swarm** — native clustering and distributed service orchestration across multiple nodes

Together, these tools bridge the gap between single-container execution and production-scale distributed systems.

---

### Repository Learning Modules

**2.1** [Complete Docker Compose Practice](./completeDockerComposePractice.pdf)

**2.2** [Docker Networking + Swarm Practicals](./Docker%20Networking%2BSwarm%20practicals.pdf)

---

### Core Technical Domains Covered

#### Multi-Container Architecture (Compose)

- Service abstraction
- Container dependency management
- Application-level structuring

#### Networking (Compose and Swarm)

- Default Compose network
- Embedded DNS-based service discovery
- Container to Container communication
- Host to Service exposure
- Overlay networks for cross-node communication in Swarm
- Ingress routing mesh

#### Storage

- Named volumes in Compose
- Data persistence across services
- Volume lifecycle independence
- Volume behavior in Swarm services

#### Configuration Management

- Environment variables
- YAML-based infrastructure definition
- Build vs Image strategies

#### Docker Swarm Orchestration

- Swarm initialization on a single node (manager setup)  
- Understanding service abstraction over containers  
- Creation of services using `docker service create`  
- Attaching services to overlay networks  
- Inter-service communication using service names (DNS)  
- Scaling services using replicas  
- Verification of load balancing across replicas  
- Understanding routing mesh through published ports  

---

### Internal Understanding Developed

- How Docker Compose translates YAML into container runtime instructions  
- How Docker automatically provisions networks for services  
- How DNS resolution replaces manual linking  
- How volumes decouple storage from containers  
- How multi-service systems behave during startup and shutdown  

- How Swarm uses service abstraction instead of direct container management  
- How routing mesh forwards incoming requests to available replicas  
- How load balancing distributes traffic across containers  
- How overlay networks enable communication between services  
- Difference between container-level and service-level networking  

---

### Practical Systems Built

- Node.js + MongoDB multi-container setup using Compose
- Service communication via internal DNS
- Persistent database using named volumes
- Port exposure and request routing
- Swarm cluster with manager and worker nodes
- Multi-replica service deployment with load balancing
- Rolling update with zero-downtime strategy
- Stack deployment from a Compose file into Swarm mode

---

### Compose and Swarm in the Bigger Picture

Docker Compose and Swarm together act as a bridge between:

- Single-container execution → Distributed multi-node systems
- Manual setup → Declarative infrastructure
- Local development → Production-ready architecture
- Single-host orchestration → Clustered service management

---

## Unit 3: Build Systems with Maven

### Introduction

After mastering containerization and orchestration, the next critical layer is build automation and dependency management.

Apache Maven plays a key role in:

- Structuring Java-based projects
- Managing dependencies efficiently
- Automating builds and packaging
- Integrating seamlessly with Docker-based workflows

---

### Repository Learning Modules

**3.1** [Complete Maven Mastery](./Complete%20Maven%20Mastery.pdf)

**3.2** [Maven Plugin and Packaging Practice](./Maven%20Final%20Armageddon-for%20pom%20practice.pdf)

**3.3** [Maven Final Practice](./Maven-final-armageddon.pdf)

---

### Core Technical Domains Covered

#### Project Structure & Lifecycle

- Standard directory layout
- Build lifecycle phases (validate → compile → test → package → install → deploy)
- Maven conventions over configuration

#### Dependency Management

- Transitive dependencies
- Dependency scopes (compile, provided, runtime, test)
- Conflict resolution (nearest definition strategy)

#### Build & Packaging

- JAR vs WAR packaging
- Plugins and goals
- Custom build configurations

#### POM (Project Object Model)

- XML structure and hierarchy
- GroupId, ArtifactId, Version
- Dependency declarations
- Plugin configuration

#### Integration with Docker

- Building artifacts for containerization
- WAR deployment into Tomcat containers
- Clean separation of build and runtime environments

---

### Internal Understanding Developed

- How Maven resolves dependencies from repositories
- How lifecycle phases map to actual build steps
- How plugins extend Maven functionality
- How builds become reproducible and consistent
- How Maven integrates into CI/CD pipelines

---

### Practical Systems Built

- Java Web Application (WAR packaging)
- Deployment on Tomcat using Docker
- Maven-based automated build pipeline
- Clean separation of source → artifact → container

---

### Maven in the Bigger Picture

Maven acts as a bridge between:

- Source code → Deployable artifact
- Manual compilation → Automated builds
- Local development → CI/CD pipelines

---

## Unit 4: CI/CD Pipelines (Automation & Deployment)

### Introduction

After mastering containerization, orchestration, and build systems, the final layer is automation — CI/CD.

CI/CD (Continuous Integration & Continuous Deployment) enables:

- Automated building, testing, and deployment
- Elimination of manual errors
- Faster and consistent delivery pipelines
- Production-grade DevOps workflows

---

### Repository Learning Modules

**4.1** [Complete CI/CD Mastery](./Complete-CI-CD-Mastery.pdf)

**4.2** [CI/CD Pipeline Implementation](./ci-cd-pipeline.pdf)

---

### Core Technical Domains Covered

#### Continuous Integration (CI)

- Automated build triggers on code push
- Maven-based build automation
- Dependency resolution in pipelines
- Artifact generation (JAR/WAR)

#### Continuous Deployment (CD)

- Automated Docker image creation
- Image tagging and versioning
- Push to container registry (GHCR/Docker Hub)
- Deployment-ready artifacts

#### Pipeline Architecture

- Workflow definition (GitHub Actions YAML)
- Job and Step execution model
- Event-based triggers (push, pull_request)
- Environment isolation (runners)

#### Docker + CI/CD Integration

- Build Docker images inside pipelines
- Multi-stage builds for optimization
- Registry authentication (tokens)
- Image publishing and version control

#### Automation & Reliability

- Eliminating manual build steps
- Reproducible deployments
- Version-controlled infrastructure
- Failure handling in pipelines

---

### Internal Understanding Developed

- How CI/CD pipelines execute step-by-step on remote runners
- How GitHub Actions converts YAML into executable workflows
- How build → test → package → dockerize → deploy flows work
- How artifacts move across stages
- How authentication enables secure registry access
- How pipelines ensure consistency across environments

---

### Practical Systems Built

- Maven-based automated build pipeline
- Docker image creation inside CI pipeline
- Image push to GitHub Container Registry (GHCR)
- Fully automated CI → CD workflow
- Version-controlled deployment process

---

### CI/CD in the Bigger Picture

CI/CD acts as the bridge between:

- Code → Automated Build → Deployment
- Manual execution → Fully automated pipelines
- Development → Production systems

---

## Unit 5: Jenkins Mastery (CI/CD Orchestration Engine)

### Introduction

After building a strong foundation in CI/CD pipelines, the next step is mastering Jenkins — a powerful automation server used to orchestrate complete DevOps workflows.

This unit focuses on:

- Understanding Jenkins architecture (Controller → Agent model)
- Building and managing CI/CD pipelines
- Integrating Maven and Docker into Jenkins workflows
- Executing distributed builds using agent nodes
- Understanding real-world pipeline execution and debugging

---

### Repository Learning Modules

**5.1** [Complete Jenkins Mastery (CI/CD)](./Complete%20Jenkins%20Mastery%28CI-CD%29.pdf)

---

### Core Technical Domains Covered

#### Jenkins Architecture

- Controller (master) vs Agent (node) model
- Distributed build execution
- Label-based node selection
- Workspace allocation per node

#### Pipeline Development

- Declarative pipeline syntax
- Stages and steps
- Post actions (success, failure, always)
- Pipeline structuring and readability

#### Maven Integration

- Tool configuration in Jenkins
- Automated build lifecycle execution
- Artifact generation (JAR/WAR)
- Build reproducibility

#### Docker Integration

- Running Docker commands inside pipelines
- Image build and container execution
- Container lifecycle management via Jenkins
- Debugging containerized applications

#### Distributed Builds (Nodes)

- Creating and configuring Jenkins agents
- Connecting agents using `agent.jar`
- Running pipelines on remote nodes
- Understanding node workspaces and execution flow

---

### Internal Understanding Developed

- How Jenkins schedules and distributes jobs
- How pipelines are executed step-by-step
- How tools like Maven and Docker integrate into CI/CD workflows
- How agent nodes handle execution independently
- How workspace isolation works across nodes
- How failures propagate through pipeline stages

---

### Practical Systems Built

- Jenkins pipeline for Docker command execution
- Maven-based build pipeline
- Maven + Docker integrated pipeline
- Fully automated CI/CD workflow
- Distributed pipeline execution using agent node

---

### Jenkins in the Bigger Picture

Jenkins acts as the bridge between:

- Source Code → Build → Containerization → Deployment
- Individual tools → Unified automation system
- Manual processes → Fully automated DevOps pipelines

---
## UNIT-6 Special Practicals(Final Armageddon preparation)

### Microservices Docker CI/CD-1

- [Design and Implementation of Docker Microservices with CI-CD](./Design%20and%20Implementation%20of%20Docker%20Microservices%20with%20CI-CD.pdf)

A hands-on implementation of a containerized microservices system using Docker Compose, consisting of NGINX (frontend), Node.js (backend), and MySQL (database). 

Includes a complete CI/CD pipeline using GitHub Actions with:
- MySQL integration testing (service readiness + API validation)
- Automated Docker image build and push to Docker Hub

Focus: service communication, reverse proxy, container networking, and real CI/CD workflow.

### Microservices Docker CI/CD-2

- [Production-Ready Dockerized Microservices with Nginx, Node.js, MongoDB & CI/CD Pipeline](./End_to_End_Docker_Nginx_Node_Mongo_CI_CD.pdf)

A hands-on implementation of a containerized microservices system using **Docker Compose**, consisting of **NGINX (frontend), Node.js (backend), and MongoDB (database)**.

Includes a complete **CI/CD pipeline using GitHub Actions** with automated service-level and integration testing, along with Docker image build and push.

Focus: reverse proxy routing, container networking, environment-based configuration, and real-world CI/CD workflow.

### WordPress Docker Deployment

- [WordPress Deployment with Nginx Reverse Proxy and MySQL](./WordPress%20Deployment%20with%20Nginx%20Reverse%20Proxy%20and%20MySQL.pdf)

A hands-on implementation of a **containerized WordPress application** using Docker Compose, consisting of **Nginx (reverse proxy)**, **WordPress (PHP-FPM backend)**, and **MySQL (database)**.

Includes practical setup of **service orchestration**, **reverse proxy configuration**, and **database connectivity**, along with persistent storage using Docker volumes.

Focus: reverse proxy routing, multi-container architecture, environment-based configuration, Docker networking, and real-world debugging of database connectivity issues.

### Multi-Node Docker Swarm Cluster

- [Multi-Node Docker Swarm Cluster with Distributed Service Orchestration](./Multi-Node%20Docker%20Swarm%20Cluster%20with%20Distributed%20Service%20Orchestration.pdf)

A hands-on implementation of a **distributed container orchestration system** using **Docker Swarm**, consisting of a **Manager node** and multiple **Worker nodes** simulated via Docker-in-Docker (dind).

Includes **service creation with replicas**, **dynamic scheduling**, **self-healing**, and **load balancing** using the ingress routing mesh.

Focus: cluster setup, service orchestration, task scheduling, routing mesh networking, and fault-tolerant distributed systems.

### Special Practicals – Jenkins CI/CD-1

- [Design and Implementation of a CI Pipeline using Jenkins, Maven, and Docker for Java Applications (done via both Pipeline script and Jenkinsfile)](Special%20practicals-Jenkins%20part%201.pdf)

A hands-on implementation of real-world CI/CD workflows using Jenkins, covering both UI-based Pipeline scripts and Jenkinsfile (Pipeline as Code) approaches.

Includes automated build, testing, Docker-based containerization, webhook-triggered execution, and email notifications for failure handling.

#### Special Practicals Covered:
**1.** Jenkins-Based Python CI Pipeline with Webhook Automation and Email Notifications  
**2.** Design and Implementation of a CI Pipeline using Jenkins, Maven, and Docker for Java Applications  

Focus: CI automation, pipeline design, containerized builds, GitHub integration, and production-style DevOps workflows.

### Special Practicals – Jenkins Distributed CI/CD-2

- [Jenkins Controller-Agent Architecture on AWS EC2](./Special%20Practicals%20Jenkins-2.pdf)

A hands-on implementation of a distributed Jenkins CI/CD architecture using a local Jenkins Controller and an AWS EC2 Ubuntu instance configured as a remote Agent node via SSH communication.

Includes secure SSH-based agent connectivity, remote build execution, Jenkins node configuration, environment variable management, Linux permission handling, and distributed job scheduling using node labels.

Focus: controller–agent architecture, Jenkins remoting, SSH authentication, distributed build execution, temporary directory management, Linux permissions, resource monitoring, and CI/CD fundamentals.

### Special Practicals - Dockerized React Vite application

- [Multi-Stage Dockerized React Vite Deployment using Nginx and CI Pipeline](./Multi-Stage%20Dockerized%20React%20Vite%20Deployment%20using%20Nginx%20and%20CI%20Pipeline.pdf)

A hands-on implementation of a containerized React Vite frontend application using a multi-stage Docker build and Nginx production server.

Includes Docker-based frontend build optimization, static asset serving, automated CI pipeline using GitHub Actions, and Docker Hub image publishing.

Focus: React Vite production builds, Nginx frontend hosting, Docker image optimization, containerized frontend deployment, and CI workflow automation.

### Dockerized Java Web Application Deployment

- [Dockerized Java Web Application Deployment Using Maven WAR and Apache-Tomcat](./Dockerized%20Java%20Web%20Application%20Deployment%20Using%20Maven%20WAR%20and%20Apache-Tomcat.pdf)

A hands-on implementation of a containerized Java web application using Maven, JSP, Apache Tomcat, and Docker, demonstrating the complete workflow from WAR generation to Tomcat-based deployment.

Includes practical setup of Maven project structure, WAR packaging, JSP rendering, Tomcat auto-deployment, Docker image creation, and containerized web hosting with port mapping.

Focus: Java web architecture, JSP and Servlets fundamentals, Apache Tomcat deployment lifecycle, Docker-based application containerization, WAR deployment mechanics, and real-world Java DevOps workflow understanding.

### Multi-Container Spring Boot + PostgreSQL Deployment

- [Multi-Container Orchestration of Spring Boot and PostgreSQL Using Docker Compose](Springboot-postgres-devops.pdf)

A hands-on implementation of a **containerized backend infrastructure** using Docker Compose, consisting of **Spring Boot (backend application)** and **PostgreSQL (database)**.

Includes practical setup of **Docker image building**, **service orchestration**, **healthchecks**, **persistent storage using Docker volumes**, and **environment-based configuration**.

Focus: multi-container architecture, Docker networking, containerized Java deployment, PostgreSQL integration, health monitoring, restart policies, and real-world backend infrastructure orchestration.

### Multi-Container Microservices Scaling Using Docker Compose and Nginx

- [Scaling Microservices for High Traffic Using Docker Compose and Nginx](Scaling%20Microservices%20for%20High%20Traffic%20Using%20Docker%20Compose%20and%20Nginx.pdf)

A hands-on implementation of a scalable containerized microservices infrastructure using Docker Compose, consisting of multiple Flask backend containers and an Nginx reverse proxy/load balancer.

Includes practical setup of Docker image building, horizontal container scaling, reverse proxy configuration, load balancing, Docker networking, healthchecks, restart policies, and service orchestration using Docker Compose.

Focus: microservices scalability, Docker bridge networking, Nginx load balancing, container orchestration, health monitoring, reverse proxy architecture, stateless backend deployment, and real-world high-traffic backend infrastructure design.

### Microservices API Gateway using Docker and Nginx

- [Implementation of a Microservices API Gateway using Docker Compose](./Implementation%20of%20a%20Microservices%20API%20Gateway%20using%20Docker%20Compose.pdf)

A hands-on implementation of a **containerized microservices infrastructure** using Docker Compose, consisting of an **Nginx API Gateway** and multiple backend microservices.

Includes practical setup of **reverse proxy architecture**, **container orchestration**, **Docker networking**, **service discovery**, **path-based routing**, and **multi-container communication** using Docker Compose.

Focus: API Gateway pattern, Nginx reverse proxy, Docker Compose orchestration, microservices communication, internal container networking, restart policies, and real-world DevOps-based backend infrastructure deployment.

### Docker Compose Based Multi-Container Web Application with Redis Persistence

- [Docker Compose Based Multi-Container Web Application with Redis Persistence](./Docker%20Compose%20Based%20Multi-Container%20Web%20Application%20with%20Redis%20Persistence.pdf)

A hands-on implementation of a containerized web infrastructure using Docker Compose, consisting of an Nginx frontend container, a Node.js backend service, and a Redis persistence layer.

Includes practical setup of container orchestration, Docker networking, Redis data persistence, inter-container communication, environment variable configuration, restart policies, and persistent storage management using Docker volumes.

Focus: Docker Compose orchestration, Redis persistence with AOF, multi-container communication, internal container networking, frontend-backend integration, persistent Docker volumes, restart policies, and real-world DevOps-oriented infrastructure deployment.

## Final Armageddon Deployment

A full production-style integration combining:

- Custom Dockerfile
- ENV configuration
- VOLUME declaration
- EXPOSE instruction
- Semantic tagging (1.0.0, latest)
- Publishing to GHCR
- Persistent storage
- Versioned deployment flow

Demonstrates:

- Image immutability
- Volume persistence across rebuilds
- Registry boundary control
- Deployment reproducibility

---

## Tools & Environment

- Docker Engine
- Alpine & Ubuntu images
- MySQL container deployments
- Git & GitHub
- GitHub Container Registry (GHCR)
- Windows + Git Bash workflow

---

## Philosophy

This repository is not about memorizing commands.

It is about understanding:

- What happens inside the kernel
- How namespaces isolate processes
- How overlay filesystems manage layers
- How registries store image manifests
- Why volumes outlive containers
- How version tags affect deployment stability

Understanding Docker deeply is not about running containers.

It is about understanding what truly happens when you do.

---

## Long-Term Direction

This foundation directly supports:

- CI/CD automation
- Microservices architecture
- Image optimization
- Secure software supply chains
- Kubernetes orchestration

---

## Maintained by

**Sreevishnu07**

A disciplined journey toward mastering systems, infrastructure, and production-grade software engineering.
