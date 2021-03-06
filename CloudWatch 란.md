### Amazon CloudWatch: Amazon EC2 의 리소스 상태 감시

![img (1)](https://user-images.githubusercontent.com/50399804/135118078-9a05caf5-8b14-4813-ab41-322e439238d4.png)

- 일반적인 서버와 마찬가지로 AWS 서비스도 감시가 필요하고 물리적인 부분에 대해서는 AWS가 관리해줄 수 있을지 몰라도 설치한 시스템이나 소프트웨어의 감시는 본인 스스로 해야 할 필요가 있다.

- Amazon CloudWatch는 각 AWS 서비스의 리소스 모니터링과 관리를 담당하는 서비스이다.

- AWS의 각 서비스에서 지표 (여러 관점에서 동작을 평가하는 수치), 로그 등을 수집, 기록한다.

- 수집한 로그가 임계 값을 넘으면 특정 동작이 일어나도록 설정할 수 있기 때문에 감시 상황에 대처하는 관리도 가능하다.

- 기본 요금은 없고 종량제 요금제로 사용한 만큼만 지불한다. 또한, Amazon CloudWatch는 지원하는 서비스와 지원하지 않는 서비스가 있다.

<br>

#### 사용 가능한 조작과 Amazon CloudWatch Logs

- Amazon CloudWatch 로 CPU 사용률, 볼륨의 읽기 쓰기 횟수나 바이트 수, 네트워크 송수신 패킷 수 등을 감시할 수 있다.

- 감시하고 있는 항목이 임계 값을 넘을 경우에 어떠한 작업을 하도록 설정할 수 있다. 작업은 이메일 송신, EC2 작동(인스턴스 시작, 정지 등), Auto Scailing(인스턴스 수를 변경), Lambda 함수에 의한 임의 프로그램 실행 등이 있다.

- Amazon CloudWatch Logs를 통해 각종 로그를 기록할 수도 있는데 Lambda 함수를 실행할 때 로그가 기록되며 이 로그는 범용적인 로그이다. Amazon EC2 인스턴스에 에이전트를 설치하면 인스턴스 내에서 임의의 로그를 기록할 수 있다.

- 간단한 필터 기능도 있고, 로그를 확인할 수 있는 화면도 있다. 일정 기간이 지나면 CloudWatch Logs의 로그를 삭제하거나 S3 버킷(Amazon S3에서 데이터를 저장하는 용기)로 내보내는 것도 가능하다.

- AWS CloudTrail 이라는 감사 서비스를 활성화하면 누가 어떤 리소스에 접근했는지도 기록으로 남길 수 있다.
