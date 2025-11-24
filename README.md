# SMART-HEALTH-MONITORING-ALERT-SYSTEM-PROJECT-REPORT
 
 Overview of the project
 
The Smart Health Monitoring System is a modular real-time health analytics platform that collects vital parameters (heart rate, SpO₂, temperature) from sensors or user inputs, processes them through backend anomaly-detection logic, and triggers automated alert workflows. The architecture includes secured authentication, role-based access control, encrypted data handling, and an event-driven alert engine. Historical data is stored for trend analysis and audit logging, while the system’s API-centric design enables seamless integration with IoT devices, mobile apps, and clinical dashboards. This ensures fast, reliable, and scalable monitoring of critical health parameters with high data integrity and operational efficiency.

Features

Real-time Vital Monitoring: Continuously tracks heart rate, SpO₂, and body temperature using sensor data or user inputs.
Anomaly Detection Engine: Identifies abnormal patterns with threshold-based and rule-based validation.
Automated Alerts: Generates instant Warning, Critical, or Emergency alerts with event-driven notifications.
Secure Authentication: Implements user login, role-based access control, and data-level permission handling.
Encrypted Data Management: Ensures secure storage of user profiles, health history, and logs.
Health Trends & Insights: Displays historical records, charts, and analytics for long-term pattern analysis.
Audit & Activity Logging: Captures all system actions for traceability and compliance.
Modular Architecture: Supports easy scaling, maintenance, and feature expansion.
API-Ready System: Exposes structured endpoints for integration with IoT devices, web dashboards, or mobile apps.
Cross-Platform Compatibility: Works with cloud servers, edge devices, or standalone desktop environments.
Fault-Tolerant Design: Detects sensor errors, invalid data inputs, and fallback recovery mechanisms.
Privacy Protection: Ensures secure data flow with encryption, access rules, and compliance-oriented design.

Technologies/tools used

Frontend: HTML5, CSS3, JavaScript
Backend: Java Spring Boot (or Django / Node.js depending on setup)
Database: MySQL
Design Tools: Draw.io (ERD), Lucidchart
Development: VS Code, Git & GitHub
Testing: Postman
Deployment: Docker / Apache / Nginx

Steps to install & run the project

 Install Dependencies
mvn clean install
Configure the Database
Create MySQL database:
CREATE DATABASE smart_health_monitor;
Open src/main/resources/application.properties and update:
spring.datasource.url=jdbc:mysql://localhost:3306/smart_health_monitor
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD
spring.jpa.hibernate.ddl-auto=update
 Run the Application
mvn spring-boot:run
Access the Application
Open browser at:
http://localhost:8080/

Instructions for Testing

Testing via Postman (Recommended)
Open Postman
Import the included API collection (if provided)
Test endpoints such as:
Create patient health record
POST http://localhost:8080/api/health/create
Sample JSON body:
{
  "patientId": 101,
  "heartRate": 88,
  "temperature": 98.3,
  "oxygenLevel": 96
}

Fetch all health records
GET http://localhost:8080/api/health/all

Fetch specific patient record
GET http://localhost:8080/api/health/101
Unit Testing (JUnit)
Run:
mvn test
