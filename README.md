# recipe-app-api

# linting

docker-compose run --rm app sh -c "flake8"

# Test

docker-compose run --rm app sh -c "python manage.py test"
docker-compose run --rm app sh -c "python manage.py wait_for_db"

# Create core app

docker-compose run --rm app sh -c "python manage.py startapp core"
