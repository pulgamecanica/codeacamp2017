
---

# Chef Ruby SQLite3 Program

This project demonstrates how to use Ruby with SQLite3 inside a Docker container. It includes a class `Chef` that interacts with a SQLite database to perform operations like creating chefs, retrieving all chefs, filtering by specific fields, and more.

## Prerequisites

- **Docker** and **Docker Compose** installed on your machine. You can follow the official installation guide here: [Docker Installation](https://docs.docker.com/get-docker/).

## Project Structure

```
.
├── Dockerfile                # Dockerfile for setting up Ruby and SQLite3
├── docker-compose.yml        # Docker Compose configuration for running the program
├── Juntando_fuerzas.rb           # Ruby program with Chef class interacting with SQLite3
├── Sitio_De_Recetas_De_Comida.xml # XML DataBase Schema
└── README.md                 # This file
```

## Steps to Use the Program

Follow these steps to build and run the program in a Docker container:

### 1. Go to your local Repository

Clone this repository to your local machine:

```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Build the Docker Image

Run the following command to build the Docker image:

```bash
docker-compose build
```

This command will download the Ruby base image, install necessary dependencies (including SQLite3), and set up the environment.

### 3. Run the Program

Once the image is built, you can run the Ruby program inside the container. The program will create the `chefs` table, seed it with sample data, and then display all chefs from the database.

```bash
docker-compose run ruby
```

This will execute the `Juntando_fuerzas.rb` script and show the output in the terminal.

### 4. Interact with the Program

You can modify the `Juntando_fuerzas.rb` file to perform different actions on the SQLite database. Some of the available methods include:

- **Create a new Chef**:
  You can add new chefs by creating instances of the `Chef` class. For example:
  
  ```ruby
  Chef.new('John', 'Doe', '1985-05-14', 'john.doe@example.com', '1234567890')
  ```

- **Retrieve all chefs**:
  The `Chef.all` method will return all chefs stored in the database:
  
  ```ruby
  Chef.all
  ```

- **Find a chef by ID**:
  You can retrieve a chef by their unique ID:
  
  ```ruby
  Chef.find(1)
  ```

- **Delete a chef by ID**:
  To delete a chef by ID, use the `Chef.delete` method:
  
  ```ruby
  Chef.delete(1)
  ```

- **Filter chefs**:
  You can filter chefs by a specific field using the `Chef.where` method:
  
  ```ruby
  Chef.where('last_name', 'Adriá')
  ```

### 5. Accessing the Database

If you want to access or modify the SQLite database directly, you can connect to it using the SQLite3 command line tool. The database file is stored as `chefs.db` and is available in the `/app` directory inside the container.

To access the database inside the container:

```bash
docker-compose run ruby sqlite3 chefs.db
```

Once you're inside the SQLite shell, you can run SQL queries directly on the database.

### 6. Stopping the Services

To stop any running services and remove containers, run:

```bash
docker-compose down
```

This will stop the container and remove any associated resources.

---

## Conclusion

This project demonstrates how to set up Ruby with SQLite3 using Docker. You can use this setup to experiment with database operations without needing to install Ruby or SQLite3 directly on your local machine.

--- 
