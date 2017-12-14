# Movie Fun!

Smoke Tests require server running on port 8080 by default.

## Build WAR ignoring Smoke Tests

```
$ mvn clean package -DskipTests -Dmaven.test.skip=true
```

## Run Smoke Tests against specific URL

```
$ MOVIE_FUN_URL=http://moviefun.example.com mvn test
```
```
minio server ~/shared

git clean -df
./gradlew bootRun --parallel
echo "source ~/workspace/apps-movie-fun-modernization-code/.env" >> ~/.bashrc
source .env
env

./gradlew tasks
./gradlew bootRun
./gradlew build
./gradlew clean build
cf push moviefun --random-route -p build/libs/moviefun-1.1.0-SNAPSHOT.war 

./gradlew applications:movie-fun-app:bootRun
./gradlew applications:movie-service:bootRun
./gradlew applications:album-service:bootRun

logs6.papertrailapp.com:16333 

https://hartford-2017-11.pal.pivotal.io/modernization/service-discovery/index.html

cf create-service p-mysql 100mb movies-mysql
cf bind-service moviefun movies-mysql
cf restage moviefun

cf create-service aws-s3 standard moviefun-s3
cf bind-service movie-fun-app moviefun-s3

mvn spring-boot:run
mvn clean package -DskipTests -Dmaven.test.skip=true
cf push moviefun --random-route --no-start -p target/moviefun.war
cf push moviefun --random-route -p target/moviefun.war

cf create-user-provided-service paper-trail -l syslog-tls://logs6.papertrailapp.com:16333 

git push --set-upstream origin logging-start-2

     "access_key_id": "AKIAJXKJUHYWUAXCCOYA",
     "bucket": "cf-6dff8c99-a0d2-4f39-91f9-f70c8ef00a75",
     "region": "us-east-1",
     "secret_access_key": "7TVZSoMKcpC3GK/7PzKRNC/iCpARZQyRFi2pG5X8"

flyway -url="jdbc:mysql://10.0.4.41:3306/cf_9a12cbb0_4994_498a_9779_b18cf7662c59/albums?user=C5rKNUumgxsRJ2nk&password=wr4cH182dpdro4Dh" -locations=filesystem:databases/albums clean migrate

cf ssh -N -L 63306:10.0.4.41:3306 album-service

cf set-env moviefun S3_ENDPOINTURL http://s3.amazonaws.com 
cf set-env moviefun S3_ACCESSKEY AKIAJXKJUHYWUAXCCOYA
cf set-env moviefun S3_SECRETKEY 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
cf set-env moviefun S3_BUCKETNAME cf-6dff8c99-a0d2-4f39-91f9-f70c8ef00a75

cf set-env moviefun MOVIEFUN_DATASOURCES_MOVIES_URL jdbc:mysql://10.0.4.41:3306/cf_be8fc5a0_1ae6_47e2_830d_fff7332f943c
cf set-env moviefun MOVIEFUN_DATASOURCES_MOVIES_USERNAME hkmPNWrDDBIb4EWV
cf set-env moviefun MOVIEFUN_DATASOURCES_MOVIES_PASSWORD r6nhUJVkvleQ8v6P



cf set-env movie-fun-app   MOVIEFUN_DATASOURCES_MOVIES_URL dbc:mysql://10.0.4.41:3306/cf_c1d9ccfc_577d_4508_8fed_fbeb2398f5e5
cf set-env movie-fun-app   MOVIEFUN_DATASOURCES_MOVIES_USERNAME Az8tMzi7K6aVBoRo
cf set-env movie-fun-app   MOVIEFUN_DATASOURCES_MOVIES_PASSWORD 2dXO9W4uxsagPN5L

cf set-env album-service S3_ENDPOINTURL http://s3.amazonaws.com 
cf set-env album-service S3_ACCESSKEY AKIAJDC5CPGAHQR27BLA
cf set-env album-service S3_SECRETKEY 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
cf set-env album-service S3_BUCKETNAME cf-1e05dd8b-ccbb-47a9-9589-b72c8be36751

cf set-env album-service   MOVIEFUN_DATASOURCES_MOVIES_URL jdbc:mysql://10.0.4.41:3306/cf_88c05047_c4e0_484f_97c9_6460ebdc8d74
cf set-env album-service   MOVIEFUN_DATASOURCES_MOVIES_USERNAME ImAbJ2GzdkvQEEgR
cf set-env album-service   MOVIEFUN_DATASOURCES_MOVIES_PASSWORD kQ3zAuHz3XxEgCMP

cf set-env movie-service   MOVIEFUN_DATASOURCES_MOVIES_URL jdbc:mysql://10.0.4.41:3306/cf_3263b984_5c8d_4eb5_87fc_3eafd4b16fae
cf set-env movie-service   MOVIEFUN_DATASOURCES_MOVIES_USERNAME TaXD6cc1WDK7QKia
cf set-env movie-service   MOVIEFUN_DATASOURCES_MOVIES_PASSWORD zx40jicGCyAlHyvC

cf set-env movie-fun-app S3_ENDPOINTURL http://s3.amazonaws.com 
cf set-env movie-fun-app S3_ACCESSKEY AKIAI7A4DBKGLXNW72IQ
cf set-env movie-fun-app S3_SECRETKEY 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
cf set-env movie-fun-app S3_BUCKETNAME cf-1e05dd8b-ccbb-47a9-9589-b72c8be36751

cf set-env album-service GRANT_TYPE client_credentials 
cf set-env movie-service GRANT_TYPE client_credentials 

aws s3 ls s3://cf-6dff8c99-a0d2-4f39-91f9-f70c8ef00a75
aws configure
aws s3 cp albums.csv s3://cf-6dff8c99-a0d2-4f39-91f9-f70c8ef00a75

cf mysql album-database < databases/albums/schema.ddl


apt search rabbitmq
/etc/init.d/rabbitmq-server start
cd /etc/init.d
sudo rabbitmq-plugins enable rabbitmq_management
http://localhost:15672/#/queues

curl -X POST http://localhost:8080/rabbit -d ""

cf create-service p.rabbitmq solo rabbit
cf bind-service moviefun rabbit
cf service rabbit
https://rmq-5471641b-58d6-4a98-acca-f4b1e8af0017.sys.longs.pal.pivotal.io


curl -X POST http://moviefun-adductive-goldcrest.apps.longs.pal.pivotal.io/rabbit -d ""

./gradlew submitReplatformingBackgroundJobsWithAmqp -PmovieFunUrl=http://moviefun-adductive-goldcrest.apps.longs.pal.pivotal.io

mvn clean package
cf push remove-session-state -p target/remove-session-state-lab.war -i 2 --random-route --no-start
cf create-service p-redis shared-vm my-redis 
cf bind-service remove-session-state my-redis
cf start remove-session-state


```
