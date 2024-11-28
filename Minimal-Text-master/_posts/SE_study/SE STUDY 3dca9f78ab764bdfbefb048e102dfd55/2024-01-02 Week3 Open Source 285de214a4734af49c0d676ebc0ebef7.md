# Week3 Open Source

## Open Source Software

- Definition, Fundamental Principles, Types of Licenses (GPL, MIT, Apache, etc.)
    - 개방형 협업을 통해 개발 및 관리되는 소프트웨어. 무료로 누구나 원하는 대로 사용, 수정, 재배포 가능케 하는 것이 일반적.
    - Fundamental Principles
        1. 투명성 : 오픈 소스 프로젝트를 통해 커뮤니티의 모든 사람이 자신의 작업물에 필요한 정보와 자료에 액세스할 수 있다. 팀원들은 퀄리티를 위해 서로의 아이디어 공유하고 발견하는 것을 바탕으로 작업을 한다.
        2. 커뮤니티 : 오픈 소스 커뮤니티는 공통의 목표를 달성하고자 모인 사람들의 모임으로 공동의 가치와 목표가 의사 결정과 오픈 소스 프로젝트를 이끈다.
        3. 공개 협업 : 커뮤니티 프로젝트는 공동 작업을 장려하여 개인이 해결할 수 없는 문제가 발생했을 때, 그룹이 이를 해결한다. 
        4. 신속한 프로토타입 제작 : 팀원들이 프로토타입을 만들고 공유하는 반복적 접근 방식(애자일)을 따른다. 신속한 프로토타입 제작은 실험 문화를 장려하므로 효과가 있는 변경 사항을 개선 및 수행하고 그렇지 않은 사항은 폐기한다.
        5. 포용적 능력주의 : 오픈 소스 운동은 다양한 관점과 대화를 장려한다. 커뮤니티는 합의에 따라 결정을 내리지만 성공을 우선시하여 좋은 아이디어는 오픈 소스 커뮤니티로부터 더 많은 지지를 받는다.
    - Types of Licenses
        1. GPL(General Public License) → 복제 방지
        - GNU 프로젝트에서 개발.
        * GNU 프로젝트 : 리처드 스톨만의 주도하에 시작된 공개 소프트웨어 프로젝트.
        누구나 자유롭게 "실행, 복사, 수정, 배포"할 수 있고, 누구도 그런 권리를 제한하면 안 된다는 사용 허가권(License) 아래 소프트웨어를 배포한다.
        - 결과물로 작성된 코드가 모두가 사용할 수 있도록 무료로 게시된다는 조건 하에 누구나 적합한 방식으로 그의 소프트웨어를 재작성할 수 있다고 명시.
        - 다음 조건을 지켜야 한다.
            1) 컴퓨터 프로그램을 어떤 목적으로든 사용할 수 있으나, 법으로 제한된 행위는 할 수 없다.
            2) 컴퓨터 프로그램의 실행 복사본은 언제나 프로그램의 소스 코드와 함께 판매하거나, 소스 코드를 무료로 배포할 것.
            3) 컴퓨터 프로그램의 소스 코드를 용도에 따라 변경할 수 있다.
            4) 변경된 컴퓨터 프로그램 역시 소스 코드를 반드시 공개 배포할 것
            5) 변경된 컴퓨터 프로그램 역시 반드시 똑같은 라이센스(GPL)를 취할 것
        2. MIT → 매우 자유로움
        - MIT 대학에서 소프트웨어 공학도를 위해 설계한 라이센스.
        - 매우 유연한 라이센스로 존재하는 거의 모든 라이센스와 서로 호환된다. 저작권 고지만 유지된다면 소스코드를 사용, 수정, 배포하는데 제한이 없다.
        - 다음 조건을 지켜야 한다.
            1) 이 소프트웨어를 누구라도 무상으로 제한없이 취급해도 좋으나, 저작권 표시 및 이 허가 표시를 소프트웨어의 모든 복제물 또는 중요한 부분에 기재할 것(저작권자 표기)
            2) 저자 또는 저작권자는 소프트웨어에 관해서 아무런 책임을 지지 않는다. (책임 보증 부인)
        3. Apache → 튿ㄱ
        - 아파치 재단에서 만든 오픈 소스 라이센스.
        - 저작권자 고지해야 하고 사용, 수정, 배포의 자유는 있지만 책임 보증 부인 원칙을 따른다. 상표 사용 제한하며, 원본 소프트웨어를 수정해서 배포할 경우, 원본과 수정된 부분을 명확하게 구분하여 수정 사항을 문서화해야 한다.
        
        → 리액트, 
        → Next.js
        → 오픈소스의 강점들을 잘 보여주는 것 : VScode
        

---

## Open Source Projects

- Contribution Process (Issues, Fork, Pull Request), Documentation, Code Review, Conventions
    - Contribution Process
    1. Issues : 프로젝트의 문제점, 버그 또는 기능 추가 요청을 이슈 트래커에 기록 
    2. Fork : GitHub와 같은 플랫폼에서 원본 프로젝트와 독립적인 복사본을 자신의 계정에 생성하는 과정.
    3. Pull Request : 수정된 브랜치를 원본 저장소에 병합.
    - Documentation : 해당 소프트웨어를 이해하고 사용할 수 있도록 돕는 문서.
    - 구성 요소 : README 파일, CONTRIBUTING 파일, API 문서, 릴리스 노트 등
    - 문서화 도구 : Sphinx, MkDocs 등
    - Code Review : 개인 또는 여러 명의 개발자가 본인이 만들지 않은 코드의 내용을 점검하고 피드백을 주는 과정.
    - Conventions
    - Naming Rules : 파스칼 케이스(HelloWorld), 카멜 케이스(helloWorld), 스네이크 케이스(hello_world), 케밥 케이스(hello-world), 어퍼 케이스(HELLO_WORLD)
    - 들여쓰기 : tab, space 방식
    - 커밋 컨벤션
    
    ![Untitled](Week3%20Open%20Source%20285de214a4734af49c0d676ebc0ebef7/Untitled.png)
    

---

## Utilizing Open Source

- Benefits, Limitations, Examples (Linux, Apache, Mozilla Firefox, etc.)
    - Benefits : 라이선스 비용 절감, 필요에 맞게 수정하여 맞춤형 기능 추가 가능
    - Limitations : 보안 취약, 지적재산권 문제 발생
    - Examples
    - 리눅스 : 유닉스 기반 오픈 소스 OS
    - 아파치 : 웹 서버 SW
    - 모질라 파이어폭스 : 오픈 소스 웹 브라우저

---

### 참고

[https://www.ibm.com/kr-ko/topics/open-source](https://www.ibm.com/kr-ko/topics/open-source)

[https://aws.amazon.com/ko/what-is/open-source/](https://aws.amazon.com/ko/what-is/open-source/)

[https://nx006.tistory.com/26](https://nx006.tistory.com/26)

[https://velog.io/@rex/코드-작성-규칙들-Coding-Conventions](https://velog.io/@rex/%EC%BD%94%EB%93%9C-%EC%9E%91%EC%84%B1-%EA%B7%9C%EC%B9%99%EB%93%A4-Coding-Conventions)

[https://sdstony.github.io/open source/contributing-md/](https://sdstony.github.io/open%20source/contributing-md/)

[https://guscoco.com/entry/오픈-소스와-독점-소프트웨어의-장단점](https://guscoco.com/entry/%EC%98%A4%ED%94%88-%EC%86%8C%EC%8A%A4%EC%99%80-%EB%8F%85%EC%A0%90-%EC%86%8C%ED%94%84%ED%8A%B8%EC%9B%A8%EC%96%B4%EC%9D%98-%EC%9E%A5%EB%8B%A8%EC%A0%90)

[https://yozm.wishket.com/magazine/detail/1105/](https://yozm.wishket.com/magazine/detail/1105/)