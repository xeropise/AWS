### AWS Lambda: 서버리스 서비스이며 이벤트를 자동 실행

​																								![다운로드](https://user-images.githubusercontent.com/50399804/134811278-c82358e3-d2bc-4f85-ad77-d3f23c874ccf.png)			


- AWS Lambda는 데이터나 요청에 대한 실시간 처리나 백엔드 처리를 자동으로 실행하는 구조이다.

  

- 이와 같은 처리를 위해 전용 서버를 구축하거나 따로 관리하지 않아도 필요한 이벤트가 자동으로 실행된다.



- 서버에 상주하는 프로그램과는 다르게 <u>프로그램 실행 시에만 요금이 부과된다.</u>



- Lambda 함수 라는 형식의 함수를 사용하지만 새로운 프로그래밍 언어는 아니다. 잘 알려진 프로그래밍 언어로 작성한 코드를 바탕으로 Lambda 콘솔을 사용하여 GUI로 만들 수 있다.

  

- 사용할 수 있는 언어는 자바, C#, 파이썬, 루비, Node.js, Go 등이 있으며 템플릿도 제공한다.



![product-page-diagram_Lambda-RealTimeFileProcessing a59577de4b6471674a540b878b0b684e0249a18c](https://user-images.githubusercontent.com/50399804/134811281-55be0b0b-3664-46d4-a72c-5db002a2b218.png)

- Lambda 함수는 Lambda 서비스에 저장되며, 임의의 작업이 트리거가 되어 함수를 호출해 특정 AWS 리소스에서 작업이 수행된다.
  - 대표적인 예는 S3 버킷에 이미지를 저장하면 썸네일 생성 함수를 호출하여 자동으로 썸네일이 작성되는 예이다.



<br>



***

### Lambda의 용어

![aws-lambda-function-created](https://user-images.githubusercontent.com/50399804/134811400-0679e7a4-9265-4908-ba4d-9447413c6842.png)

- Lambda 는 프로그램 코드를 Lambda 서비스에 업로드하여 특정 AWS의 서비스를 실행하는 방식이다.



| 항목                  | 내용                                                         |
| --------------------- | ------------------------------------------------------------ |
| 이벤트 구동           | S3에 파일을 저장하거나 DynamoDB 에 데이터를 저장하거나 SES에 메일이 도착하는 등 AWS 서비스에 어떠한 변화가 생기면 Lambda 프로그램을 실행할 수 있다. |
| CGI를 대신하는 Lambda | API Gateway와 조합하여 [웹 CGI](https://velog.io/@seanlion/cgi)처럼 사용할 수 있다. |



<br>



***

### 이벤트 소스 목록

- Lambda 를 호출하는 방법으로는 3가지가 있다. 대표적으로 S3나 SES, API Gateway와 조합하여 사용하는 방식이다.



- Lambda 가 이벤트를 읽는 서비스

  - Kinesis

  - DynamoDB

  - SQS

    

- Lambda 함수를 동기적으로 호출하는 서비스

  - ELB
  - ALB
  - Cognito
  - Lex
  - Alexa
  - API Gateway
  - CloudFront
  - Kinesis Data Firehose



- Lambda 함수를 비동기적으로 호출하는 서비스
  - S3
  - SNS
  - SES
  - CloudFormation
  - CloudWatch Logs
  - CloudWatch Events
  - CodeCommit
  - Config



<br>

***

### Lambda 요금

- 요금 = 단가 x 실행 시간(초 단위) 로 단가는 Lambda에 할당한 메모리의 크기에 따라 다르다.