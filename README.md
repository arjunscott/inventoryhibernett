# Hibernate Supermarket (MySQL + Maven)

This is a minimal, runnable Hibernate project connected to MySQL.

## Prerequisites
- Java 17 installed
- Maven installed
- MySQL Server running locally with user `root` (change password in `src/main/resources/hibernate.cfg.xml` if needed)

## Setup
1. Create a database (optional, auto created via URL parameter):
   ```sql
   CREATE DATABASE IF NOT EXISTS supermarket;
   ```
2. Update DB credentials in `src/main/resources/hibernate.cfg.xml` if your MySQL user/password differ.

## Build
```bash
mvn -q -e -DskipTests package
```

This creates a fat JAR with all dependencies at:
```
target/hibernateSupermarkett-1.0-SNAPSHOT-shaded.jar
```

## Run
```bash
java -jar target/hibernateSupermarkett-1.0-SNAPSHOT-shaded.jar
```

You should see SQL logs and CRUD demo output.
