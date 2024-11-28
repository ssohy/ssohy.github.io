# Service Implementation

## 서버 서비스 배포 방식

<aside>
💡

무중단 배포란? 

서비스를 운영 중일 때 새로운 버전을 배포하기 위해선 1) 기존의 서비스를 종료하고 2) 새로운 서비스를 시작하는 과정이 필요하지만, 서비스의 중단 없이 새로운 버전의 소프트웨어를 배포하는 것을 말한다.
무중단 배포 방식으론 **Rolling, Canary, BlueGreen**이 있다.

</aside>

- Rolling Deploy 
- 사용 중인 인스턴스들에 새 버전의 서비스를 점진적으로 배포하는 방법.
- 서비스 중인 인스턴스 하나를 로드 밸런서에서 라우팅하지 않도록 한 후, 새로운 버전의 서비스를 적용하여 다시 라우팅하도록 함.

![image.png](Service%20Implementation%2011a8109a408e804884c7eff2e9e3749d/image.png)

장점

1. 인스턴스마다 차례로 배포하기 때문에 에러 등 이슈 발생 시 롤백 가능.
2. 기존의 인스턴스에 추가적인 인스턴스 늘리지 않아도 됨.
3. 관리에 용이

단점

1. 새로운 버전을 배포할 때 라우팅되어 있는 인스턴스의 수가 감소하기에 정상 동작 중인 인스턴스에 트래픽 몰릴 수 있음. 
→ 라우팅되어 있는 인스턴스들의 서비스 처리 용량을 고려해야 하는 이유임.
2. 배포가 진행될 때 기존의 버전과 새로운 버전이 함께 존재해 호환성 문제 발생 가능.

---

- Canary Deploy 
- 지정한 서버 또는 특정한 유저에게만 배포했다가 정상적이면 전체에게 배포하는 방법.

![image.png](Service%20Implementation%2011a8109a408e804884c7eff2e9e3749d/image%201.png)

장점

1. 문제 상황을 빠르게 감지 가능하여 성능 모니터링에 유용.
2. A/B 테스트 가능
* A/B 테스트 : 대조군과 실험군으로 나누어 특정한 UI나 알고리즘의 효과를 비교하는 방법론

단점

1. 네트워크 트래픽 제어에 부담될 수 있음.

---

- BlueGreen Deploy
- 신 버전을 배포하고 일제히 전환하여 모든 연결이  신 버전을 바라보게 하는 방법.
- Blue : 기존 버전, Green : 새로 배포될 버전
- 운영 중인 구 버전과 동일한 신 버전의 인스턴스를 나란히 구성한 후 배포 시점에 로드 밸런서를 통해 모든 트래픽이 일제히 전환됨.

![image.png](Service%20Implementation%2011a8109a408e804884c7eff2e9e3749d/image%202.png)

장점

1. 구 버전의 인스턴스가 그대로 남아있어서 빠른 롤백 가능.
2. 운영 환경에 영향을 주지 않고 새 버전 테스트 가능.
3. 구 버전의 환경을 다음 배포에 재사용 가능.

단점

1. 시스템 자원이 2배로 필요해 많은 비용 발생.

## DevOps와 애자일 개념

- DevOps
- 등장배경 : 과거의 개발 운영 체계는 1) 운영 이슈에 대한 처리의 어려움과 2) 빠르고 안정적인 배포의 어려움을 겪고 있어, 이를 해결하기 위해 나온 것이 DevOps이다.
- Development + Operation의 합성어
- 애플리케이션 개발-운영 간의 협업 프로세스를 자동화하는 것
    
    DevOps의 필수요소( = DevOps를 실행하기 위한 필수요소) : CALMS 모델
    

![image.png](Service%20Implementation%2011a8109a408e804884c7eff2e9e3749d/image%203.png)

* 추가 설명 : [https://sso-programing.tistory.com/entry/Week2-DevOps](https://sso-programing.tistory.com/entry/Week2-DevOps)

- 애자일
- 등장배경 : 1) 기존 폭포수 모델은 SW의 불확실성에 대처가 어려워 이를 해결하기 위해 나온 것이 애자일이다.
- 프로젝트에 대한 빠른 피드백을 통해 방향을 평가하여 짧은 사이클을 반복하는 방법.

## CI/CD 방식

- 지속적인 통합(Continuous Integration) : 개발자가 작업한 코드를 자동으로 테스트하고 테스트에 통과하면 코드를 통합하여 저장
- 지속적인 배포(Continuous Delivery/Deployment) : 작업한 코드 및 변경사항들은 테스트를 거쳐 리포지토리에 업로드 되고 실제 서비스 배포까지 자동화
- 개발된 코드를 기존 코드에 Merge하기 전에 잘 작동하는지, 규칙에 맞게 개발되었는지 자동으로 테스트. 테스트 통과한 코드를 바탕으로 빌드 후 테스트.

## CI/CD 툴 예시

- Jenkins
- 코드 변경 사항 발생 시 자동으로 빌드, 테스트, 배포 과정 수행 
→ 개발자는 고드 젼경에 따른 빌드 및 테스트 과정을 수동으로 수행할 필요할 없어 신속하게 개발에 대한 코드 검증 및 배포 가능

**- 구조 : Master/Slave**
∘ Master : controller로, Jenkins slave를 관리하고 작업 스케줄링과 slave 모니터링을 포함하여 다양한 작업을 관리.
∘ Slave : agent로, 실제 파이프라인 작업을 수행. 다양한 환경에서 작동하며 작업을 분산시켜 부하를 감소시키는 역할을 담당.  agent는 로컬 또는 클라우드 컴퓨터를 통해 Jenkins controller에 연결될 수 있어 다양한 유연성 제공.

![image.png](Service%20Implementation%2011a8109a408e804884c7eff2e9e3749d/image%204.png)

- Github Action
- 리포지토리에 대한 모든 풀 요청을 빌드 및 테스트하는 Workflows를 생성하거나 Merge된 풀 요청을 프로덕션에 배포 가능.

**- 구성요소 : Workflows/Events/Jobs/Steps/Actions/Runners/Evironment Variables and Secrets/Artifacts and Caching**
∘ Workflows : GitHub Actions의 기본 구성 단위로, “.github/workflows/<workflowName>.yml”이라는 YAML 파일에 정의됨. 워크플로우는 하나 이상의 작업을 포함할 수 있으며 리포지토리에서 푸시 또는 풀 요청과 같은 이벤트에 의해 트리거됨.
∘ Events : workflow를 시작하는 트리거 
∘ Jobs : workflow 내에서 실행되는 개별 작업
∘ Steps : Job 내 Job의 가장 작은 단위
∘ Actions : workflow에서 공유 및 결합할 수 있는 재사용 가능한 코드 단위
∘ Runners : 작업이 실행되는 가상 머신 또는 자체 호스팅 환경
∘ Evironment Variables and Secrets : 환경 변수는 workflow 내의 작업 및 스크립트에서 액세스할 수 있는 데이터를 저장하는 데 사용되고,  Secrets은 액세스 토큰 또는 API 키와 같은 민감한 데이터를 저장하는 데 사용되는 암호화된 환경 변수.
∘ Artifacts and Caching : 아티팩트는 빌드 출력 또는 테스트 결과와 같이 나중에 저장하고 사용할 수 있는 workflow에서 생성된 파일이고, 캐싱은 workflow 실행 간에 데이터를 저장하고 검색하는 데 사용되므로 이전에 다운로드한 종속성 또는 빌드 출력을 재사용하여 프로세스 속도를 높임.

### 출처

[https://hoehen-flug.tistory.com/53#google_vignette](https://hoehen-flug.tistory.com/53#google_vignette)

[https://blog.lxinternational.com/29539/](https://blog.lxinternational.com/29539/)

[https://wlsdn3004.tistory.com/63](https://wlsdn3004.tistory.com/63)

[https://somaz.tistory.com/213](https://somaz.tistory.com/213)