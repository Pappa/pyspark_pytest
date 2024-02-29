# Pyspark Pytest

Testing pyspark code with pytest

## Build docker container

    docker build -t "test_pyspark" .

## Run tests with coverage

    docker run -it -v $(pwd):/app test_pyspark bash -c 'pytest --cov --cov-report=xml'

## Run marked tests with coverage

    docker run -it -v $(pwd):/app test_pyspark bash -c 'pytest -m "is_spark" --cov --cov-report=xml'

## Build and run with compose

    docker compose run --build spark bash -c 'pytest -m "not is_spark" --cov --cov-report=xml'