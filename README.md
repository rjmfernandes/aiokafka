# AioKafka small guide

This small guide is based on:
- https://aiokafka.readthedocs.io/en/stable/index.html
- https://github.com/aio-libs/aiokafka

## Installation

```shell
virtualenv env

source env/bin/activate

pip install aiokafka

confluent local kafka start
confluent services schema-registry start
```

Create topic:

```shell
confluent local kafka topic create my_topic
```

Update [consumer.py](./consumer.py) with plaintext port:

```shell
chmod u+x consumer.py

./consumer.py 
```

Update [producer.py](./producer.py) with plaintext port and in another shell run:

```shell
virtualenv env
source env/bin/activate
pip install aiokafka
```

```shell
chmod u+x producer.py

./producer.py 
```

# Cleanup

```shell
confluent local services stop
confluent local kafka stop
deactivate
```


