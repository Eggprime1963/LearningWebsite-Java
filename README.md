# Learning Management System (LMS)

A comprehensive Java-based Learning Management System built with Jakarta EE, providing a platform for online education with course management, assignments, lectures, and student enrollment capabilities.

## 📚 Features

### 👨‍🎓 Student Features
- **User Registration & Authentication** - Secure account creation with role-based access
- **Course Enrollment** - Browse and enroll in available courses
- **Course Dashboard** - View enrolled courses with progress tracking
- **Lecture Access** - Watch video lectures and access course materials
- **Assignment Submission** - Submit assignments and view grades
- **Progress Tracking** - Monitor completion status across courses
- **Profile Management** - Update personal information and preferences

### 👨‍🏫 Teacher Features
- **Course Creation & Management** - Create, update, and delete courses
- **Lecture Management** - Upload video content and course materials
- **Assignment Creation** - Create assignments with due dates and descriptions
- **Student Management** - View enrolled students and their progress
- **Grade Management** - Review and grade student submissions
- **Course Analytics** - Track enrollment and completion statistics

### 🔧 Administrator Features
- **User Role Management** - Assign and update user roles
- **System Overview** - Monitor platform usage and activities
- **User Activity Tracking** - View login/logout times and session duration

## 🛠️ Technology Stack

### Backend
- **Java 11** - Core programming language
- **Jakarta EE 9.1** - Enterprise Java platform
- **Hibernate 5.6** - Object-Relational Mapping (ORM)
- **JPA 3.0** - Java Persistence API
- **Maven** - Build and dependency management

### Database
- **MySQL 8.0** - Primary database
- **Microsoft SQL Server** - Alternative database support

### Frontend
- **JSP (Jakarta Server Pages)** - Server-side rendering
- **JSTL** - JSP Standard Tag Library
- **Bootstrap** - Responsive UI framework
- **HTML5/CSS3** - Modern web standards

### Security & Authentication
- **BCrypt** - Password hashing
- **Google OAuth2** - Social authentication
- **Session Management** - Secure user sessions

## 🏗️ Project Structure

```
LearningWebsite-Java/
├── src/main/
│   ├── java/
│   │   ├── Controller/          # Servlet controllers
│   │   │   ├── AssignmentServlet.java
│   │   │   ├── CourseServlet.java
│   │   │   ├── LectureServlet.java
│   │   │   ├── LoginServlet.java
│   │   │   └── ...
│   │   ├── DAO/                 # Data Access Objects
│   │   │   ├── CourseDAO.java
│   │   │   ├── StudentDAO.java
│   │   │   ├── AssignmentDAO.java
│   │   │   └── ...
│   │   └── Model/               # Entity classes
│   │       ├── User.java
│   │       ├── Course.java
│   │       ├── Lecture.java
│   │       ├── Assignment.java
│   │       └── ...
│   ├── resources/
│   │   └── META-INF/
│   │       ├── persistence.xml  # JPA configuration
│   │       └── context.xml      # Database context
│   └── webapp/
│       ├── *.jsp               # JSP pages
│       ├── css/                # Stylesheets
│       ├── img/                # Images and assets
│       └── WEB-INF/
│           ├── web.xml         # Web application configuration
│           └── jsp/            # Protected JSP files
├── target/                     # Compiled classes
├── pom.xml                     # Maven configuration
└── *.sql                      # Database scripts
```

## 🗄️ Database Schema

The system uses a well-structured relational database with the following main entities:

- **Users** - Student, teacher, and admin accounts
- **Courses** - Course information and metadata
- **Lectures** - Video content and materials
- **Assignments** - Tasks and assessments
- **Submissions** - Student assignment submissions
- **Enrollments** - Student-course relationships
- **UserActivity** - Login/logout tracking

## 🚀 Getting Started

### Prerequisites

- **Java 11** or higher
- **Apache Maven 3.6+**
- **MySQL 8.0** or **Microsoft SQL Server**
- **Apache Tomcat 10** (or any Jakarta EE compatible server)
- **Git**

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Eggprime1963/LearningWebsite-Java.git
   cd LearningWebsite-Java
   ```

2. **Database Setup**
   ```bash
   # Create database using provided SQL scripts
   mysql -u root -p < learning_management.sql
   # or for MySQL specifically
   mysql -u root -p < learning_management-mysql.sql
   ```

3. **Configure Database Connection**
   
   Update `src/main/resources/META-INF/persistence.xml`:
   ```xml
   <property name="jakarta.persistence.jdbc.url" 
             value="jdbc:mysql://localhost:3306/learning_management"/>
   <property name="jakarta.persistence.jdbc.user" value="your_username"/>
   <property name="jakarta.persistence.jdbc.password" value="your_password"/>
   ```

4. **Build the Project**
   ```bash
   mvn clean compile
   ```

5. **Package as WAR**
   ```bash
   mvn package
   ```

6. **Deploy to Tomcat**
   - Copy `target/learning-platform-1.0.0.war` to your Tomcat `webapps` directory
   - Start Tomcat server
   - Access the application at `http://localhost:8080/learning-platform-1.0.0`

### Default Access

The system includes sample data with default accounts:
- **Admin**: Check the SQL files for admin credentials
- **Teacher**: Sample teacher accounts for testing
- **Student**: Sample student accounts for enrollment testing

## 📊 Key Features in Detail

### Course Management
- Create courses with thumbnails and descriptions
- Organize content into lectures and assignments
- Track student enrollment and progress
- Support for video content and downloadable materials

### Assignment System
- Create timed assignments with due dates
- File upload functionality for submissions
- Automated grading system
- Progress tracking and analytics

### User Authentication
- Traditional username/password authentication
- Google OAuth2 integration
- Role-based access control (Student/Teacher/Admin)
- Secure password hashing with BCrypt

### Progress Tracking
- Real-time progress calculation
- Completion percentages for courses
- Activity logging and duration tracking
- Enrollment status management

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Authors

- **Eggprime1963** - *Initial work* - [GitHub](https://github.com/Eggprime1963)

## 🙏 Acknowledgments

- Jakarta EE community for the robust enterprise framework
- Hibernate team for excellent ORM capabilities
- Bootstrap team for responsive UI components
- MySQL team for reliable database management

## 📞 Support

For support, please open an issue on GitHub or contact the development team.

---
*Built with ❤️ for modern online education*
