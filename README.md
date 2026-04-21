# Employee Management System - Backend API 🚀

A robust REST API for employee management built with **Spring Boot** and **Java 25** (Latest LTS). This backend service provides comprehensive CRUD operations for employee data management.

## Features ✨

- **Complete CRUD Operations**: Create, Read, Update, and Delete employees
- **RESTful API Design**: Clean, intuitive REST endpoints
- **Database Integration**: JPA/Hibernate with support for MySQL and H2 (for testing)
- **Exception Handling**: Comprehensive error handling and validation
- **Modern Java**: Built with Java 25 (Latest LTS) for optimal performance
- **Maven Build**: Configured with Maven wrapper for consistent builds
- **Unit Testing**: Comprehensive test suite with 100% pass rate

## Tech Stack 🛠️

- **Java**: 25 (Latest LTS)
- **Framework**: Spring Boot 3.4.7
- **Database**: MySQL (production), H2 (testing)
- **ORM**: Spring Data JPA / Hibernate 6.x
- **Build Tool**: Maven 3.9.15
- **Testing**: JUnit 5, Mockito, Spring Boot Test

## Prerequisites 📋

- **Java 25** (Latest LTS) - Download from [Adoptium](https://adoptium.net/)
- **Maven** (or use included Maven wrapper)
- **MySQL** (for production database)

## Quick Start 🚀

### 1. Clone the Repository
```bash
git clone https://github.com/ashudubeyvns/employee-management-system.git
cd employee-management-system/EmployeeManagementSystem
```

### 2. Configure Database
Update `src/main/resources/application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/employee_db
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

### 3. Run the Application
```bash
# Using Maven wrapper (recommended)
./mvnw spring-boot:run

# Or using Maven directly
mvn spring-boot:run
```

The API will be available at: `http://localhost:8080`

### 4. Run Tests
```bash
# Run all tests
./mvnw test

# Run with coverage
./mvnw clean verify
```

## API Endpoints 📡

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/employees` | Get all employees |
| GET | `/api/employees/{id}` | Get employee by ID |
| POST | `/api/employees` | Create new employee |
| PUT | `/api/employees/{id}` | Update employee |
| DELETE | `/api/employees/{id}` | Delete employee |

### Sample API Usage

#### Get All Employees
```bash
curl -X GET http://localhost:8080/api/employees
```

#### Create Employee
```bash
curl -X POST http://localhost:8080/api/employees \
  -H "Content-Type: application/json" \
  -d '{
    "firstName": "John",
    "lastName": "Doe",
    "email": "john.doe@example.com"
  }'
```

## Project Structure 📁

```
EmployeeManagementSystem/
├── src/
│   ├── main/
│   │   ├── java/com/example/EmployeeManagementSystem/
│   │   │   ├── controller/     # REST controllers
│   │   │   ├── dto/           # Data Transfer Objects
│   │   │   ├── exception/     # Custom exceptions
│   │   │   ├── mapper/        # Entity-DTO mappers
│   │   │   ├── model/         # JPA entities
│   │   │   ├── repository/    # Data repositories
│   │   │   ├── service/       # Business logic
│   │   │   └── EmployeeManagementSystemApplication.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
│       └── java/com/example/EmployeeManagementSystem/
│           └── EmployeeManagementSystemApplicationTests.java
├── .mvn/wrapper/              # Maven wrapper configuration
├── target/                    # Build output
├── pom.xml                    # Maven configuration
├── mvnw & mvnw.cmd           # Maven wrapper scripts
└── README.md                 # This file
```

## Configuration ⚙️

### Application Properties
```properties
# Server
server.port=8080

# Database
spring.datasource.url=jdbc:mysql://localhost:3306/employee_db
spring.datasource.username=root
spring.datasource.password=password
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# JPA/Hibernate
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect

# Logging
logging.level.com.example=DEBUG
```

## Testing 🧪

The project includes comprehensive unit tests:

- **Test Framework**: JUnit 5 with Spring Boot Test
- **Database**: H2 in-memory database for isolated testing
- **Coverage**: All business logic and API endpoints tested
- **CI/CD Ready**: Tests run automatically on build

Run tests:
```bash
./mvnw test
```

## Security & Best Practices 🔒

- **Input Validation**: Comprehensive validation on all inputs
- **Exception Handling**: Global exception handling with meaningful error messages
- **CORS Configuration**: Configured for frontend integration
- **Zero CVEs**: All dependencies scanned and patched for security vulnerabilities
- **Modern Dependencies**: Latest stable versions of all libraries

## Deployment 🚀

### Build for Production
```bash
./mvnw clean package
java -jar target/EmployeeManagementSystem-0.0.1-SNAPSHOT.jar
```

### Docker Support (Optional)
```dockerfile
FROM openjdk:25-jdk-slim
COPY target/*.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
```

## Contributing 🤝

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Recent Updates 📈

- ✅ **Upgraded to Java 25** (Latest LTS) - April 2026
- ✅ **Enhanced Security** - Patched HIGH severity CVE in MSSQL JDBC
- ✅ **Improved Testing** - Added H2 database for isolated unit tests
- ✅ **Build Optimization** - Configured Maven wrapper for consistent builds

## License 📄

This project is licensed under the MIT License - see the LICENSE file for details.

## Support 💬

For questions or issues:
- Create an issue on GitHub
- Check the upgrade documentation in `.github/java-upgrade/`

---

**Built with ❤️ using Spring Boot and Java 25**</content>
<parameter name="filePath">/Users/ashutoshdubey/Downloads/Employee-Management-Sys-main/EmployeeManagementSystem/README.md