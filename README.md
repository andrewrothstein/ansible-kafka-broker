andrewrothstein.kafka-broker
=========
[![Build Status](https://travis-ci.org/andrewrothstein/ansible-kafka-broker.svg?branch=master)](https://travis-ci.org/andrewrothstein/ansible-kafka-broker)

Install a [Kafka](https://kafka.apache.org/) broker. Assumes access to a ZooKeeper quorum.

Requirements
------------

See [meta/main.yml](meta/main.yml). Assumes a running ZooKeeper cluster.

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

See [meta/main.yml](meta/main.yml)

Example Playbook
----------------

inventory.ini
```ini
[zookeeper-quorum]
zk-host[1:3]

[kafka-broker]
kb-host1 kafka_broker_id=1
kb-host2 kafka_broker_id=2
kb-host3 kafka_broker_id=3
...
```

```yml
- hosts: kafka-broker
  roles:
    - andrewrothstein.kafka-broker
```

License
-------

MIT

Author Information
------------------

Andrew Rothstein <andrew.rothstein@gmail.com>
