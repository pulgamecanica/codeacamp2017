
---

# **Ruby-Based Projects: Day 1 to Day 4**

## **Index**

1. [Day 1: Raw SQL](#day-1)
2. [Day 2: Chef Application with ActiveRecord Integration](#day-2)
3. [Day 3: User Management Application with CSV Import](#day-3)
4. [Day 4: MVC-based Applications (Marathon Game & Task Reminder)](#day-4)
5. [Conclusion](#conclusion)
6. [Technologies Used](#technologies-used)

---

### <a name="day-1"></a> **1. Day 1: Raw SQL**

On Day 1, we learnt SQL and how it handles databases.

There are two examples:

```
├── Modificando_una_base_de_datos.rb
└── preguntale_a_la_base_de_Datos.bd.rb
```

---

### <a name="day-2"></a> **2. Day 2: Simple Ruby Database Manipulation (Chef Database)**

#### **Project Overview**
On Day 2, we built a basic Ruby application that connects to an SQLite database and allows CRUD (Create, Read, Update, Delete) operations for `chefs`. The database stores information about chefs such as their name, email, phone, and birthday.

#### **File Structure**
```
├── Juntando_fuerzas.rb
└── Sitio_De_Recetas_De_Comida.xml
```

#### **Key Components**
- **Juntando_fuerzas.rb**:
  - Used SQLite3 to create a database for chefs.
  - Implemented methods to insert, find, delete, and update records in the `chefs` table.
  - A `seed` method to pre-populate the database with sample chef data.
  
- **Sitio_De_Recetas_De_Comida.xml**:
  - Generated using a tool to visualize the database schema and help design relationships between tables in XML format.

#### **Methods Implemented**
- `initialize`: Initializes an instance of a `Chef` object and inserts it into the database.
- `self.all`: Retrieves all chefs from the database.
- `self.where`: Retrieves chefs based on a field value.
- `self.find`: Finds a chef by their ID.
- `self.delete`: Deletes a chef by their ID.
- `self.create_table`: Creates the `chefs` table in the database.
- `self.seed`: Seeds the database with initial data.

---

### <a name="day-3"></a> **3. Day 3: User Management Application with CSV Import**

#### **Project Overview**
On Day 3, we built a **User Management Application** that reads user data from a CSV file and imports it into an SQLite database using **ActiveRecord**.

#### **Key Components**
- **User Model**: Implements attributes like `first_name`, `last_name`, `gender`, `birthday`, `email`, and `phone`. It also includes validation rules (e.g., email format and age validation).
- **CSV Import**: Uses the `UserWriter` class to generate a CSV file with random user data.
- **Seeds**: The `UserSeeds.import` method reads from the CSV file and imports data into the database.
- **Rakefile**: Includes tasks for database creation, migration, seeding, and running tests.

#### **Features**
- Data validation for the `email` format and the `age` of users (must be greater than or equal to 18).
- Phone numbers are cleaned before validation.
- CSV file generation with randomly generated user data using the `Faker` gem.

---

### <a name="day-4"></a> **4. Day 4: MVC-based Applications (Marathon Game & Task Reminder)**

#### **Project Overview**
On Day 4, we implemented two MVC-based applications:
1. **Marathon Game** – A simple question-answer game where users can answer questions and track their score.
2. **Task Reminder** – A task management app to help users create, view, and complete tasks.


#### **Key Components**

- **Game Model** (`task.rb`):
  - Represents a game where each game has a question and an answer.
  - Tracks the score based on user input.

- **Task Model** (`task.rb`):
  - Represents a task with attributes like `name`, `due_date`, and `completed`.

- **Game Controller** (`task_controller.rb`):
  - Handles game logic such as displaying questions, receiving user answers, and calculating scores.

- **Task Controller** (`task_controller.rb`):
  - Manages tasks like creating new tasks, viewing tasks, and marking them as complete.

- **Views** (`tasks_view` and `tasks_view` directories for each app):
  - Contains rb files for displaying the game questions and task list.

#### **Features**
- **Marathon Game**:
  - Displays a question and checks if the user’s answer is correct.
  - Tracks and displays the user’s score.

- **Task Reminder**:
  - Allows users to create, update, and delete tasks.
  - Marks tasks as complete and displays them in a list.

- **MVC Architecture**:
  - The application follows the MVC pattern, separating concerns into models, views, and controllers.

---

### <a name="conclusion"></a> **5. Conclusion**

The projects from **Day 1** to **Day 4** showcase the gradual evolution of your Ruby development skills. Initially starting with database manipulation and basic CRUD operations, you then moved to using **ActiveRecord** to simplify database operations. Later, you expanded your knowledge to work with CSV files and validations. On Day 4, you implemented the **MVC architecture** to build more complex, interactive applications like the **Marathon Game** and **Task Reminder**.

This progression demonstrates not only the technical skills required to work with Ruby and ActiveRecord but also the organizational skills necessary to manage a growing project using best practices like MVC.

---

### <a name="technologies-used"></a> **6. Technologies Used**
- Ruby
- ActiveRecord
- SQLite3
- CSV
- RSpec for testing

---

