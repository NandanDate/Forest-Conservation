Overview:
This project focuses on forest conservation through data collection, report generation, and user interaction. It consists of a React frontend, a Java Spring Boot backend, and a MongoDB database. The frontend and backend communicate via RESTful APIs. The project is structured to enable users to submit and access information about forests, submit reports, and manage user accounts securely.

Frontend (React) Features:
The frontend of the project is built using React and is responsible for handling user interaction and visual representation of the forest conservation system. Key features include:

User Interface (UI):

Clean and interactive UI for easy navigation.
Access to query data, submit reports, and view submitted reports.
User authentication screens, including login and registration.
Query System:

Users can search or query forest-related data, such as conservation efforts, environmental statistics, and reports.
Provides filters and sorting options to narrow down results.
Report Submission:

Users can submit new forest conservation reports, such as deforestation data, illegal activities, or wildlife conservation efforts.
The form supports validation and error handling to ensure accurate submissions.
User Account Management:

Users can register and log into the system, with role-based access control (admin, user).
User profiles with editable information, including passwords and personal data.
Data Visualization:

Charts and graphical representations of forest data, allowing users to understand statistics such as deforestation rates and wildlife population trends.
Integration with Backend:

Uses RESTful APIs to fetch and submit data to the backend (Java Spring Boot).
Secure data transfer with JWT (JSON Web Tokens) for authentication and access control.
Backend (Java Spring Boot):
The backend handles all the business logic, security, and database interactions of the forest conservation platform.

Core Structure:

Controllers:
QueryController, ReportController, and UserController handle REST API endpoints for queries, reports, and user management, respectively.
Services:
QueryService, ReportService, and UserService contain the business logic for each respective feature, such as processing user inputs, handling database interactions, and enforcing validation rules.
Repositories:
QueryRepository, ReportRepository, and UserRepository interact with MongoDB to store and retrieve information about forest queries, reports, and users.
Database (MongoDB):

Stores:
User Data: User profiles, authentication credentials (secured), and role-based access.
Query Data: Environmental data, conservation details, and research that users can query.
Reports: Reports on forest conditions, illegal activities, and other conservation efforts submitted by users.
The system uses MongoDB's schema flexibility to handle unstructured data like reports and dynamic forest conservation information.
Security:

JWT Authentication: Secure login and token-based authentication for users.
Role-based access control: Restricts certain functionalities based on the user's role (e.g., only admins can delete reports).
CORS Configuration: Allows the frontend (hosted separately) to communicate with the backend by enabling cross-origin resource sharing.
Key APIs:

User Authentication API: Handles login, registration, and token validation.
Query API: Allows users to submit forest data queries, with results fetched from MongoDB.
Report API: Provides endpoints for submitting, viewing, and managing forest reports.
Security and Cross-Origin Resource Sharing (CORS):

Managed by CorsConfig.java and SecurityConfig.java, ensuring secure communication between the frontend and backend with proper CORS policy setup.
Testing:

Basic unit and integration testing are implemented in ForestConservationApplicationTests.java to ensure the core functionalities like user authentication, queries, and report submission work as expected.
Workflow:
User Interaction:
A user interacts with the React frontend, submitting queries or reports, and views forest-related data.
Frontend & Backend Communication:

The frontend communicates with the backend via API calls, sending and receiving data (JSON) over HTTP. All API requests for secure operations are authenticated using JWT tokens.
Business Logic:

The backend processes the user requests, applies business logic (e.g., user authentication, query processing, or report validation), and interacts with MongoDB to fetch/store data.
Database Operations:

MongoDB handles the storage of large datasets related to forest conservation (such as reports, user profiles, and query results). The repositories interact with MongoDB collections to persist and retrieve this information.
Conclusion:
This forest conservation system provides a complete platform for users to engage with conservation data, submit reports, and interact with the forest environment in a meaningful way. The React frontend ensures a smooth user experience, while the Java Spring Boot backend enforces security, handles data processing, and provides a scalable architecture with MongoDB. The system is well-structured with security measures like JWT and CORS, ensuring safe and seamless communication between frontend and backend services.
