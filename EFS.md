## Elastic File System 이란? 

- 네트워크 파일 시스템 **(NFS v4)**을 사용하는 파일 스토리지 서비스 
- VPC 내에서 생성되며, 파일 시스템 인터페이스를 통해 EC2 에서 액세스
- **수천 개의 EC2 에서 동시에 액세스 가능**하며 , **탄력적으로 파일을 추가,삭제함에 따라 자동으로 Auto Scaling 가능**, 즉 <u>미리 크기를 프로비저닝할 필요가 없음</u> 
- 페타바이트단위 데이터까지로 확장 가능
-  최대 1 천 개의 파일 시스템 생성 가능 
-  가용성 
  - 여러 가용영역에서 액세스 가능 
  - 여러 가용영역에 중복 저장되기 때문에 하나의 가용영역이 파괴되더라도 다른 AZ 에서 서비스 제공 가능
  - IPSEC VPN 또는 Direct Connect 를 통해 On-premise 에서 접속 가능 가능 
  - 성능 모드 / 처리량 모드 모드 
  - 성능 모드 에 있어서 대 부분의 파일 시스템에 Bursting Mode 를 권장하지만 처리량이 많을 경우 Provisioned Mode 를 권장 
  - 처리량 모드 모드 에 있어서 액세스하는 EC2 가 매우 많을 경우 , MAX I/O mode 를 사용하는  것이 바람직하며(지연시간이 약간 길어짐 ) 그 밖의 경우 General Mode 를 사용하는 것을 권장 
- 수명 주기 관리
  - 위에서 언급한 스토리지 클래스와 관련된 서비스로 사용자가 지정한 일정기간동안 액세스하지 않은 파일을 Infrequent Access Class 로 옮길수 있도록 하는기능 
- 파일 시스템 정책 
  -  EFS 를 사용하는 모든 NFS 클라이언트들에게 적용되는 적용되는 IAM 리소스 정책 
  - 전송 중 암호화 , 루트 액세스 비활성화 , 읽기 전용 액세스 등 설정 가능 