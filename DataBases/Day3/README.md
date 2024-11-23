
# Build and Run the Docker Container

1. **Build the Docker Image:**

```bash
docker-compose build
```

2. **Run the Docker Container:**

```bash
docker-compose run ruby-app
```

This will start the container, run the necessary Rake tasks (such as `db:create`, `db:migrate`, and `db:seed`), and run your tests.

### Step 4: Test Your Application

To run the application, use the following command:

```bash
docker-compose run ruby-app rake db:create db:migrate db:seed
docker-compose run ruby-app rake specs
```

This will run the migrations, seed the database, and run the specs inside the Docker container.
