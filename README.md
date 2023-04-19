# recipe-app-api

# linting

docker-compose run --rm app sh -c "flake8"

# Test

docker-compose run --rm app sh -c "python manage.py test"
