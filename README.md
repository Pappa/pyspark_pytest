# Pyspark Pytest

Testing pyspark code with pytest

## Build docker container

    docker build -t "pyspark" .

## Run tests

    docker run -it -v $(pwd):/app pyspark bash -c 'pytest'

## Run marked tests

    docker run -it -v $(pwd):/app pyspark bash -c 'pytest -m "is_spark"'