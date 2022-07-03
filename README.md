

[DockerHubSparkHadoopAirflow](https://hub.docker.com/r/avnish327030/spark-hadoop-airflow)

"E:\MLDL\bigdata" has to be replaced with output of cd command

```
docker run -it -p 9870:9870 -p 8088:8088 -p 8080:8080 -p 18080:18080 -p 9000:9000 -p 8888:8888 -p 9864:9864 -p 8085:8085 -p 8793:8793 -p 8081:8081 -v E:\MLDL\bigdata\notebook:/root/ipynb -v E:\MLDL\bigdata\airflow:/home/airflow -v E:\MLDL\bigdata\data:/data --name mldl-spark-class spark-hadoop-airflow
```

[Name Node](http://localhost:9870/)
[Airflow](http://localhost:8085/)
[Hadoop Data Node](http://localhost:9864/)
[Jupyter lab](http://localhost:8888/)
[Hadoop Cluster](http://localhost:8088/)
[Spark Master](http://localhost:8080/)



To List docker images
```
docker images
```

To list all running container
```
docker ps
```

To Build docker images
Note: We must have a Dockerfile in current directory 
```
docker build -t image_name:tag_name .
```

to stop running container
```
docker stop container_id
```

To start stop container
```
docker start container_name
```

```
airflow user: admin
airflow pass: airflow
```

To setup in linux system
```
PROJECT_DIR=$(pwd)
```
```
docker run -it \
    -p 9870:9870 \
    -p 8088:8088 \
    -p 8080:8080 \
    -p 18080:18080 \
    -p 9000:9000 \
    -p 8888:8888 \
    -p 9864:9864 \
    -p 8085:8085 \
    -p 8793:8793 \
    -p 8081:8081 \
    -v $PROJECT_DIR/notebook:/root/ipynb \
    -v $PROJECT_DIR/airflow:/home/airflow \
    -v $PROJECT_DIR/data:/data \
    spark-hadoop-airflow
```