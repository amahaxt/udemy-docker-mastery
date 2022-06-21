# create your custom drupal image here, based of official drupal

# Drupal 9.3.13
# Note: if it fails to build, try the latest 9 branch (drupal:9)
FROM drupal:9.3.13

# Run apt package manager command to install git:
RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*

# Set working directory to /var/www/html/themes
WORKDIR /var/www/html/themes

# Use the git clone command to clone the branch for the required theme
RUN git clone --branch 8.x-4.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

# Change the working directory back to the default
WORKDIR /var/www/html