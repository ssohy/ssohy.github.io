# Deployment and Monitoring

## Deployment

- pod의 개수를 관리
- 레플리카셋과 함께 동작함

* 파드

- 컨테이너를 실행하는 최소 단위

- 일시적인 존재로 컨테이너 재사용 촉진을 위한 플랫폼으로 컨테이너의 실행 상태를 관리하고 초기화 전용 컨테이너를 실행함

* 레플리카셋

- 파드 집합의 실행을 안정적으로 유지
- 명시된 동일 파드 개수에 대한 가용성을 보증하는데 사용.

![디플로이먼트, 레플리카셋, 파드 관계](Deployment%20and%20Monitoring%2011a8109a408e80349353fb485d6c91ef/image.png)

디플로이먼트, 레플리카셋, 파드 관계

## monitoring

(in docker)

- Prometheus
- 컨테이너화 된 환경에서 애플리케이션 모니터링을 위한 시스템
- 분산 스토리지에 대해 의존성이 없음

* Grafana

## 출처

[https://kubernetes.io/ko/docs/concepts/workloads/controllers/deployment/](https://kubernetes.io/ko/docs/concepts/workloads/controllers/deployment/)
[https://kubernetes.io/ko/docs/concepts/workloads/controllers/replicaset/](https://kubernetes.io/ko/docs/concepts/workloads/controllers/replicaset/)

[https://prometheus.io/docs/introduction/overview/](https://prometheus.io/docs/introduction/overview/)