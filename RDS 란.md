### Amazon RDS란

![AWS-Feature](https://user-images.githubusercontent.com/50399804/134775169-04a5d733-e23b-4bbb-a2f9-6099aca4a4a7.png)

- Amazon Relational Database Service(Amazon RDS)는 관계형 데이터베이스 6종류의 제품을 클라우드에 최적화된 상태로 제공하는 서비스이다.

- Amazon Aurora 외에도 PostgreSQL, MySQL, MariaDB, Oracle Dtabase, SQL Server 를 지원하며 메모리, 성능, I/O 등이 최적화된 데이터베이스 인스턴스를 제공한다.

- 데이터베이스의 제공 방식은 EC2와 비슷하다. VPC 상에 인스턴스 형태로 구축하며 다양한 인스턴스 클래스를 사용할 수 있다.

  - EC2와 다른 점은 RDS는 '매니지드 서비스' 이며 업데이트 등의 관리가 AWS에 의해 자동으로 이루어진다는 점이다.

  - 백업과 같이 번거로운 관리 작업도 자동화되어 있어 관리자가 수행할 필요가 없다.

- AWS Database Migration Server(DMS) 를 사용하면 기존 데이터베이스를 이전하거나 복제하는 것도 가능하다.
