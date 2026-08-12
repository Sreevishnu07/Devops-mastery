# Mastering the Intricacies of DevOps 
**Update: Many Advanced Practicals for Puppet,Ansible,Nagios,Terraform are being added,scroll through to find the additions** 

A structured, hands-on journey into Docker, CI/CD, and production-grade DevOps workflows.

This repository documents practical implementations and internal understanding of:

- Docker and Dockerfiles
- Docker Compose
- Docker Swarm
- Container Networking
- CI/CD Pipelines
- GitHub Actions
- Jenkins
- Maven Workflows
- Puppet's Configuration Management

The focus is not just on using tools, but understanding how they operate internally and how they integrate into real-world deployment pipelines.

**Concept → Practical Implementation → Internal Breakdown → Documentation**

Every topic is studied, executed, analyzed, and recorded with intent.

---

## A Very Special Note

A special thanks to **Dr. Harpreet Kaur** mam for being the sole source of inspiration behind this journey.

What started as learning Docker gradually turned into more than 3 months of deep exploration, consistent practice, and countless hours of building and experimenting. From beginner-level concepts to advanced DevOps workflows, this repository represents a structured hands-on journey through real implementation and internal understanding.And **starting with a deep dive into Configuration Management and IaC**,manifesting that this journey to be even more fruitful.

**This journey includes:**

- A very large collection of practicals ranging from foundational to advanced concepts
- 14 special practicals built with dedicated repositories
- CI/CD integration included across repositories wherever applicable
- Architecture-level understanding alongside implementation

This **INT-332 course** has genuinely been one of the most special and impactful learning experiences throughout this process and my college life.
Thereby **INT-333 course** and its documentation would be done in the days to come.
This README is designed to provide the complete structure, navigation flow, and step-by-step organization of the repository so every section can be explored systematically.

> **Make sure to check out the 12 Special Practicals section in the README.**

# DevOps / CI-CD / Docker / Microservices Practical Repository Collection

These 14 repositories are fully CI-CD enabled practical projects.  
Each project teaches a new real-world DevOps, Docker, Jenkins, GitHub Actions, deployment, scaling, microservices, or infrastructure concept through hands-on implementation.

---

## Special Practical Repositories

1. [Docker Compose Microservices Scaling](https://github.com/Sreevishnu07/docker-compose-microservices-scaling)

2. [Spring Boot + PostgreSQL DevOps Stack](https://github.com/Sreevishnu07/springboot-postgres-devops-stack)

3. [Docker WordPress + Nginx + MySQL](https://github.com/Sreevishnu07/docker-wordpress-nginx-mysql)

4. [React + Nginx Docker Deployment](https://github.com/Sreevishnu07/react-nginx-docker-deployment)

5. [Node + Mongo Microservices Docker](https://github.com/Sreevishnu07/node-mongo-microservices-docker)

6. [Docker Compose Service Dependency Healthcheck](https://github.com/Sreevishnu07/docker-compose-service-dependency-healthcheck)

7. [Microservices Docker CI-CD](https://github.com/Sreevishnu07/Microservices-Docker-CI-CD)

8. [Microservices API Gateway](https://github.com/Sreevishnu07/microservices-api-gateway)

9. [Fullstack CI-CD Pipeline](https://github.com/Sreevishnu07/fullstack-cicd-pipeline)

10. [Flask GHCR Pipeline](https://github.com/Sreevishnu07/flask-ghcr-pipeline)

11. [Maven CI Workflow](https://github.com/Sreevishnu07/maven-ci-workflow)

12. [Jenkins Practice 2](https://github.com/Sreevishnu07/jenkins-practice2)

13. [Jenkins Practice 3](https://github.com/Sreevishnu07/jenkins-practice3)

14. [Jenkins Practice 4](https://github.com/Sreevishnu07/Jenkins-practice4)

---

# Special Highlight Project — XAI Threat Detection System

A complete end-to-end Explainable AI threat detection project with:
- CI/CD pipeline integration
- EC2 cloud deployment
- Dockerized infrastructure
- Real-world deployment workflow
- Explainable AI based threat analysis(Gradcam++,Scorecam,Integrated Gradients)
- Production-style architecture(FastAPI,Streamlit and much more)

🔗 [XAI Threat Detection](https://github.com/Sreevishnu07/XAI-Threat-Detection)

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

**2.3** [Ultimate Docker Compose Practice: Extensive Multi-Service Interaction Scenarios](./Docker%20Scenario%20Based%20Questions-3.pdf)

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

## Tools and Environment

- Docker Engine
- Dockerfiles
- Docker Compose
- Docker Swarm
- Alpine, Ubuntu, and other lightweight base images
- Multi-container application deployment and container networking
- MySQL
- PostgreSQL
- MongoDB
- Redis
- Containerized database deployments
- Git
- GitHub
- GitHub Container Registry (GHCR)
- Windows + Git Bash workflow
- Jenkins
- Maven
- GitHub Actions
- Amazon EC2 deployments
- CI/CD pipeline setup and automation
- DevOps Mastery project implementation involving Dockerized applications, Swarm orchestration, automated builds, container registries, database integration, and cloud deployments

---
# Start of INT333

## Unit 1: Puppet Configuration Management and Infrastructure Automation

### Introduction

After mastering containerization, orchestration, build automation, and CI/CD pipelines, the next critical layer is **Configuration Management**.

Puppet enables infrastructure to be managed declaratively, allowing servers to be configured, monitored, and maintained consistently across development, testing, and production environments.

This unit focuses not only on writing Puppet manifests but also on understanding how Puppet internally compiles catalogs, manages system state, structures reusable modules, and scales infrastructure automation.

---

## Repository Learning Modules

**1. Puppet Mastery Part-1**

- [Complete Puppet Mastery Part-1.pdf](Complete%20Puppet%20Mastery%20Part-1.pdf)

**Topics Covered**
- 1.1 Puppet Installation and Development Environment
- 1.2 Puppet Development in Isolation
- 1.3 Advanced Puppet Configuration
- 1.4 Managing Software Packages with Puppet
- 1.5 Designing and Deploying Custom Puppet Modules
- 1.6 Production-Style Puppet Modules
- 1.7 Parameterized and Reusable Puppet Modules
- 1.8 EPP Templates and Dynamic Configuration Generation

**2. Puppet Mastery Part-2**

- [Complete Puppet Mastery Part 2.pdf](Complete%20Puppet%20Mastery%20Part%202.pdf)

**Topics Covered**
- 2.1 Monitoring and Managing Apache Web Server Using Puppet
- 2.2 Deploying and Configuring a Secure Puppet Master-Agent Infrastructure
- 2.3 Centralized Configuration Management Using Puppet Master Catalogs

**3. Puppet Mastery Part-3 (Flagship Standalone Practical-1)**

- [Complete Puppet Mastery Part-3 (Flagship Standalone Practical).pdf](Complete%20Puppet%20Mastery%20Part-3%28Flagship%20standalone%20practical%29.pdf)

**Topics Covered**

- 3.1 Enterprise Dynamic Configuration Management Using Puppet Facts, EPP Templates, Parameterized Classes, and Centralized Modules
- 3.2 Dynamic Resource Management Using Facter and Structured Facts
- 3.3 Multi-Node Configuration with Parameterized Modules and Resource Relationships

4. **Puppet Mastery Part-4 (Standalone Flagship Practical-2)**

- [Complete Puppet Mastery Part-4 (Standalone Flagship Practical-2).pdf](./Complete%20Puppet%20Mastery%20Part-4%28Standalone%20Flagship%20practical-2%29.pdf)

**Topics Covered**

- 4.1 Enterprise Multi-Environment Configuration Management Using Puppet Production and Development Environments
- 4.2 Environment Isolation, Catalog Compilation, and Environment-Specific Module Deployment
- 4.3 Managing Multiple Puppet Agents with Independent Environments, Dynamic Templates, and Centralized Puppet Server

5. **Puppet Mastery Part-5 (Standalone Flagship Practical-3)**

- [Complete Puppet Mastery Part-5 (Standalone Flagship Practical-3).pdf](./Complete%20Puppet%20Mastery%20Part-5%28Standalone%20Flagship%20Practical-3%29.pdf)

**Topics Covered**

- **5.1** Enterprise Data-Driven Configuration Management with Hiera, Automatic Parameter Lookup (APL), and Multi-Environment Puppet

- **5.2** Hierarchical Data Management Using Node, Environment, and Common YAML Files with Automatic Parameter Lookup and Explicit Hiera Lookups

- **5.3** Centralized Multi-Environment Puppet Deployments with Data-Driven Modules, Environment Isolation, EPP Templates, and Dynamic Package Management

6. **Puppet Mastery Part-6 (Practical 15) (Flagship Practical-4)**

- [Puppet Mastery Part-6,Practical 15(Flaghsip Practical-4).pdf](<https://github.com/Sreevishnu07/Devops-mastery/blob/main/Puppet%20Mastery%20Part-6%2CPractical%2015(Flaghsip%20Practical-4).pdf>)

**Topics Covered**

- **6.1** Enterprise Data-Driven Puppet Automation Using Hiera, Automatic Parameter Lookup (APL), Facts, Parameterized Classes, and Multi-Layer Configuration Management
- **6.2** Advanced Custom Puppet Functions with Typed Parameters, Default Values, Validation, Conditional Logic, Structured Return Types, and True Function Composition
- **6.3** Production-Style Dynamic Configuration Using EPP Templates, OS-Aware Package and Service Management, Resource Relationships, Notifications, and End-to-End Catalog Deployment

7. **Puppet Mastery Part-7 (Flagship Practical-5)**

- [Puppet Mastery Part-7 (Flagship Practical-5).pdf](./Puppet%20Mastery%20Part-7%28Flagship%20practical-5%29.pdf)

**Topics Covered**

- **7.1** Enterprise Load Balancing Using HAProxy, Puppet-Managed Web Server Clusters, and Round-Robin Traffic Distribution
- **7.2** High-Availability Load Balancing with Backend Health Checks, Automatic Failover, Recovery, and Puppet-Enforced Service State
- **7.3** Data-Driven Horizontal Scaling Using Hiera, APL, Puppet Hashes, EPP Iteration, and Multi-Node HAProxy Backend Management

8. **Puppet Mastery Part-8 (Practical 17) — Ruby Foundations for Puppet, Puppet DSL, and Custom Function Integration**

**Topics Covered**

- **8.1** Ruby Fundamentals for Puppet — Variables, Arrays, Hashes, Conditions, Methods, Blocks, and Iteration
- **8.2** Ruby Methods vs Puppet Custom Functions, Typed Parameters, Return Values, and Function-Based Configuration Logic
- **8.3** Understanding Puppet DSL, Ruby Influence, Catalog Compilation, and Integration of Custom Functions with Puppet Manifests

---

## Core Technical Domains Covered

### Puppet Fundamentals

- Declarative Infrastructure as Code
- Resources and Resource Types
- Desired State Configuration
- Idempotency
- Puppet Manifests
- Catalog Compilation
- Puppet Language Fundamentals

### Puppet Configuration

- `puppet.conf`
- Main, Agent and Master configuration sections
- Environment management
- Module path configuration
- Configuration precedence
- Puppet CLI utilities
- Manifest validation and debugging

### Package Management

- Package resources
- Package providers
- APT provider abstraction
- Package installation, removal and updates
- Version management
- Provider architecture

### Module Development

- Standard Puppet module structure
- `init.pp`
- Multiple manifest organization
- Namespaces
- Production-style module architecture
- Separation of responsibilities

### Parameterized Modules

- Typed parameters
- String, Integer and Boolean data types
- Default parameter values
- Class declarations
- Parameter forwarding
- Variable interpolation

### EPP Templates

- Embedded Puppet (EPP)
- Dynamic configuration generation
- Template rendering
- Passing variables into templates
- Separation of logic and configuration
- Production configuration management

### Service Management

- Package-Service relationships
- Service lifecycle management
- Automatic startup configuration
- Configuration enforcement
- Idempotent service management

---

## Internal Understanding Developed

- How Puppet compiles manifests into catalogs.
- How resources are evaluated against the current system state.
- How providers abstract operating-system-specific implementations.
- How Puppet enforces idempotency through desired state reconciliation.
- How Puppet discovers modules using `modulepath`.
- How `include` automatically loads `manifests/init.pp`.
- How namespaces organize enterprise-scale Puppet modules.
- How parameterized classes enable reusable infrastructure code.
- How parameters are forwarded between multiple classes.
- How EPP templates generate dynamic configuration files.
- Difference between static files and dynamically rendered templates.
- Production practices followed by official Puppet Forge modules.
- Difference between declarative configuration management and imperative system administration.

---

## Practical Systems Built

- Puppet standalone development environment
- Custom Puppet module from scratch
- Production-style multi-class Puppet module
- Automated package management
- File and configuration management
- Parameterized reusable modules
- Dynamic configuration generation using EPP templates
- Service management automation
- Idempotent infrastructure validation
- Enterprise-style module architecture

---

## Puppet in the Bigger Picture

Puppet acts as the bridge between:

```
    Manual Server Administration
                ↓
    Infrastructure as Code
                ↓
Individual Server Configuration
                ↓
Enterprise Configuration Management
                ↓ 
      Imperative Administration
                ↓
Declarative Desired State Management
                ↓
      Static Configuration
                ↓
Reusable Parameterized Infrastructure
                ↓
        Manual Changes
                ↓
Consistent Automated Infrastructure
```
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
