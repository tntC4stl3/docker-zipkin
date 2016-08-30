Running
=====

* If you want to run an in-memory zipkin server, just run:  
`docker run -d -p 9410:9410 -p 9411:9411 zipkin`

* If you want to run zipkin with MySQL storage, there are some environment variables need to be set to docker container:  
    * STORAGE_TYPE=mysql
    * MYSQL_HOST=xx.xx.xx.xx (default is localhost)
    * MYSQL_USER=xxx (default is zipkin)
    * MYSQL_PASS=xxx (default is zipkin)
    * MYSQL_PORT=xxx (default is 3306)
    * MYSQL_DB=xxx (default is zipkin)