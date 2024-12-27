# Docker Project Overview

## Project Goal
- **Objective**: To create a Dockerized environment for setting up and running Jenkins, enabling efficient and consistent deployment of CI/CD pipelines.

---

## Key Components in the Dockerfile

### 1. **Base Image**
- **Image Used**: `ubuntu:24.04`
  - A lightweight and updated Linux distribution, serving as the foundation for installing Jenkins and its dependencies.

### 2. **Environment Preparation**
- Switched to `root` user to allow unrestricted package installation and configuration.

### 3. **Package Installation**
- **OpenJDK 17**: Required for running Jenkins, as it depends on Java.
- **Essential Utilities**: Installed `wget`, `curl`, and `gnupg` to manage repositories and download files.
- **Jenkins Installation**:
  - Added Jenkins' official repository key and source.
  - Installed Jenkins using `apt`.

---

## Features of the Docker Image

### Automation
- Fully automates the installation of Jenkins, reducing manual setup.

### Port Exposure
- Opens port `8080`, allowing Jenkins to be accessible externally.

### Default Behavior
- Automatically starts Jenkins using the `jenkins.war` file located at `/usr/share/java/jenkins.war`.

---

## Key Docker Commands Used

### Building the Image
```bash
docker build -t jenkins:latest .
