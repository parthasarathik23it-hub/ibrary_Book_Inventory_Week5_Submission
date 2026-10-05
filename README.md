# Library Book Inventory System - Week 5

## Integration, Deployment, and Documentation

This final-week version integrates the refactored Java CLI application from Week 4 into one deployable application. It includes the model, validation utility, inventory service, CLI entry point, JUnit tests, deployment scripts, packaging configuration, and developer documentation.

## Project Structure

```text
Library_Book_Inventory_Week5/
├── src/main/java/com/partha/library/
│   ├── Main.java
│   ├── model/Book.java
│   ├── service/BookManager.java
│   └── util/InputValidator.java
├── src/test/java/com/partha/library/service/BookManagerTest.java
├── deployment/
│   ├── build.sh
│   ├── build.bat
│   ├── run.sh
│   └── run.bat
├── docs/
│   ├── Week_4_Refactoring_Summary.md
│   └── Week_5_Developer_Documentation.md
├── dist/
├── pom.xml
├── README.md
└── SAMPLE_RUN.txt
```

## Technologies

- Java 17+
- Maven 3+
- JUnit 5 for unit testing
- Java Collections (`LinkedHashMap`, `List`)
- Executable JAR packaging

## Functional Modules

1. **Book model** - stores ISBN, title, author, and quantity.
2. **Input validation** - centralizes text, ISBN, and quantity validation.
3. **Book manager** - implements add, view, find, update, delete, and count operations.
4. **CLI** - connects user input to the service layer.
5. **Tests** - verifies CRUD operations, validation, case-insensitive ISBN handling, and collection protection.

## Deployment Notes

The application is intentionally a self-contained command-line Java application. It does not require a database or external runtime service. A deployment consists of the JAR plus a compatible JRE/JDK. The application keeps inventory in memory, so restarting the process resets the data to the sample/default runtime state.

See `docs/Week_5_Developer_Documentation.md` for the complete handover guide.
