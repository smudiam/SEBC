mysql> SHOW SLAVE STATUS \G;


		*************************** 1. row ***************************
               Slave_IO_State: Waiting for master to send event
                  Master_Host: ip-10-0-10-106.us-west-2.compute.internal
                  Master_User: repuser
                  Master_Port: 3306
                Connect_Retry: 60
              Master_Log_File: mysql_binary_log.000001
          Read_Master_Log_Pos: 4064
               Relay_Log_File: ip-10-0-10-122-relay-bin.000002
                Relay_Log_Pos: 1089
        Relay_Master_Log_File: mysql_binary_log.000001
             Slave_IO_Running: Yes
            Slave_SQL_Running: Yes
              Replicate_Do_DB:
          Replicate_Ignore_DB:
           Replicate_Do_Table:
       Replicate_Ignore_Table:
      Replicate_Wild_Do_Table:
  	Replicate_Wild_Ignore_Table:
                   Last_Errno: 0
                   Last_Error:
                 Skip_Counter: 0
          Exec_Master_Log_Pos: 4064
              Relay_Log_Space: 1305
              Until_Condition: None
               Until_Log_File:
                Until_Log_Pos: 0
           Master_SSL_Allowed: No
           Master_SSL_CA_File:
           Master_SSL_CA_Path:
              Master_SSL_Cert:
            Master_SSL_Cipher:
               Master_SSL_Key:
        Seconds_Behind_Master: 0
	Master_SSL_Verify_Server_Cert: No
                Last_IO_Errno: 0
                Last_IO_Error:
               Last_SQL_Errno: 0
               Last_SQL_Error:
  	Replicate_Ignore_Server_Ids:
             Master_Server_Id: 1
                  Master_UUID: 06f83a45-0dba-11e7-ab4a-0249fa88a6d9
             Master_Info_File: /var/lib/mysql/master.info
                    SQL_Delay: 0
          SQL_Remaining_Delay: NULL
      Slave_SQL_Running_State: Slave has read all relay log; waiting for 	more updates
           Master_Retry_Count: 86400
                  Master_Bind:
      Last_IO_Error_Timestamp:
     Last_SQL_Error_Timestamp:
               Master_SSL_Crl:
           Master_SSL_Crlpath:
           Retrieved_Gtid_Set:
            Executed_Gtid_Set:
                Auto_Position: 0
         Replicate_Rewrite_DB:
                 Channel_Name:
           Master_TLS_Version:
1 row in set (0.00 sec)