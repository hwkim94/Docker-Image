# Docker-Image
Hadoop, Hive, Spark, Zookeeper, Kafka의 Docker Image
- Ubuntu 16.04
- Java 1.8
- Hadoop 2.9.0
- Hive 2.3.3
- Spark 2.3.1
- Anaconda 5.3.1
- Zookeeper 3.4.10
- Kafka 1.0.0

## 0. 인스턴스 준비
- AWS 인스턴스 준비

## 1. Docker 설치

- 패키지 설치
```bash
$ sudo apt-get update
$ sudo apt-get install \
  apt-transport-https \
  ca-certificates \
  curl \
  software-properties-common
```

- Docker repo 추가
```bash
$ sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg \
  | sudo apt-key add -
$ sudo apt-key fingerprint 0EBFCD88
$ sudo add-apt-repository \
  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) \
  stable"
```

- Docker CE 설치
```bash
$ sudo apt-get update
$ sudo apt-get install docker-ce

$ sudo groupadd docker
$ sudo usermod -aG docker $USER
```

- 테스트
```bash
$ docker run hello-world
```

## 2. Git clone
```bash
$ git clone 
```


