# Twitchain

Design Twitter!

Initial Vagrant firstly

Amazon S3 is used to store user avatar(branch 23)

Install redis after branch 32

Run celery manually after branch 38 (check settings.py file)
```
celery -A twitter worker -l INFO
```
Setup HBase manually after branch 41
```
sudo bash bin/start-hbase.sh
```
HBase thrift
```
bin/hbase-daemon.sh start thrift
```


Deploy to AWS EC2:

1. The demo uses AWS EC2 instance, t2.micro or below can only be used for testing.

2. Once the instance is up and running, modify /etc/ssh/sshd_config
   ```
   sudo vim /etc/ssh/sshd_config
   ```
   ```
   PubkeyAuthentication yes
   PasswordAuthentication yes
   ```
3. Edit inbound rules:
   
   Add Type TCP port 8000 Source 0.0.0.0/0
   
   Add Type HTTP Source 0.0.0.0/0

4. Pull the code, configurate MySQL/Redis/HBase/thrift

5. Deploy with Nginx is recommended


Sample: http://54.219.184.225/ (Work In Progress)

Users for Demo:
  username: test_user_1   
  password: testuser_testuser

  username: test_user_2  
  password: testuser_testuser
