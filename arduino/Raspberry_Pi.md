### rulare automata java
vezi 

http://askubuntu.com/questions/99232/how-to-make-a-jar-file-run-on-startup-and-when-you-log-out 
http://raspberrypi.stackexchange.com/questions/13034/executing-a-jar-file-when-raspberry-boots-up

- am pus fisierul jar si fisierele de configurare in directorul in /opt/openhab
- am pus owner:group openhab:openhab
- in /usr/local/bin am creat scripturi pt pornire si oprire program
- (nu stiu daca e bine) fisierele au owner:group root:staff si -rwxr-xr-x

opendoor-start.sh
```
#!/bin/bash
cd /opt/openhab
java -jar /opt/openhab/home-0.0.1.jar
```
opendoor-stop.sh (nu stiu exact ce face si vrea sa opreasca 2 procese; pe al doilea nu il poate opri)
- cred ca al doilea este exact comanda care se da
```
#!/bin/bash
pid=`ps aux | grep home-0.0.1 | awk '{print $2}'`
kill -9 $pid
```
acum cred ca puteam sa pun in crontab intrarea 
```
@reboot /usr/local/bin/opendoor-start.sh
```
dar am pus in /etc/init.d
```
start)
stop)
```
si apoi am rulat comanda
```
update-rc.d opendoor defaults 
```
