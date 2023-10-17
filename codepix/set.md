❯ docker-compose ps
              Name                            Command               State                                          Ports
--------------------------------------------------------------------------------------------------------------------------------------------------
codepix_app_1                      tail -f /dev/null                Up
codepix_control-center_1           /etc/confluent/docker/run        Up       0.0.0.0:9021->9021/tcp,:::9021->9021/tcp
codepix_db_1                       docker-entrypoint.sh postgres    Up       0.0.0.0:5432->5432/tcp,:::5432->5432/tcp
codepix_kafka-topics-generator_1   bash -c sleep 5s && kafka- ...   Exit 0
codepix_kafka_1                    /etc/confluent/docker/run        Up       0.0.0.0:9092->9092/tcp,:::9092->9092/tcp, 0.0.0.0:9094->9094/tcp,:::9094->9094/tcp
codepix_pgadmin_1                  /entrypoint.sh                   Up       443/tcp, 0.0.0.0:9000->80/tcp,:::9000->80/tcp
codepix_zookeeper_1                /etc/confluent/docker/run        Up       2181/tcp, 2888/tcp, 3888/tcp

❯ docker exec -it codepix_app_1 bash
root@a161a3e01f09:/go/src#
root@a161a3e01f09:/go/src# go mod init github.com/eduardotecn
ologo/imersao15CodePix/codepix-go
go: creating new go.mod: module github.com/eduardotecnologo/imersao15CodePix/codepix-go
root@a161a3e01f09:/go/src#