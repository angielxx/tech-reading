# 왜 리액트인가?

> 리액트가 시장을 점령하게 된 이유

1. 명시적인 상태 변경

   - 리액트의 상태 변화는 '단방향', '명시적'
   - 양방향 바인딩(ex. Angular) 단점 : 코드의 규모가 커질수록 상태변화 흐름을 파악하기 어려워짐
   - 이에 반해 단방향 바인딩의 장점 : 데이터 흐름의 변화가 단순하기 때문에 코드를 읽기가 쉽고 버그를 야기할 가능성이 적다.

2. JSX(JavaScript XML)

   - Angular가 뷰를 표현하기 위해 사용하는 것
     - 문자열 템플릿
     - ngIf라는 Angular 전용 문법
   - React가 뷰를 표현하기 위해 사용하는 것
     - JSX : HTML에 자바스크립트 문법을 더한 쉬운 문법 = "자바스크립트 친화적"

3. 배우기 쉽고 간편

   - 위 두 특징에 의해 배우고 사용하기 쉬움
   - 완벽히 이해하고 성능을 최적화하는 것은 어려움

4. 강력한 커뮤니티, 그리고 메타

   - 리액트의 자유도 : UI를 위한 라이브러리로만 작동하고 그 외 모든 것에 자유도
   - 커뮤니티의 존재 = 리액트 사용자들이 같은 어려움의 해결을 빠르게 도와줌
   - 메타의 존재 = 오픈 소스가 빠르고 안정적으로 성장할 수 있게 하는 메인 스폰서

# 리액트의 역사

### 2010년대 : 프런트엔드 개발 환경을 향한 페이스북의 도전

#### 2000년대

- LAMP 스택 = Linux, Apache, MySQL, PHP
- 웹 브라우저 : 서버에서 동적으로 생성된 콘텐츠를 단순히 다운로드하여 렌더링
- 자바스크립트 : 폼 처리와 같은 부수적인 역할만 담당

#### 2010년대

- 제이쿼리
- 브라우저의 발전 : 로컬 스토리지, 웹소켓, 캔버스, SVG, Geolocation 등 다양한 기능 제공
- ES5가 표준 스펙

> 브라우저 환경의 변화로 자바스크립트 코드가 복잡해짐

- 자바스크립트의 DOM 조작
- Ajax를 통해 클라이언트에서도 서버와 통신

> 복잡해진 자바스크립트 코드에 의해 AngularJS, CoffeeScrript, Underscore.js 등의 등장

- MVVM, MVC 패턴을 통해 자바스크립트 코드를 체계화하고자 함

> 페이스북의 BoltJS 개발

- 다수가 이용하는 서비스이기에 성능이 중요했음
- 비대해지는 자바스크립트 코드 + 서버 렌더링의 한계 -> 서비스 성능 저하 -> BoltJS 개발

### BoltJS 등장과 한계

- BoltJS 개발 이유 : 당시 존재하던 옵션(바닐라JS, 제이쿼리, Angular 등)으로 복잡한 서비스를 구현하면서 사용자 경험 또한 높이기 어렵다고 판단
- BoltJS의 한계점으로 Fbolt 개발 : Functional Bolt = 함수형 지향 = 리액트의 시초

단방향 바인딩 구조의 채택

- 기존에 사용되던 양방향 바인딩은 DOM의 변경을 최소화하기 위해 채택되었음
- 단방향 바인딩의 아이디어는 모델의 데이터가 변경되어 뷰가 변경되어야 할 때 이전 DOM을 버리고 새롭게 렌더링하자는 방식이었음 -> DOM 변경이 잦아지며 성능에 대한 우려
- 하지만 성능보다도 DOM 업데이트의 어려움(추적의 어려움)으로 인해 단방향 바인딩이 더 유용하여 채택됨

### 페이스북 팀의 대안으로 떠오른 리액트

- UFI 프로젝트 : 게시물 하단에 댓글, 공유 버튼이 있는 화면 구현
- 즉각적으로 반응하는 화면을 구현하기 위해 JSX 구문, Flux 패턴에 대한 아이디어 등장
- 인스타그램 : 인수한 인스타그램을 리액트를 사용해 웹 개발 도전
- 리액트 오픈소스로 공개하려는 노력 시도

### 리액트에 대한 회의적인 의견과 비판

- JSConf US 2013에서 공개한 리액트 -> JS내의 HTML이 들어간 JSX 구문이 관심사의 분리 원칙을 지키지 않는다며 비판받음
- 이유 : 페이스북 개발자와 일반 웹 개발자 사이의 관점 차이 = 페이스북은 복잡한 웹 어플리케이션을 효율적으로 관리하기 위해 리액트를 개발

### 드디어 빛을 보는 리액트

- 오픈 소스 컨트리뷰터들로부터 많은 아이디어와 도움을 받아 리액트 커뮤니티를 형성하는데 노력을 기울임
- 커뮤니티의 지지를 받으며 성장
- 이러한 커뮤니티 속에서 상태 관리 라이브러리, 라우터 라이브러리, 서버 사이드 렌더링 프레임워크 등이 등장하며 생태계를 형성
- 야후, 넷플릭스의 리액트 채택

> 대형 IT 회사의 리액트 도입, 리액트 커뮤니티 성장에 따른 다양한 리액트향 라이브러리의 등장으로 리액트는 프런트엔드 시장에서 전성기를 맞이함

### 리액트의 현재와 미래

> 현재 리액트의 과업 : 서버에서의 리액트 활용

- 브라우저와 클라이언트에서의 작동 개선
- 클라이언트에서 할 수 없는 서버에서의 작업과 서버 환경의 가능성에 초점을 두고 서버에서 작동할 수 있는 다양한 기능과 유스케이스를 추가할 것

> 즉, 앞으로 리액트 개발자들은 Node.js 같은 서버 환경을 공부하는 것이 기본소양으로 자리 잡게 될 것
