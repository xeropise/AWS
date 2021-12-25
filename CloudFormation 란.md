## CloudFormation 이란

![AWS-CloudFormation](https://user-images.githubusercontent.com/50399804/151097931-3d351791-e4d2-429e-9c8e-b8424bced67d.png)

- AWS 인프라를 코드를 통해 설정할 수 있는 것 , 자신이 생성할 AWS 인프라 자원을 코드로 정의하여 자동으로 정의된 자원을 생성하거나 삭제가능

  

- 일반적으로 이러한 개념을 IaC (Infrastructure as Code) 라고 부름

  

![스크린샷 2022-01-26 오후 12 16 52](https://user-images.githubusercontent.com/50399804/151098209-9c19c668-cba0-495f-a5ae-a35abc8f961d.png)

- 코드로 정의한 파일을 템플릿이라고 부르는데, 코드 형태는 JSON 이나 YAML 형식의 코드로 작성 가능



![create-stack-diagram](https://user-images.githubusercontent.com/50399804/151097936-ffa40905-5b39-441f-9b04-1e8612dc1160.png)

- 템플릿을 CloudFormation에 업로드하면 스택을 생성할 수 있다. 스택을 생성하면 템플릿에 정의된 AWS 인프라 자원에 대해 순서대로 자동 생성
  - 스택을 삭제하면 스택 생성에 의해 생성된 AWS 인프라 자원을 순서대로 자동 삭제한다.
    - 생성된 자원을 삭제할 때 일일이 수동으로 삭제할 필요 없이, 스택을 삭제하면 자동으로 생성된 자원이 삭제된다.

