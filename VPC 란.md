## Amazon VPC

![Picture2-2](https://user-images.githubusercontent.com/50399804/134214722-775e4c07-78d5-4612-997b-2ed8f10aea4b.png)

- AWS가 제공하는 AWS 계정 전용 가상 네트워크

- 네트워크와 서브넷 범위, 라우팅 테이블, 네트워크 게이트웨이 등 가상 네트워킹 환경을 설정할 수 있다.

- 웹 서버나 데이터베이스 서버와 같은 서버들은 네트워크에 연결되어 있어야 한다.

- 한 장소에 모아서 네트워크를 연결하는 것도 가능하지만 그렇게 되면 서버로서의 의미가 없다.
 
- AWS 서비스인 EC2 나 RDS(Relational Database Service) 도 마찬가지로 네트워크에 연결되어 있어야 한다.

- 이러한 네트워크를 구축하기 위해 사용되는 것이 Amazon Virtual Private Cloud(Amazon VPC)이다.

- AWS 계정 전용 가상 네트워크 서비스로, AWS에서 제공하는 리소스만 설치할 수 있다. 

- EC2 나 RDS 의 경우 VPC를 선택하지 않으면 서버를 생성할 수 없기 때문에 리소스를 사용하기 위해서는 반드시 필요한 서비스이다.
