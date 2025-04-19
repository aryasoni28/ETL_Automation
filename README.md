# ETL_Automation
ETL Automation System with Spring Boot
A robust data pipeline for CSV processing, analysis, and storage

Java
Spring Boot
MySQL

🚀 Key Features
✔ Automated CSV Processing - Ingests and parses CSV files with dynamic header detection
✔ Database Storage - Stores raw CSV data in MySQL with metadata tracking (source file, upload timestamp)
✔ Statistical Analysis - Calculates mean, median, skewness, and kurtosis for numeric columns (Legacy)
✔ Data Visualization - Generates interactive histograms and box plots using Chart.js
✔ Extensible Architecture - Built with SOLID principles for easy feature additions

🛠️ Technology Stack
Backend: Java 17, Spring Boot 2.7

Database: MySQL 8.0 (Compatible with PostgreSQL/H2)

Frontend: Thymeleaf, Bootstrap 5, Chart.js

Build Tool: Maven

Design Patterns: Repository, Strategy, Factory Method, MVC

⚙️ Setup Instructions
Prerequisites
Java 17+

MySQL 8.0+

Maven 3.8+

Installation
Clone the repository:
git clone https://github.com/yourusername/etl-system.git

Configure database:
Update src/main/resources/application.properties:
spring.datasource.url=jdbc:mysql://localhost:3306/etl_system
spring.datasource.username=youruser
spring.datasource.password=yourpassword

Build and run:
mvn clean install
mvn spring-boot:run

Access the UI at:
http://localhost:8080

📂 Project Structure
markdown
src/
├── main/
│   ├── java/com/etl/
│   │   ├── config/       # Spring configuration
│   │   ├── controller/   # MVC Controllers (ETLController)
│   │   ├── entity/       # JPA entities (ProcessedData)
│   │   ├── repository/   # Database repositories
│   │   ├── service/      # Business logic layer
│   │   └── util/         # Utilities (CSVHelper)
│   └── resources/
│       ├── static/       # CSS/JS files
│       ├── templates/    # Thymeleaf HTML
│       └── application.properties
🔍 Design Highlights
Architecture
MVC Pattern: Separation of concerns between controllers, services, and views

Layered Design:

Web Layer: Handles HTTP requests/responses

Service Layer: Business logic and transaction management

Repository Layer: Database operations via Spring Data JPA

Key Design Patterns
Pattern	Implementation Example	Benefit
Repository	ProcessedDataRepository	Abstracts database operations
Strategy	DataAnalyzer implementations	Swappable analysis algorithms
Factory	DataAnalyzerFactory	Decouples object creation
📊 Sample Workflow
User uploads CSV via web interface

System parses file and validates structure

Data is analyzed (statistics calculated)

Results stored in MySQL with metadata

Visualizations rendered in browser
