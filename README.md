# java-springboot-assignment
Here’s a set of **Java Spring Boot assignments** designed to mimic real-world tasks and challenges you might face during interviews. These assignments will help demonstrate your understanding of Spring Boot, REST APIs, database integration, and more.

---

### **1. Create a RESTful CRUD API**
**Task:**
Build a simple Spring Boot application to manage a list of "Books". Each book should have:
- `id` (UUID)
- `title`
- `author`
- `price`
- `publishedDate`

**Requirements:**
1. Create endpoints for:
   - Adding a book (`POST /books`)
   - Fetching all books (`GET /books`)
   - Fetching a book by `id` (`GET /books/{id}`)
   - Updating a book (`PUT /books/{id}`)
   - Deleting a book (`DELETE /books/{id}`)
2. Use an in-memory database (e.g., H2) for storing the books.
3. Validate inputs using `@Valid` and custom validation annotations.

---

### **2. Implement Pagination and Sorting**
**Task:**
Extend the CRUD API to support:
- Pagination (`GET /books?page=0&size=10`)
- Sorting (`GET /books?sort=title,asc` or `GET /books?sort=price,desc`).

---

### **3. Build a REST API with Relationships**
**Task:**
Build an API for a "Library Management System" with two entities:
1. **Library**:
   - `id`, `name`, `location`
2. **Book**:
   - `id`, `title`, `author`, `price`, `libraryId` (foreign key)

**Requirements:**
- Implement endpoints to:
  - Add a library and books to it.
  - Fetch all books in a library.
  - Delete a library and cascade-delete its books.
- Use a relational database (e.g., MySQL or PostgreSQL) with JPA.

---

### **4. Secure the REST API**
**Task:**
Add security to your API using Spring Security:
1. Use JWT for authentication.
2. Define two roles: `ADMIN` and `USER`.
3. Allow:
   - `ADMIN` to perform all operations.
   - `USER` to fetch books (`GET` endpoints only).

---

### **5. Exception Handling**
**Task:**
Implement global exception handling for the CRUD API:
1. Handle exceptions like:
   - `ResourceNotFoundException` for invalid IDs.
   - `MethodArgumentNotValidException` for validation errors.
   - Generic exceptions (`500 Internal Server Error`).
2. Return meaningful error responses with status codes and messages.

---

### **6. Caching with Spring Boot**
**Task:**
Optimize the CRUD API by adding caching for:
1. Fetching a book by ID.
2. Fetching all books.
3. Use Spring Boot's caching mechanism (`@Cacheable`, `@CacheEvict`) with an in-memory cache like **Caffeine** or **EhCache**.

---

### **7. Connect to an External API**
**Task:**
Create a Spring Boot application that consumes an external API (e.g., OpenWeatherMap API):
1. Fetch current weather data for a city.
2. Provide a REST endpoint (`GET /weather?city=cityName`) that fetches and returns the data.
3. Use `RestTemplate` or `WebClient` for API consumption.

---

### **8. File Upload and Download**
**Task:**
Build a REST API to handle file uploads and downloads:
1. Allow users to upload files to the server (`POST /files`).
2. Allow users to download files by filename (`GET /files/{filename}`).
3. Store files in the local file system or a database (e.g., as BLOBs).

---

### **9. Schedule Tasks with Spring Boot**
**Task:**
Create a Spring Boot application to:
1. Fetch weather data for a predefined list of cities every hour.
2. Store the data in a database.
3. Use Spring's `@Scheduled` annotation for task scheduling.

---

### **10. Develop a Messaging System**
**Task:**
Create a producer-consumer messaging application:
1. Use **RabbitMQ** or **Kafka**.
2. The producer sends a message containing book details (e.g., title, author).
3. The consumer listens to the queue/topic and stores the book details in the database.

---

### **11. Implement Spring Boot Actuator**
**Task:**
Add Spring Boot Actuator to monitor the application:
1. Enable health checks (`/actuator/health`) and metrics (`/actuator/metrics`).
2. Create a custom health check (e.g., verify database connectivity).

---

### **12. Test the Application**
**Task:**
Write unit and integration tests for your CRUD API:
1. Use **JUnit 5** and **MockMVC** for controller tests.
2. Test repository methods using an in-memory database (H2).
3. Ensure 100% test coverage for the service layer.

---

### **13. Deploy the Application**
**Task:**
Package and deploy your Spring Boot application:
1. Create a Dockerfile to containerize the app.
2. Write a `docker-compose.yml` file to run the app with a database (e.g., MySQL).
3. Deploy the app on a cloud service like AWS, GCP, or Heroku.

---

These assignments focus on building foundational and advanced skills in Spring Boot development and prepare you for real-world problems and interview scenarios. Let me know if you'd like detailed guidance or implementation for any of these!