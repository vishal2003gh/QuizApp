# markdown
# Quiz Application

A dynamic and interactive Quiz Application built using **Java** with a PostgreSQL database backend. The app allows users to test their knowledge across various topics, track scores, and enjoy a user-friendly interface.

# Features

**User Authentication** : Secure login and signup for personalized quiz sessions.
**Dynamic Questions**: Fetches questions from a PostgreSQL database.
**Interactive UI**: Built using Java Swing/JavaFX for a seamless experience.
**Real-Time Scoring**: Calculates and displays scores as users progress through the quiz.
**Result Summary**: Provides a detailed score breakdown at the end of the quiz.

# Tech Stack

### Backend
- **Java** (Core and JDBC)
- **PostgreSQL** for database management

### Frontend (Optional, for a hybrid setup)
- **HTML**, **CSS**, and **JavaScript** (if integrated with a web-based UI)

---

## Database Schema

### Tables
1. **`users`**  
   Stores user credentials.  
   | Column         | Type         | Description                 |
   |----------------|--------------|-----------------------------|
   | `user_id`      | SERIAL       | Primary Key                 |
   | `username`     | VARCHAR(50)  | Unique username             |
   | `password`     | VARCHAR(100) | Encrypted password          |

2. **`questions`**  
   Holds quiz questions and options.  
   | Column         | Type         | Description                 |
   |----------------|--------------|-----------------------------|
   | `question_id`  | SERIAL       | Primary Key                 |
   | `question_text`| TEXT         | Quiz question               |
   | `option1`      | TEXT         | First option                |
   | `option2`      | TEXT         | Second option               |
   | `option3`      | TEXT         | Third option                |
   | `option4`      | TEXT         | Fourth option               |
   | `correct_option`| INT         | Index of the correct answer |

3. **`user_scores`**  
   Tracks user scores for completed quizzes.  
   | Column         | Type         | Description                 |
   |----------------|--------------|-----------------------------|
   | `score_id`     | SERIAL       | Primary Key                 |
   | `user_id`      | INT          | Foreign Key (users.user_id) |
   | `score`        | INT          | User's score                |

---

## How to Run the Project

1. **Clone the Repository**
   ```bash
   git clone https://github.com/vishal200gh/quiz-application.git
   cd quiz-application
   ```

2. **Set Up the Database**
   - Install PostgreSQL and create a database named `quizapp`.
   - Execute the SQL script provided in the `database` folder to create tables and seed data.

3. **Configure Database Credentials**
   - Update the database connection details in `DatabaseConnection.java`:
     ```java
    
   4. **Compile and Run**
   - Compile the Java files:
     ```bash
     javac -cp .:postgresql-42.6.0.jar *.java
     ```
   - Run the application:
     ```bash
     java -cp .:postgresql-42.6.0.jar Main
     ```

## Future Enhancements

- Add support for quiz categories and difficulty levels.
- Implement a leaderboard system to foster competition.
- Introduce API integration for fetching quiz questions dynamically.
- Enhance the UI using web technologies like React.js or Vue.js.
- 
### **How to Customize:**
1. Replace **yourusername** with your GitHub username.
2. Add your **email** or any preferred contact method.
3. Include your **SQL script** in the `database` folder if you plan to share it.
