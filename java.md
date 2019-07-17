# java

- get pid:
jps

- Request a thread dump from the JVM
jstack -l <pid>

- heap dump 
sudo -u ubuntu jmap -dump:format=b,file=/tmp/dump.bin <pid>