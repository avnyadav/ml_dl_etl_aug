

docker run -it -p 9870:9870 -p 8088:8088 -p 8080:8080 -p 18080:18080 -p 9000:9000 -p 8888:8888 -p 9864:9864 -p 8085:8085 -p 8793:8793 -p 8081:8081 -v E:\MLDL\bigdata\notebook:/root/ipynb -v E:\MLDL\bigdata\airflow:/home/airflow -v E:\MLDL\bigdata\data:/data --name mldl-spark-class spark-hadoop-airflow