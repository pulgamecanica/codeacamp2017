# Use the official Ruby image as a base
FROM ruby:3.1

# Install SQLite3 and dependencies
RUN apt-get update && apt-get install -y \
    sqlite3 \
    libsqlite3-dev

# Set the working directory inside the container
WORKDIR /app

# Copy the Ruby program files into the container
COPY Juntando_fuerzas.rb /app

# Install any gems specified in the Gemfile
RUN gem install sqlite3

# Run the Ruby program by default
CMD ["ruby", "Juntando_fuerzas.rb"]
