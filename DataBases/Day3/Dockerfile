# Use Ruby 2.2 based on Debian Buster (which is still supported)
FROM ruby:2.2

# Set the working directory to /app
WORKDIR /app

# Copy the Gemfile and Gemfile.lock into the container
COPY Gemfile ./

# Install the gems specified in the Gemfile
RUN bundle install

# Copy the rest of the application code
COPY . .

# Expose port 3000 for the application
EXPOSE 3000

# Set the default command to run the Rake tasks
CMD ["bash"]
