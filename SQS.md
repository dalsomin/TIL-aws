# SQS

Amazon Simple Queue Service(SQS)는 **마이크로 서비스, 분산 시스템 및 서버리스 애플리케이션을 쉽게 분리하고 확장할 수 있도록 지원하는 완전관리형 메시지 대기열 서비스**입니다. SQS는 메시지 지향 미들웨어를 관리하고 운영하는 데 따른 복잡성과 오버헤드를 제거하고 개발자가 차별화 작업에 집중할 수 있도록 지원합니다. SQS를 사용하면 메시지를 손실하거나 다른 서비스를 가동할 필요 없이 소프트웨어 구성 요소 간에 어떤 볼륨의 메시지든 전송, 저장 및 수신할 수 있습니다. AWS 콘솔, 명령줄 인터페이스 또는 원하는 SDK, 3가지 간단한 명령을 사용하여 몇 분 만에 SQS를 시작할 수 있습니다.

SQS에서는 2가지 종류의 메시지 대기열을 제공합니다. **표준** 대기열은 최대 처리량, 최선 노력 순서, 최소 1회 전달을 제공합니다. SQS **FIFO** 대기열은 메시지가 전송된 정확한 순서대로 정확히 한 번 처리되도록 설계되었습니다.

1. 관리 오버헤드 제거 

   * 선결제 비용이 없고 메시징 소프트웨어를 구매 설치 및 구성할 필요가 없으며 지원 인프라를 구축 및 유지 관리하는 시간과 같은 소모적이 작업이 필요없다. 
   * SQS 대기열이 동적으로 생성되고 자동으로 확장되므로 어플리케이션을 신속하고 효율적으로 구축 및 확장가능하다. 

2. 메세지를 안정적으로 전달

   * 메세지를 손실하거나 다른 서비스를 가용 상태로 유지하지 않고도 처리량과 관계 없이 모든 데이터 볼륨을 전송할 수 있다. SQS를 사용하게 되면 어플리케이션 구성요소를 분리할 수 있으므로 이러한 구성요소가 독립적으로 실행되고 장애가 발생하여 시스템의 전체 내결함성이 향상된다. 
   * 모든 메시지의 복사본 여러개가 다중 가용 영역전체에 중복으로 저장

3. 민감한 데이터를 안전하게 유지 

   * SSE를 통해 각 메세지 본문을 암호화 하여 어플리케이션 간에 민감한 데이터를 교환할 수 있다. 
   * SSE는 AWS Keymanagement Service와 통합 되므로 SQS메세지를 보호하는 키와 다른 AWS리소스를 보호하는 키를 모두 중앙에서 관리할 수 있다. 

4. 탄력적이고 비용 효율적으로 확장

   * 용량 계획과 사전 프로비저닝에 대하여 걱정할 필요가 없다. 
   * 사용가능한 대기열당 메시지 수에 제한이 없다
   * 표준 대기열은 거의 무제한의 처리량을 제공한다. 
   * 비용은 사용량을 기준으로 부과되므로 자가 관리형 메시징 미들웨어를 사용하는 상시가동 모델과 비교하여 상당한 비용절감을 제공한다. 

   