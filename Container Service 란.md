### AWS 컨테이너 서비스: 애플리케이션 단위로 실행할 수 있는 가상 환경

<img width="402" alt="2202B14A57728FBF0A" src="https://user-images.githubusercontent.com/50399804/134812606-c0d30a02-fc5c-4359-a81d-0c0c886ce099.png">

- 컨테이너란 프로그램 실행 환경을 분리하는 방식으로 버추얼박스나 VMware 와 같은 가상 서버는 OS 전체가 가상 환경이다.

  

- 컨테이너는 애플리케이션 프로그램만 컨테이너로 분리하고, 애플리케이션에 필요한 라이브러리나 데이터를 포함하고 있다.

  

- 도커는 유명한 컨테이너 형식 중 하나로 AWS는 도커 형식의 컨테이너를 지원한다.

  

- 일반적으로 컨테이너 서비스에는 컨테이너를 배치, 관리하기 위한 '레지스트리 서비스'와 컨테이너로 분리된 애플리케이션의 실행과 컨테이너의 조정을 수행하는 '오케스트레이션 서비스'가 필요하다.

  

- AWS의 레지스트리 서비스로는 Amazon Elastic Container Registry(ECR) 가 있다.

  

- 오케스트레이션 서비스로는 AWS 각 서비스를 기반으로 이루어진 Amazon Elastic Container Service(ECS)와 최근 주목받고 있는  쿠버네티스와 호환되는 서비스인 Amazon Elastic Kubernetes Service(EKS)가 있다.



<br>

***

### 컨테이너 서비스의 용어

| 항목                                                       | 내용                                                         |
| ---------------------------------------------------------- | ------------------------------------------------------------ |
| 컨테이너                                                   | 프로그램 전체를 분리하여 실행하는 시스템을 말한다.           |
| 도커 이미지                                                | 컨테이너를 구성하는 프로그램이나 설정을 말한다.              |
| 도커 허브                                                  | 도커 이미지를 등록하는 서비스로 AWS는 도커 허브로 ECR을 사용한다. |
| Amazon EC2 Container Registory(ECR)                        | 도커 이미지를 등록하는 서비스이다.                           |
| Amazon ECS                                                 | 도커 이미지에서 EC2나 AWS Fargate에 컨테이너를 생성하여 실행하는 서비스이다. |
| 쿠버네티스                                                 | 컨테이너를 종합 관리하는 방식이다.                           |
| Amazon Elastic<br>Container Service for<br>Kubernetes(EKS) | AWS가 제공하는 쿠버네티스 서비스이다.                        |
| AWS Fargate                                                | 컨테이너를 실행하는 EC2를 자동으로 관리하기 위한 방식이다.   |



<br>

***

### AWS Fargate의 방식

<img width="1167" alt="Product-Page-Diagram_Fargate@2x a20fb2b15c2aebeda3a44dbbb0b10b82fb89aa6a" src="https://user-images.githubusercontent.com/50399804/134812767-09c44f1f-8e6c-42cd-8fef-31c6335f2f09.png">

- AWS Fargate 는 EC2 를 관리하는 서비스이다.

  

- AWS Fargate는 필요에 따라 EC2 인스턴스를 기동하고 EC2 안에 컨테이너를 할당하고 실행하는 방식이다.



<br>

***

### 컨테이너 서비스 요금

- EC2 시작 유형의 경우는 'EC2 요금'만 발생하여 요금이 추가되지 않는다.

 

- Fargate 시작 유형의 경우

  - ( 할당된 CPU당 실행 단가 x 자동 시간(분) x 컨테이너 수 ) <br> + ( 메모리 단가 x 가동 시간(분) ) <br> + 데이터 전송 요금 이다.

