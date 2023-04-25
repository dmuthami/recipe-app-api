# recipe-app-api

# linting

docker-compose run --rm app sh -c "flake8"

# Test

docker-compose run --rm app sh -c "python manage.py test"
docker-compose run --rm app sh -c "python manage.py wait_for_db"

# Create core app

docker-compose run --rm app sh -c "python manage.py startapp core"

# Create user app

docker-compose run --rm app sh -c "python manage.py startapp user"

# Migrations

docker-compose run --rm app sh -c "python manage.py makemigrations"

docker-compose run --rm app sh -c "python manage.py wait_for_db && python manage.py migrate"

# Create super user

docker-compose run --rm app sh -c "python manage.py createsuperuser"

# Volume

<!-- List all volumes -->

docker volume ls

<!-- clear data in our database -->

docker volume rm recipe-app-api_dev-db-data

# Run server

docker-compose up
