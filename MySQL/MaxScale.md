## MaxScale

##### Watch log
```
watch tail /path/to/log
```

Demo:
```
2021-08-09 10:34:58   info   : Pinging 'server2', idle for 301 seconds
2021-08-09 10:34:58   info   : (2) Response to COM_CHANGE_USER is OK, writing stored query                                                   
2021-08-09 10:35:23   info   : Pinging 'server1', idle for 301 seconds
2021-08-09 10:35:23   info   : (2) Response to COM_CHANGE_USER is OK, writing stored query                                                   
2021-08-09 10:35:46   info   : Server variables loaded from 'server2', next update in 600 seconds.                                           
2021-08-09 10:38:23   info   : Server variables loaded from 'server1', next update in 600 seconds.
2021-08-09 10:39:59   info   : Pinging 'server2', idle for 301 seconds
2021-08-09 10:39:59   info   : (2) Response to COM_CHANGE_USER is OK, writing stored query
2021-08-09 10:40:24   info   : Pinging 'server1', idle for 301 seconds
2021-08-09 10:40:24   info   : (2) Response to COM_CHANGE_USER is OK, writing stored query
2021-08-09 10:47:30   info   : (2) [readwritesplit] (Read-Write-Service) Reply complete, last reply from server2
2021-08-09 10:47:30   info   : (2) (Read-Write-Service) > Autocommit: [enabled], trx is [not open], cmd: (0x04) COM_FIELD_LIST, plen: 34, type: QUERY_TYPE_READ, stmt:
2021-08-09 10:47:30   info   : (2) [readwritesplit] (Read-Write-Service) Route query to slave: server2 <
2021-08-09 10:47:30   info   : (2) [readwritesplit] (Read-Write-Service) Reply complete, last reply from server2
2021-08-09 10:47:30   info   : (2) (Read-Write-Service) > Autocommit: [enabled], trx is [not open], cmd: (0x04) COM_FIELD_LIST, plen: 43, type: QUERY_TYPE_READ, stmt:
2021-08-09 10:47:30   info   : (2) [readwritesplit] (Read-Write-Service) Route query to slave: server2 <
2021-08-09 10:47:30   info   : (2) [readwritesplit] (Read-Write-Service) Reply complete, last reply from server2
```