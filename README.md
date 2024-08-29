# CONFIGURAÇÃO E DEMONSTRAÇÃO EM UM CLUSTER DISTRIBUÍDO COM APACHE FLINK 

## Visão Geral do Trabalho 

Este trabalho tem como objetivo configurar e demonstrar um ambiente de processamento distribuído utilizando o Apache Flink, implementando um cluster funcional em um ambiente virtual com o uso preferencial de Docker. A validação da configuração do cluster será realizada por meio da execução do código exemplo `WordCount.jar`, demonstrando a capacidade de processamento de dados distribuído do Apache Flink. 

## Códigos usados para rodar

```bash
sudo apt-get update

sudo apt-get install -y docker.io docker-compose

touch docker-compose.yml

sudo docker-compose up --scale taskmanager=3 -d

sudo docker exec -it jobmanager flink run -c org.apache.flink.examples.java.wordcount.WordCount /opt/flink/examples/batch/WordCount.jar 

sudo docker exec -it jobmanager flink run -p 3 -c org.apache.flink.examples.java.wordcount.WordCount /opt/flink/examples/batch/WordCount.jar
```

## Made by

João Victor Ferrareis Ribeiro

Miguel Malini
