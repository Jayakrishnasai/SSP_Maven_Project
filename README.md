# SSP_Maven_Project

## Overview
This is a simple web application for SHIVA SAI PERSEVERANCE, a software training institute. The application is built using Java and Maven, and it serves a static landing page with information about courses, schedules, mentors, and admissions.

## Features
- **Static Landing Page**: A single-page web application with a responsive design.
- **Course Information**: Displays a list of available courses with descriptions and schedules.
- **Mentor Profiles**: Introduces the mentors with their expertise.
- **Contact Form**: Allows users to submit their information for admissions.

## Prerequisites
- **Java Development Kit (JDK) 8** or higher
- **Apache Maven 3.6** or higher
- **Apache Tomcat 9** or higher (for deployment)
- **Docker** (optional, for containerized deployment)
- **Jenkins** (for CI/CD)

## Build Instructions
To build the project, run the following command from the root directory:
```bash
mvn clean install
```
This will generate a `ssp.war` file in the `target` directory.

## Deployment Instructions
### Manual Deployment
1. Copy the `ssp.war` file from the `target` directory to the `webapps` directory of your Tomcat installation.
2. Start the Tomcat server.
3. The application will be accessible at `http://localhost:8080/ssp`.

### Docker Deployment
1. Build the Docker image:
```bash
docker build -t ssp-maven-project .
```
2. Run the Docker container:
```bash
docker run -p 8080:8080 ssp-maven-project
```
3. The application will be accessible at `http://localhost:8080/ssp`.

## CI/CD
This project is configured with a Jenkins pipeline for continuous integration and deployment. The `Jenkinsfile` in the root directory defines the pipeline stages:
1. **Checkout**: Clones the repository.
2. **Build**: Compiles the code and runs unit tests.
3. **Deploy**: Deploys the application to a staging environment.

## Folder Structure
```
.
├── pom.xml
└── src
    └── main
        └── webapp
            ├── WEB-INF
            │   └── web.xml
            └── index.jsp
```

## Contact Information
- **Email**: `shivasai.praveen@gmail.com`
- **Phone**: `+91-9876543210`
