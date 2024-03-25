Connection Pooling
====================
=> SessionFactory Object will holds Jdbc connection pool, which have set of ready made JDBC connection objects and uses them in the
                   creation of Hibernate session Objects.

=> By default hibernate uses builtin jdbc connection pool which is not suitable for production environment due to performance issues.

=> To integrate hibernate built in JDBC connection pool we write the below property in hibernate.cfg.xml file
     <property name ="hibernate.connection.pool_size">25</property>

The best JDBC connection pooling for hibernate integration 
------------------------------------------------------------
For STANDALONE mode -> Use 3rd party suppiled JDBC connection pool like hikaricp(recommended), proxool, viboor, agroal, c3po....
                       Don't use built in JDBC connection pool.

For WEBAPPLICATION mode -> use server provided connection pool from servers like webLogic, Tomcat, Wildfly...
                           Don't use 3rd party suppiled.		
