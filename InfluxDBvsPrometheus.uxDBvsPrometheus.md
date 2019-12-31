https://kimsup10.com/2018/11/03/influxdb-vs-prometheus/

# 데이터 수집 방식: Push vs. Pull
InfluxDB는 push 기반의 시스템이다.    
InfluxDB에 데이터를 쌓기 위해서는 누군가 InfluxDB로 데이터를 넣어줘야 한다.    
어플리케이션 서버가 직접 api를 호출해 데이터를 넣거나, fluentd 등을 이용해 데이터를 넣어줘야 한다.

Prometheus는 pull 기반의 시스템이다. 
데이터를 가져 갈 수 있는 통로를 열어 놓고 이를 prometheus 서버의 설정에 넣어주면 알아서 데이터를 가져 간다. 
다양한 클라이언트 라이브러리들을 통해 데이터를 수집하고 이를 prometheus가 가져갈 수 있도록 포트나 api를 열어 주면 된다.

지표 수집 서버보다는 실제 서비스 서버가 훨씬 대수가 많은 것이 보통이다. 
Push 방식에서 각 서비스 서버의 데이터 수집 옵션을 수정하고 배포하는 것보다, 
소수의 지표 수집 서버의 설정만 바꿔주면 되는 pull 방식이 더 효율적이다.

# 데이터 저장 방식
InfluxDB는 metric value와 이것의 index들이 모두 database로 관리된다.
Prometheus는 index에 대해서만 디비로 관리하고 metric value들은 file로 관리 된다.

이 때문에 속도와 디스크 효율 면에서 prometheus가 더 나은 모습을 보인다. 
지표 수집은 필요로 하는 key에 대한 데이터 위치를 찾고 이를 가져가기만 하면 되는데, 
InfluxDB가 metric value도 db로 관리하는 것은 오버헤드에 가깝기 때문이다. 
대신, InfluxDB의 이런 특징은 지표 모니터링 보단 이벤트 로깅에서 더 강점을 보인다.

# 궁시렁
한곳에서 관리해도 귀찮습니다.^^
단점으로 스케일 아웃이 어렵다라고 합니다.
언젠가?? 한번? 으아아아~
