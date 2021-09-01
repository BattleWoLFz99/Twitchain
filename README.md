# Twitchain

Initial Vagrant firstly

You need to run celery manually after branch 38 (check settings.py file)
```
celery -A twitter worker -l INFO
```
You need to setup HBase manually after branch 41
```
sudo bash bin/start-hbase.sh
```
You also need HBase thrift
``````
bin/hbase-daemon.sh start thrift
```