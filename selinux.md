Selinux
``` 
# getenforce
```
```
# setenforce 1
```
```
# getenforce
```

```
# sepolicy network -t mysqld_port_t
```
```
# yum -y install libsemanage policycoreutils-python setools-console policycoreutils-devel
```
```
# sepolicy network -t mysqld_port_t
```
```
# semanage port -m -t mysqld_port_t -p tcp 4444
```
```
# semanage port -m -t mysqld_port_t -p tcp 4567
```
```
# semanage port -m -t mysqld_port_t -p tcp 4568
```
```
# semanage port -a -t mysqld_port_t -p tcp 4568
```
```
# sepolicy network -t mysqld_port_t
```
```
# systemctl start mysql
```
Firewalld


```
# firewall-cmd --permanent --get-zones
```
```
# firewall-cmd --zone=public --list-all
```
```
# firewall-cmd --zone=public --permanent --add-port=3306/tcp
# firewall-cmd --zone=public --permanent --add-port=4444/tcp
# firewall-cmd --zone=public --permanent --add-port=4567/tcp
# firewall-cmd --zone=public --permanent --add-port=4568/tcp
```
```
# firewall-cmd --zone=public --permanent --add-port=3306/udp
# firewall-cmd --zone=public --permanent --add-port=4444/udp
# firewall-cmd --zone=public --permanent --add-port=4567/udp
# firewall-cmd --zone=public --permanent --add-port=4568/udp
```
```
# firewall-cmd --zone=public --list-all
```
```
# firewall-cmd --reload
```
```
# firewall-cmd --zone=public --list-all
```
```
# firewall-cmd --permanent --zone=public --add-source=192.168.56.0/24
```
```
# firewall-cmd --reload
```
```
# firewall-cmd --zone=public --list-all
```
```
cp -vrfp /var/lib/mysql /mnt/data/
```
```
```
cd /mnt/data/
```
```
cp -vrfp /var/lib/mysql /mnt/data/
```
```
cd /mnt/data/
```
```
ll
cd mysql/
ls
ll
clear
cd
```
cd /var/log/mysql/
```
```
echo " " > linuxacademy01-error.log
```
```
systemctl start mysql@bootstrap.service
```
```
less linuxacademy01-error.log
```
```
stat /mnt/data/mysql/grastate.dat
```
```
stat /var/lib/mysql/grastate.dat
```
```
stat /var/lib/mysql
```
```
stat /mnt/data/mysql/
```
```
cd
```
```
clear
```
```
semanage fcontext -a -t mysqld_db_t "/mnt/data/mysql(/.*)?"
```
```
restorecon -Rv /mnt/data/mysql/
```
```
clear
```
```
stat /var/lib/mysql
```
```
stat /mnt/data/mysql/
```
```
clear
```
```
cd /var/log/mysql/
```
```
ls
```
```
echo " " > linuxacademy01-error.log
```
```
systemctl start mysql@bootstrap.service
```
```
mkdir /dev/shm/mysql
```
```
chown -vR mysql:mysql /dev/shm/mysql/
```
```
stat /dev/shm/mysql/
```
```
semanage fcontext -a -t mysqld_db_t "/dev/shm/mysql(/.*)?"
```
```
restorecon -vR /dev/shm/mysql/
```
```
ls -lZ /dev/shm
```
```
ls -lZ /dev/shm/mysql
```



