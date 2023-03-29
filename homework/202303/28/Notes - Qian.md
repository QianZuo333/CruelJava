# JDBC
- It is the middleware between DB and application.
- Persistence: the application send the data to database which stores the data.
  云原生年代，DB，文件存储，高速缓存，HBASE都可以进行persistent.
  
```
for (DriverInfo aDriver : registeredDrivers) {
    if(isDriverAllowed(aDriver.driver, callerCL)) {
        try {
            println(" trying " + aDriver.driver.getClass().getName());
            Connection con = aDriver.driver.connect(url, info);
            if (con != null) {
                println("getConnection returning " + aDriver.driver.getClass().getName());
                return (con);
            }
        } catch (SQLExcepton ex) {
            if (reason == null) {
                reason = ex;
            }
        }
    } else {
        println(" skipping: " + aDriver.getClass().getName());
    
    }
}
```
