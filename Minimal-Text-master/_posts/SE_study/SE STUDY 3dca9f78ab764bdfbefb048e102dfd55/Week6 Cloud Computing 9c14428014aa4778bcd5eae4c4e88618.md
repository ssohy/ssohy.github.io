# Week6 Cloud Computing

## 클라우드 컴퓨팅 개요

- **클라우드 컴퓨팅의 정의 및 기본 개념**
- 컴퓨팅 리소스인 스토리지 및 인프라를 인터넷을 통해 서비스로 사용할 수 있는 주문형 서비스를 말한다.
- 개인과 기업이 물리적 리소스를 직접 관리할 필요 없고 사용한 만큼만 비용을 지불하면 된다.
- **클라우드 서비스 모델의 개요**
**- IaaS(Infrastructure as a Service)** : 컴퓨팅, 스토리지, 네트워킹, 가상화 등 IT 인프라 서비스에  대한 주문형 액세스를 제공. IT 리소스를 가장 높은 수준으로 제어하며 기존 On-premises IT 리소스와 가장 유사.
* On-premises : 기업이 자체적으로 IT 인프라를 소유, 관리 및 운영하는 경우.

**- PaaS(Platform as a Service)** : 클라우드 애플리케이션 개발에 필요한 모든 하드웨어 및 소프트웨어 리소스를 제공. 이를 사용하면 기업은 기본 인프라의 관리 및 유지보수에 대한 부담 없이 애플리케이션 개발에 집중 가능.

**- SaaS(Software as a service)** : 기본 인프라에서 유지보수 및 앱 소프트웨어 자체 업데이트에 이르기까지 전체 애플리케이션 스택을 서비스로 제공. SaaS 솔루션은 클라우드 인프라 제공업체에서 서비스와 인프라를 모두 관리하고 유지보수하는 최종 사용자 애플리케이션인 경우가 많음.
- **클라우드 컴퓨팅의 이점과 한계**
**- 이점**
    1) TTM(Time to market) 단축 : 개발자가 새 인스턴스를 가동하거나 사용 중지하여 빠른 배포를 통해 개발 속도를 높일 수 있음.
    2) 공동작업 : 사용자는 위치나 특정 기기에 얽매이지 않고 전 세계 어디서든 인터넷 연결이 되어있다면 데이터에 액세스 가능.

**- 한계**
    1) 연결 상태가 좋지 않으면 필요한 정보나 애플리케이션에 액세스 불가.(인터넷 연결에 의존)

## 클라우드 서비스 제공업체

- **주요 클라우드 서비스 제공업체 비교**
**- AWS  :** 포괄적인 온디맨드 컴퓨팅 리소스 제품군을 제공하며 사용자에게 컴퓨팅 성능, 스토리지 및 데이터베이스에 대한 액세스를 제공.
**- Azure :** Microsoft 프라이빗 클라우드와 퍼블릭 클라우드 사용을 모두 지원하는 다양한 기능과 통합하기 쉬운 강력한 온프레미스 인프라.
**- Google Cloud :** 데이터 분석, 머신러닝, AI 프로젝트에 중점을 둔 고객에게 가장 적합.
****
- **각 제공업체의 고유한 제공 서비스 및 강점**
**- AWS** 
Amazon EC2 (Elastic Compute Cloud) : 확장 가능한 가상 서버 인스턴스를 제공.
**- Azure**
Azure DevOps : 개발, 배포, 운영 자동화 도구.
**- Google Cloud**
Google Cloud Machine Learning Engine : 대규모 ML 모델을 손쉽게 학습 및 배포할 수 있는 플랫폼.

## 클라우드 컴퓨팅 트렌드

- **서버리스 컴퓨팅(AWS Lambda, Azure Functions 등)** : 개발자가 서버를 직접 관리하는 것이 아닌 애플리케이션 코드 실행만을 집중할 수 있도록 하는 클라우드 컴퓨팅 모델.

- 이점 : 클라우드 공급업체가 서버리스 환경에서 Auto Scaling 기능을 제공하여 서버리스 애플리케이션은 수요 0에서 최대 수요까지 자동으로 확장될 수 있음.

- 사용 사례 : Taco Bell은 AWS를 사용하여 비즈니스 로직과 데이터 변환을 수행하는 서버리스 애플리케이션을 만듦.
* Taco Bell : 미국을 대표하는 외식 브랜드 중 하나. COVID-19 팬데믹 기간 동안 소비자의 배달 수요에 빠르게 대응함.
- **엣지 컴퓨팅** : 정보 저장 및 컴퓨팅 능력을 해당 정보를 생성하는 디바이스와 이를 소비하는 사용자에게 더 가까이에서 제공하는 프로세스.
- 중요성 : 데이터에 즉각적으로 액세스하고 수집하고 분석의 필요성이 높아지면서 엣지 컴퓨팅의 중요도가 올라감.
- **하이브리드 클라우드 및 멀티 클라우드 전략**
- 둘 이상의 클라우드를 통합하는 클라우드 배포를 지칭함.
- 하이브리드 클라우드 : 기업이 프라이빗 클라우드와 퍼블릭 클라우드를 결합하여 하나의 인프라처럼 사용하는 클라우드 컴퓨팅 전략

* 프라이빗 클라우드 : 내부 데이터 센터에서 기업만이 단독으로 사용하는 클라우드
* 퍼블릭 클라우드 : 외부 클라우드 서비스 공급자가 제공하는 클라우드

- 멀티 클라우드 : 여러 퍼블릭 클라우드 서비스 공급자(Cloud Service Provider)를 동시에 사용하는 클라우드 컴퓨팅 전략

## 클라우드 보안

- **클라우드 보안 원칙**
- 레이어로 구성된 보안 접근 방식 빌드하여 필요에 따라 액세스를 제한하고 암호화를 구성.
- 심층 방어 방식을 적용하여 애플리케이션 및 인프라의 각 수준에서 보안을 구현.
- 배포 및 기타 관리 작업을 자동화하여 작업 스트림에서 수동 작업을 최소화.
- 자동화 된 도구를 사용하여 애플리케이션과 인프라를 모니터링.(CI/CD 파이프라인에서 자동화된 스캔 사용)
- **주요 클라우드 제공업체가 제공하는 보안 서비스** 
IAM(Identity and Access Management) : 서비스 및 리소스에 액세스할 수 있는 주체를 지정하고 세분화된 권한을 중앙에서 관리하며 액세스 권한을 분석할 수 있도록 하는 프레임워크.

## 컨테이너와 오케스트레이션

- **컨테이너화(Docker, Kubernetes)**
- 컨테이너 : 애플리케이션 소스 코드와 모든 환경에서 코드를 실행하는 데 필요한 모든 OS 라이브러리 및 종속성을 결합하는 경량의 실행 가능한 애플리케이션 구성 요소를 말함.

- Docker : 애플리케이션과 필요한 라이브러리, 설정 파일 등을 이미지로 만들어 컨테이너로 배포.

- Kubernetes : 컨테이너를 쉽고 빠르게 배포/확장하고 관리를 자동화해주는 오픈소스 플랫폼
- **클라우드 환경에서 컨테이너 사용의 이점** : 운영을 *자동화*해줌으로써 반복해서 개발 및 배포하고 새로운 요소와 기능을 더 빠르게 출시할 수 있음.
- **Kubernetes 개요 및 컨테이너화된 애플리케이션 관리에서의 역할**
- 가장 널리 사용되는 컨테이너 오케스트레이션 플랫폼으로 지정된 수의 컨테이너를 지정된 호스트에 배포하고 원하는 상태로 계속 실행 가능.

## 클라우드에서의 머신러닝과 AI

- **클라우드 서비스가 머신러닝 및 AI 작업을 지원하는 방법**
- AutoML : 모델 개발과 훈련 과정을 자동화하여 보다 빠르게 모델을 빌드.
- **AI 및 ML 서비스**
- AWS SageMaker : 이를 사용하여 단일 통합 개발 환경(IDE)에서 노트북, 디버거, 프로파일러, 파이프라인, MLOP 등의 도구를 사용하여 대규모로 ML모델 구축, 훈련 및 배포 가능.

- Google Vertex AI : ML모델과 AI애플리케이션 학습 및 배포하고 AI기반의 애플리케이션에서 사용할 LLM을 맞춤설정할 수 있게 해주는 ML플랫폼.
*LLM : 대규모 언어 모델

## 클라우드 자동화 및 DevOps

- **클라우드 환경에서 자동화의 중요성** : 짧은 반복 시간으로 지속적인 개선을 달성하여 고객의 피드백에 빠르게 대응 가능.
- **DevOps 관행 및 도구**
- CI/CD 파이프라인 : 지속적 제공 파이프라인은 새로운 소프트웨어를 제공하기 위한 일련의 자동화된 프로세스.
- 인프라스트럭처 코드화(Infrastructure as Code, IaC)  : 수동 프로세스가 아닌 코드를 통해 인프라를 관리하고 프로비저닝하는 것.
*DevOps :  개발(Dev)과 운영(Ops)의 합성어.
*CI :  지속적인 통합, CD : 지속적인 배포
*프로비저닝 :  IT 인프라를 생성하고 설정하는 프로세스
- **주요 DevOps 도구**
- Terraform : HashiCorp에서 개발한 오픈소스 IaC(Infrastructure as Code) 도구.
- Ansible : Red Hat에서 개발한 오픈소스 자동화 도구.
- Jenkins : 오픈소스 CI/CD 도구.

## 클라우드 비용 관리

- **클라우드 비용 최적화 전략**
AWS
- Spot Instances : 스팟 인스턴스는 온디맨드 가격보다 저렴한 비용으로 제공되는 예비 EC2 용량을 사용하는 인스턴스임.  스팟 인스턴스는 애플리케이션이 실행되는 시간을 유연하게 조정할 수 있고 애플리케이션을 중단할 수 있어 비용 면에서 효율적인 방법임.
- **클라우드 비용 모니터링 및 관리 도구와 관행**
AWS
- Cost Explorer : 사용량과 비용을 시각적으로 분석하고 손쉬운 인터페이스를 제공함. 예산 초과 방지를 위해 비용을 변화시킨 원인을 파악하고 이상을 탐지함.

→ 클라우드 비용을 관리하기 위해 적정 규모의 클라우드 서비스 및 인스턴스를 산정하고, 자동 확장 기능을 사용하여 필요할 때 자원을 확장하고 필요하지 않을 땐 축소할 수 있도록 함. 필요하지 않는 날엔 오프라인 상태로 전환할 수 있어야하며, 미사용 인스턴스는 제거하도록 함.

## 출처

[https://cloud.google.com/learn/what-is-cloud-computing?hl=ko](https://cloud.google.com/learn/what-is-cloud-computing?hl=ko)
[https://cloud.google.com/learn/advantages-of-cloud-computing?hl=ko](https://cloud.google.com/learn/advantages-of-cloud-computing?hl=ko)

[https://tridenstechnology.com/ko/클라우드-서비스-제공업체/#h-different-types-of-cloud-provider-differences](https://tridenstechnology.com/ko/%ED%81%B4%EB%9D%BC%EC%9A%B0%EB%93%9C-%EC%84%9C%EB%B9%84%EC%8A%A4-%EC%A0%9C%EA%B3%B5%EC%97%85%EC%B2%B4/#h-different-types-of-cloud-provider-differences)

[https://aws.amazon.com/ko/what-is/serverless-computing/](https://aws.amazon.com/ko/what-is/serverless-computing/)
[https://aws.amazon.com/ko/what-is/edge-computing/](https://aws.amazon.com/ko/what-is/edge-computing/)
[https://www.samsungsds.com/kr/cloud-glossary/difference-hybrid-cloud-multi-cloud.html](https://www.samsungsds.com/kr/cloud-glossary/difference-hybrid-cloud-multi-cloud.html)

[https://cloud.google.com/architecture/framework/security/security-principles?hl=ko](https://cloud.google.com/architecture/framework/security/security-principles?hl=ko)

[https://www.ibm.com/kr-ko/topics/container-orchestration](https://www.ibm.com/kr-ko/topics/container-orchestration)

[https://learn.microsoft.com/ko-kr/azure/machine-learning/concept-automated-ml?view=azureml-api-1&viewFallbackFrom=azureml-api-2](https://learn.microsoft.com/ko-kr/azure/machine-learning/concept-automated-ml?view=azureml-api-1&viewFallbackFrom=azureml-api-2)
[https://aws.amazon.com/ko/sagemaker/](https://aws.amazon.com/ko/sagemaker/)
[https://cloud.google.com/vertex-ai/docs/start/introduction-unified-platform?hl=ko](https://cloud.google.com/vertex-ai/docs/start/introduction-unified-platform?hl=ko)

[https://f-lab.kr/insight/cloud-infrastructure-automation-and-devops-importance](https://f-lab.kr/insight/cloud-infrastructure-automation-and-devops-importance)
[https://www.redhat.com/ko/topics/automation/what-is-infrastructure-as-code-iac](https://www.redhat.com/ko/topics/automation/what-is-infrastructure-as-code-iac)

[https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/using-spot-instances.html](https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/using-spot-instances.html)
[https://aws.amazon.com/ko/aws-cost-management/aws-cost-explorer/](https://aws.amazon.com/ko/aws-cost-management/aws-cost-explorer/)
[https://www.servicenow.com/kr/products/enterprise-asset-management/what-is-cloud-cost-management.html](https://www.servicenow.com/kr/products/enterprise-asset-management/what-is-cloud-cost-management.html)