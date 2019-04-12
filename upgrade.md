#### gsatsrv13.globoi.com ####

No servidor gstsrv13 execute os seguintes comandos na sequência:

```
# yum check-update
```

```
# rpm -qa | grep -i percona | sort
```
```
# systemctl stop mysql
```

```
# yum -y update
```

```
# systemctl reboot
```

#### gsatsrv12.globoi.com ####

No servidor gstsrv12 execute os seguintes comandos na sequência:

```
# yum check-update
```

```
# rpm -qa | grep -i percona | sort
```

```
# systemctl stop mysql
```

```
# yum -y update
```

```
# systemctl reboot
```

#### gsatsrv11.globoi.com ####

No servidor gstsrv11 execute os seguintes comandos na sequência:

```
# yum check-update
```

```
# rpm -qa | grep -i percona | sort
```

```
# systemctl stop mysql@bootstrap.service
```

```
# yum -y update
```

```
# systemctl reboot
```

#### gsatsrv11.globoi.com ####

```
# dmesg
```

```
# multipath -ll
```

```
# systemctl status -l multipathd
```

```
# systemctl status -l iscsid
```

```
# rpm -qa | grep -i percona | sort
```

```
# systemctl start mysql@bootstrap.service
```

```
# systemctl status -l mysql@bootstrap.service
```

```
# ps ax | grep -i mysql
```

#### gsatsrv12.globoi.com ####

```
# dmesg
```

```
# multipath -ll
```

```
# systemctl status -l multipathd
```

```
# systemctl status -l iscsid
```

```
# rpm -qa | grep -i percona | sort
```

```
# systemctl start mysql
```

```
# systemctl status -l mysql
```

```
# ps ax | grep -i mysql
```

#### gsatsrv13.globoi.com ####

```
# dmesg
```

```
# multipath -ll
```

```
# systemctl status -l multipathd
```

```
# systemctl status -l iscsid
```

```
# rpm -qa | grep -i percona | sort
```

```
# dmesg
```

```
# systemctl start mysql
```

```
# systemctl status -l mysql
```

```
# ps ax | grep -i mysql
```

Execute o comando abaixo para ter acesso ao status das informações do cluster
```
show variables like ‘%wsrep%’;
```

Os parâmetros importantes aqui são os seguintes:

*wsrep_local_state_comment*
*wsrep_incoming_addresses* 
*wsrep_cluster_conf_id*

```
mysql> show status like 'wsrep%';
+------------------------------+-------------------------------------------------------+
| Variable_name                | Value                                                 |
+------------------------------+-------------------------------------------------------+
| wsrep_local_state_uuid       | 51c60d63-4e89-11e6-8353-42c2375b74c3                  |
| wsrep_last_committed         | 911397980                                             |
| wsrep_local_state_comment    | Synced                                                |
| wsrep_incoming_addresses     | 10.129.96.11:3306,10.129.96.12:3306,10.129.96.13:3306 |
| wsrep_evs_state              | OPERATIONAL                                           |
| wsrep_gcomm_uuid             | 54cf4ddf-3746-11e8-a3cf-1f284a7d9411                  |
| wsrep_cluster_conf_id        | 11                                                    |
| wsrep_cluster_conf_id        | 3                                                     |
| wsrep_cluster_state_uuid     | 51c60d63-4e89-11e6-8353-42c2375b74c3                  |
| wsrep_cluster_status         | Primary                                               |
| wsrep_connected              | ON                                                    |
| wsrep_local_index            | 2                                                     |
| wsrep_provider_name          | Galera                                                |
| wsrep_ready                  | ON                                                    |
+------------------------------+-------------------------------------------------------+
59 rows in set (0.00 sec)
```


