# Finance Management Application
 
A Java-based desktop application for managing personal finances with secure user authentication and database integration.
 
## Features
 
- **User Authentication**: Secure login and registration system
- **Session Management**: Persistent user sessions using Singleton pattern
- **Database Integration**: JDBC connectivity with SQL injection prevention
- **Data Access Layer**: DAO pattern for clean database operations
 
## Technologies Used
 
- **Java**: Core programming language
- **JDBC**: Database connectivity
- **SQL**: Database operations
- **Design Patterns**: Singleton, DAO (Data Access Object)
 
## Project Structure
 
```
src/main/java/com/finance/
├── Main.java              # Application entry point
├── UserDAO.java           # Database operations for users
├── UserSession.java       # Session management (Singleton)
├── LoginPage.java         # Login interface
├── RegisterPage.java      # Registration interface
└── DBConnection.java      # Database connection management
```
 
## Key Components
 
### UserDAO
- Handles user authentication and registration
- Implements secure database operations using PreparedStatement
- Prevents SQL injection attacks
- Methods: `authenticateUser()`, `registerUser()`, `userExists()`
 
### UserSession
- Singleton pattern implementation for session management
- Tracks logged-in user state across the application
- Methods: `getInstance()`, `login()`, `logout()`, `isLoggedIn()`
 
### Database Security
- PreparedStatement for parameterized queries
- Proper resource management with try-with-resources
- Connection cleanup in finally blocks
 
## Installation
 
1. Clone the repository
2. Set up your database and update connection details in `DBConnection.java`
3. Compile and run the application
 
## Usage
 
1. **Register**: Create a new user account with full name, username, password, and email
2. **Login**: Authenticate with your credentials
3. **Session**: User session remains active until logout
 
## Security Features
 
- SQL injection prevention using PreparedStatement
- Secure password handling
- Session management with proper cleanup
- Database connection pooling
 
## Design Patterns Implemented
 
- **Singleton Pattern**: UserSession for global session management
- **DAO Pattern**: UserDAO for database abstraction
- **Factory Pattern**: DBConnection for database connection creation
 
## Future Enhancements
 
- Password encryption
- Account recovery functionality
- Financial transaction management
- Data export features
- Multi-user support with roles# Personal-Finance_tracker
