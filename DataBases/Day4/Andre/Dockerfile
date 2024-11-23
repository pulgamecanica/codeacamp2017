# Use a basic Ruby image as the base (you can choose a different one if needed)
FROM ruby:2.7

# Install required packages for building SQLite3 from source, including unzip
RUN apt-get update -qq && apt-get install -y \
    build-essential \
    wget \
    unzip \
    tcl \
    && rm -rf /var/lib/apt/lists/*

# Download and install SQLite 3.18.0 from the provided link
RUN wget https://www.sqlite.org/src/zip/6a378c29/SQLite-6a378c29.zip && \
    unzip SQLite-6a378c29.zip && \
    cd SQLite-6a378c29 && \
    ./configure && \
    make && \
    make install && \
    cd .. && \
    rm -rf SQLite-6a378c29.zip SQLite-6a378c29

# Verify SQLite version
RUN sqlite3 --version

# Set working directory for the Ruby app
WORKDIR /app

# Copy Gemfile and Gemfile.lock for bundle install
COPY Gemfile ./

# Install Ruby gems
RUN bundle install

# Copy the rest of the application code
COPY . .

# Set the default command to run the Rake tasks
CMD ["bash"]
