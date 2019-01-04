# Docker-Image
Hadoop, Hive, Spark, Zookeeper, Kafka의 Docker Image
- Ubuntu 18.04
- Anaconda3 5.3.1
- Java 8
- Scala
- Protobuf 2.6.1
- Hadoop 2.9.0
- Spark 2.3.1
- Hive 2.3.3
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
# 완료 후, 인스턴스 재접속
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
$ git clone https://github.com/hwkim94/Docker-Image.git
```

## 3. Image 생성
```bash
$ cd Docker-Image/ybigta_docker_image
$ docker build --tag {image 이름}:{version} .
```

## 4. Container 생성
```bash
$ docker run -it --name {container 이름} -p {포트번호-포트번호}:{포트번호-포트번호} -v ~/workspace:/root/workspace {image 이름}:{version}
```

## 5. 기본 명령어  
```bash
# 컨테이너 중지
$ exit

# 컨테이너 재실행
$ docker start {container 이름}
# docker attach {container 이름}

# 컨테이너를 중지하지 않고 bash만 빠져나갈 경우
키보드에서 ctrl + p + q 입력
```

## 6. 기타
- 초기 jupyter notebook 비밀번호 : admin


## 7. Refernece
이 문서의 모든 내용 및 코드는 아래의 두 깃헙을 참고/이용하였습니다. 뿐만 아니라, 설치과정과 기본적인 명령어 부분은 '연세대학교 빅데이터 학회 YBIGTA 엔지니어링팀' 2018-여름방학 세션 중 김태오님의 Week2 - Git&Docker 세션의 자료 참고하였습니다. 

- [https://github.com/xodhx4/ybigta_pyspark_docker](https://github.com/xodhx4/ybigta_pyspark_docker)
- [https://github.com/YBIGTA/EngineeringTeam/wiki](https://github.com/YBIGTA/EngineeringTeam/wiki)
- Ybigta Engineering Team



