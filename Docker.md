출처: https://www.docker.com/
출처: https://minimilab.tistory.com/7 [MINIMI LAB]

Docker Private Registry 구축

Docker Registry
---- 

> registry v2 설치
~~~
sudo docker pull registry:latest
~~~

> registry 실행
-d : 백그라운드로 실행    
--name : 이미지 이름 설정    
-p : 사용할 포트 설정 (host port : docker port)   
--restart always : 컨테이너가 종료되어도 다시 실행    
~~~
docker run -d --name registry -p 5000:5000 --restart always registry
~~~

> tag 설정
registry에 push 할 이미지의 태그를 등록합니다.
docker tag <이미지 이름>:<태그> <Docker 레지스트리 URL>/<이미지 이름>:<태그>` 형식
~~~
$ sudo docker tag mongo:latest <원하는 도메인 또는 IP>:5000/mongo:latest
~~~

> 도커 서비스 재시작
~~~
$ sudo service docker restart
~~~

> docker push
생성한 registry 에 이미지를 push 합니다.
~~~
$ docker push <원하는 도메인 또는 IP>:5000/mongo:latest
~~~

Service
----

> insecure-registries 추가
registry를 사용할 수 있도록 insecure-registries를 설정해줍니다.
daemon.json 파일 작성
~~~
$ sudo vi /etc/docker/daemon.json
~~~
파일 없는 경우 생성해서 아래 내용 추가
아래 {} 까지 포함해서 넣어야 함 
~~~
  { "insecure-registries":["<원하는 도메인 또는 IP>:5000"] }
~~~  
  
> docker pull
생성한 registry 에서 이미지를 가져옵니다.
~~~
$ docker pull <원하는 도메인 또는 IP>:5000/mongo:latest
~~~
