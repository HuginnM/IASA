# IASA
Loaded systems labs
***
Team (KA-03MP)
* Sobol
* Kozak
***
Lab 1 (Docker)
***
service docker start

*Task1 :
cd Docker/Task1
docker-compose up

*Task2 :
cd docker_lab/Task2
docker-compose up

*Task3 :
cd docker_lab/Task3
docker-compose up

*Task4 :

cd docker_lab/Task4
docker-compose up --scale json_server=3 --scale lite_server=3

*Task5 :
cd docker_lab/Task5
cat results.txt
***
Lab 2 (Jmeter)
***
task1.jmx -> task1.csv
task2.jmx -> task2.csv
task3.jmx -> task3.csv
task4.jmx -> task4.csv
***
Lab 3 (Mongo)
***
docker-compose up -d
sh init_rs.sh
(wait several seconds)
docker-compose exec router01 sh -c “mongo < .scripts/init-router.js”
run all generate_data.ipynb
cp mongo_lab/rides.csv mongo_lab/data/
sh import_and_query_data.sh
docker-compose down -v --rmi all --remove-orphans
***
Lab 4 (Hadoop)
***
Hadoop.pdf - step by step protocol
ProcessUnits.java - fixed Java code
result.txt - results of requests (step 10)
sample.txt - input data for requests
***
Lab 5 (Spark)
***
Correctly install spark (https://phoenixnap.com/kb/install-spark-on-ubuntu)
start-master.sh --webui-port 8001
apt install python3-pip
pip3 install pyspark, geopy, faker, numpy
download London.csv
spark-submit data_generation.py
spark-submit main.py
***