## Oracle

### 建立连接

```
<?php

try{
  $tns ="(DESCRIPTION =(ADDRESS = (PROTOCOL = TCP)(HOST = 10.106.58.32)(PORT = 1521))
    (CONNECT_DATA =
    (SERVICE_NAME = dev)
  ));charset=utf-8";
  $oci = "oci:dbname=".$tns;
  $conn = new PDO($oci, "dev_master", "QXPHwLAQXzr");
  //var_dump($conn);
  $sql = "select count(*) from USER_ACCOUNT";
  $sth = $conn->prepare($sql);
  $sth->execute();
  $results = $sth->fetchAll(PDO::FETCH_ASSOC);
  var_dump($results);

} catch (PDOException $err) {

  var_dump($err, $err->getMessage());

}
```