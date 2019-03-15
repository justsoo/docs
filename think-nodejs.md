# Think NodeJS
(https://bcho.tistory.com/865)  
(http://woowabros.github.io/woowabros/2017/09/12/realtime-service.html)

#### 성능적인 관점  
> \[장점\]single thread : context switching 없음(성능 잘나옴) -> cpu 많이 않쓰고, 많은 connect를 동시에 처리 하기 좋다.  
> \[단점\]DB 연동 또는 File IO가 있을 경우, multi thread기 때문에, 서비스 성격 고려해야한다.  
> \[단점\]single thread : 하나의 작업 처리 시간이 길어지면, 급격한 성능이 저하 된다.  
#### 생산성 관점 
> \[장점\]Restful + DB API 기본 기능 개발 시간이 C#/Java 등 다른 언어보다 짧다.  
> \[단점\]코드 가독성이 떨어진다.  
> \[단점\]callback hell : callback 중첩되면 디버깅이 힘들다. 
#### 기능적인 관점  
> socket.io : websocket 지원하지 않는 브라우저도 지원한다.  
> 허허.... 다음에 고민 해보자
#### 관리적인 관점
#### 개인적인 관접
> 아.... 개인적으로 C# 더 잘 보인다.
