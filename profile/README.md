# Plogging Game Application, 줍깅 - SpringBoot / React

<div align="center">
<img width="500" alt="image" src="https://github.com/olo02/AWS_fullstack_semi_project_SNS/assets/121186383/3ce6b0f4-6ca2-48cc-9ba2-5cf9e4f6d533">

[데모 사이트 바로가기](https://jubging.olooe.city)

</div>

---

## 프로젝트 소개

> **Plogging Game Application** <br> > **개발기간: 2022.05.24 ~ 2022.07.03** <br>
> Demo Site : https://jubging.olooe.city

<br>
풀스택 개발자 과정의 파이널 프로젝트로 본 애플리케이션을 제작하였습니다. SpringBoot와 React의 사용 능숙도를 높이는 것과, 데이터 마이닝 과정과 시큐리티의 활용을 목표로 하여 프로젝트를 진행하였습니다. 개발환경은 Backend는 SpringBoot, Frontend는 React로 나누어 개발을 진행하였습니다. DataBase는 MariaDB를 사용하였고, Amazon EC2 및 Nginx와 tomcat을 사용하여 데모 사이트를 배포하였습니다.

줍깅 애플리케이션은 Tmap API와 GeoLocation API를 통해 사용자의 실시간 위치를 지도 위에 제공합니다. 또한 서울두드림길 생태문화길 코스정보 API를 활용하여 추천 산책경로를 안내합니다.

<details markdown="1">
    <summary>플로깅이란?</summary>

플로깅은 ‘이삭을 줍는다’는 뜻인 스웨덴어 plocka upp과 영어 단어 jogging(조깅)이 합쳐져 생긴 합성어로, 산책을 하며 쓰레기를 줍는 환경운동입니다. 국내에서는 이를 '줍다'와 '조깅'을 결합한 '줍깅'으로 부르고 있습니다.

플로깅(plogging) 자세는 스쿼트나 런지 운동 자세와 비슷하여 칼로리 소모량이 일반 조깅보다 약 50kcal를 더 소모한다는 연구결과가 발표되기도 했습니다.

</details>

<br>

[Backend Git 바로가기](https://github.com/plogging-project/Plogging_Project_Backend)

[Frontend Git 바로가기](https://github.com/plogging-project/Plogging_Project_Frontend)

<br>

---

## 시작 가이드

### Requirements

Backend

- [Java version 1.8](https://www.oracle.com/java/technologies/downloads/#java17)
- SpringBoot 2.7.14(SNAPSHOT)
- Gradle - Groovy

Frontend

- node.js with npm

### Installation

Backend

```bash
$ git clone https://github.com/plogging-project/Plogging_Project_Backend.git
```

Frontend

```bash
$ git clone https://github.com/plogging-project/Plogging_Project_Frontend.git
```

### 실행

Backend와 Frontend를 모두 실행해야 어플리케이션을 확인할 수 있습니다.

<br>

---

## 설계

### Stacks

- #### Environment

    <img src="https://img.shields.io/badge/intellijidea-000000?style=for-the-badge&logo=intellij Idea&logoColor=white">

- #### Language

  <img src="https://img.shields.io/badge/java-007396?style=for-the-badge&logo=java&logoColor=white"> <br>
  <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white">

- #### Framework & Library

    <img src="https://img.shields.io/badge/Spring MVC-6DB33F?style=for-the-badge&logo=spring&logoColor=white">   
    <img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=for-the-badge&logo=Spring Boot&logoColor=white">  
    <img src="https://img.shields.io/badge/Spring Security-6DB33F?style=for-the-badge&logo=Spring Security&logoColor=white"> <br>
    <img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=black">
    <img src="https://img.shields.io/badge/node.js-339933?style=for-the-badge&logo=Node.js&logoColor=white"> 
    <img src="https://img.shields.io/badge/react router-CA4245?style=for-the-badge&logo=reactrouter&logoColor=white">

- #### DataBase

    <img src="https://img.shields.io/badge/mariaDB-003545?style=for-the-badge&logo=mariaDB&logoColor=white">

- #### Infrastructure

    <img src="https://img.shields.io/badge/Amazon EC2-FF9900?style=for-the-badge&logo=Amazon EC2&logoColor=white">
    <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=Nginx&logoColor=white">
    <img src="https://img.shields.io/badge/apache tomcat-F8DC75?style=for-the-badge&logo=apachetomcat&logoColor=white">

### 요구사항

[요구사항 정의서 문서 엑셀 파일](https://onedrive.live.com/edit.aspx?resid=39026BE146DB1865!9909&ithint=file%2cxlsx&authkey=!AHkkaw2eZGgqXIE)

### UI/UX 디자인

<details markdown="1">
    <summary>Paper Prototyping</summary>

<div align="center">
<img alt="image" src="https://github.com/olo02/AWS_fullstack_semi_project_SNS/assets/121186383/d0d9fddd-53be-4249-8fa6-48014540e2c8">
</div>
</details>

### DataBase 구조

<details markdown="1">
    <summary>ERD</summary>

<br>
<div align="center">
<img alt="image" src="https://github.com/olo02/AWS_fullstack_semi_project_SNS/assets/121186383/da1e4237-c759-48d4-a81f-7d14ed119aa5">
</div>
</details>

<br>


---

## 주요 기능

#### 실시간 위치 추적 서비스

- 이동 통신 단말기의 실시간 위치를 감지하여 사용자의 현재 위치를 제공합니다. GeoLocation을 통해 받아온 좌표를 Tmap 지도에 마커로 나타냅니다.
- 사용자는 본인이 움직이는 위치를 지속적으로 확인하며 플로깅을 할 수 있습니다.

#### 경유지를 포함한 위치 정보를 도보경로로 지도에 표시

- 공공데이터 서울 두드림길 코스 API를 활용하여 데이터를 추출하였습니다. 코스를 분류하고 각 코스의 경유지를 순서대로 설정하여 데이터를 가공하였습니다. 해당 데이터의 좌표계를 Tmap API에서 사용하는 좌표계로 변환하였습니다.
- 사용자는 추천 플로깅 경로를 지도에서 본인의 위치와 함께 확인할 수 있습니다.

#### 시큐리티와 소셜로그인이 적용된 회원 서비스

- 현재 위치라는 민감한 정보가 담긴 애플리케이션의 특성을 고려하여, 시큐리티를 적용함으로써 안전한 회원 서비스를 마련하였습니다.
- 더불어 다양한 소셜로그인을 통해 편리한 회원 시스템을 구축하였습니다.

#### SNS형 친구 시스템과 메시지 기능

- 함께하고 싶은 플로거를 찾을 수 있는 플친(플로깅 친구)시스템을 제공합니다. 사용자는 원하는 플로거에게 플친을 신청하고, 신청을 수락 및 거절할 수 있습니다. 또 원하지 않는 플로거를 차단하여 더 이상의 위험을 막을 수 있습니다.
- 사용자는 나의 플친에게 메시지를 보내며 플친과 커뮤니케이션할 수 있습니다.

#### 모바일 웹 사용을 고려한 반응형 디자인

- 조깅을 하며 쓰레기를 줍는 플로깅의 특성을 고려하여, 웹 애플리케이션의 UI/UX를 다양한 이동 통신 단말기의 사이즈를 맞춘 반응형 디자인으로 제작하였습니다.
- 사용자는 언제 어디에서나 편리하게 줍깅 웹 애플리케이션을 이용할 수 있습니다. 향후 모바일 앱으로 제작 고려 중에 있습니다.

#### 지속적인 참여 유도를 위한 리워드와 챌린지 프로그램

- 환경운동 참여를 고취할 수 있도록 지속적인 참여를 위한 동기를 다양하게 마련하였습니다.
- 사용자는 챌린지 서비스를 통하여 혼자가 아닌 여럿이서, 추천경로 및 기간을 설정하여 목표로 삼고 챌린지를 진행할 수 있습니다.
- 또한 사용자는 플로깅 종료 후 인증글을 커뮤니티에 남기면 포인트를 지급받습니다. 지급받은 포인트는 리워드를 구매하는 데 사용될 수 있습니다. 리워드 서비스는 기부하기와 램덤박스로 제공됩니다.

#### 플로깅 인증글 커뮤니티

- 비동기
- 사용자는 나의 플친에게 메시지를 보내며 플친과 커뮤니케이션할 수 있습니다.

<br>

---

## 아키텍쳐

### 디렉토리 구조

Backend

```bash
├── gradle/wrapper
├── src
│   ├── main
│   │   ├── java/city/olooe/plogging_project
│   │   │    ├── config : WebMvcConfig 및 WebSecurityConfig 설정
│   │   │    ├── controller
│   │   │    ├── dto
│   │   │    ├── model
│   │   │    ├── filter
│   │   │    ├── persistence
│   │   │    ├── security : 시큐리티 및 Oauth2.0 설정
│   │   │    ├── service
│   │   │    └── PloggingProjectApplication.java : 프로젝트 실행 파일
│   │   └── resources
│   │           ├── application.yml : 기본 설정 파일 (추가 필요)
│   │           ├── application-datasource.yml : DataBase 설정 (추가 필요)
│   │           ├── application-mail.yml : Gmail 인증 설정 (추가 필요)
│   │           ├── application-oauth2.yml : Oauth2.0 설정 (추가 필요)
│   │           ├── prgrms.cer : Java keytool
│   │           ├── prgrms_keystore.p12 : Java keytool
│   │           └── prgrms_truststore.p12 : Java keytool
│   └── test/java/city/olooe/plogging_project : Junit test
├── upload/2023
├── .gitignore
├── README.md
├── build.gradle
└── settings.gradle
```

Frontend

```bash
├── .idea
├── public
├── src
│   ├── components
│   ├── config
│   │     ├── api
│   │     └── dataService : dataService.js - Backend server 연결 설정
│   ├── container
│   │     ├── pages : 모든 페이지 컴포넌트
│   │     └── profile : 회원 관련 페이지 컴포넌트
│   ├── demoData : 초기 템플릿 활용시 demodata
│   ├── i18n
│   ├── layout : top메뉴 및 sidebar
│   ├── redux : redux 관련
│   ├── routes : react-router-dom 관련
│   ├── static : css 및 이미지
│   ├── utility
│   │     ├── plogging : geolocation api
│   │     └── localStorageControl.js : 쿠키 설정
│   ├── App.js
│   ├── index.js
│   ├── logo.svg
│   ├── reportWebVitals.js
│   └── setupTests.js
├── .env : URL 및 API key 설정
├── .eslintignore
├── .eslintrc
├── .gitignore
├── .prettierrc
├── README.md
├── craco.config.js
├── customize-cra-config.js
├── package-lock.json
├── package.json
└── yarn.lock
```


---

## 화면 구성

<div align="center">

|                                                                     Web                                                                      |                                                                    Mobile                                                                    |
| :------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------: |
|                                                                 메인 페이지                                                                  |                                                                                                                                              |
| <img width="500" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/e4f1eddc-8059-4c5b-bf27-faefbf3def1a"/> | <img width="200" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/a22c6de5-b5f4-42f4-ba35-fe40f4aa4d3b"/> |
|                                                                로그인 페이지                                                                 |                                                                                                                                              |
| <img width="500" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/8555a616-ac73-4df1-a9d1-b0c6bde20b1d"/> | <img width="200" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/3a52d4cd-f015-42d7-b61a-c8606ccfe19b"/> |
|                                                               회원가입 페이지                                                                |                                                                                                                                              |
| <img width="500" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/2a7f961d-9c75-451f-9079-ffc3620a60d4"/> | <img width="200" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/92022ac6-3a69-4c29-b8c6-63c54427ece2"/> |
|                                                                플로깅 페이지                                                                 |                                                                                                                                              |
| <img width="500" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/e360cad9-5bfe-469f-a03a-bebf1e75b872"/> | <img width="200" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/8d97bdcf-f068-4c7e-ab6e-13dff8fdc2ff"/> |
|                                                               커뮤니티 페이지                                                                |                                                                                                                                              |
| <img width="500" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/7d8832a5-91e2-4784-a7f3-d614482468b5"/> | <img width="200" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/91ca6993-02de-4ba1-900d-d12a77a92d4b"/> |
|                                                                챌린지 페이지                                                                 |                                                                                                                                              |
| <img width="500" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/d5ad0a17-0e6c-4a6d-82a1-de03190b0826"/> | <img width="200" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/d4698bbc-1466-4006-88d0-52f1965323d5"/> |
|                                                                리워드 페이지                                                                 |                                                                                                                                              |
| <img width="500" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/43fe7148-b6c5-4a46-add1-170b13bc77c2"/> | <img width="200" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/c062ce52-538a-4837-9d61-ecf103674f5b"/> |
|                                                                 플친 페이지                                                                  |                                                                                                                                              |
| <img width="500" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/71912df1-f255-4b3e-9782-0cdd66fce7ef"/> | <img width="200" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/5b79bb32-c8f6-4770-bb3a-986b49d847a7"/> |
|                                                                프로필 페이지                                                                 |                                                                                                                                              |
| <img width="500" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/6bb0576c-44f5-42e0-86c2-9fe1fc963282"/> | <img width="200" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/dfc23729-cd0f-4033-af21-7479e5210dfd"/> |
|                                                                관리자 페이지                                                                 |                                                                                                                                              |
| <img width="500" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/c68e2df0-87fc-49ed-9d48-5b35bbb229ff"/> | <img width="200" src="https://github.com/plogging-project/Plogging_Project_Frontend/assets/121186383/a1fa7384-4895-4627-aae9-e67ce8bf0485"/> |

</div>



---

## 개발팀 소개

<div align="center">

|                                                            천은경(팀장)                                                            |                                      김민수                                       |                                      박연재                                       |
| :--------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------: |
| <img height="160px" src="https://user-images.githubusercontent.com/121186383/242636171-4e873ee3-bb3e-4961-806a-2f960c7210d1.jpg"/> | <img width="160px" src="https://avatars.githubusercontent.com/u/113892151?v=4" /> | <img width="160px" src="https://avatars.githubusercontent.com/u/132035172?v=4" /> |
|                                                 [@olo02](https://github.com/olo02)                                                 |              [@KimMinSoocoding](https://github.com/KimMinSoocoding)               |                    [@yeonjae97](https://github.com/yeonjae97)                     |
|                               - SNS 및 플친 기능 <br> - 커뮤니티/첨부파일 <br> - 회원 기능 : 관리자                                |         - 챌린지 기능 <br> - 챌린지원 및 일정 <br> - 로고 및 뱃지 디자인          |                     - 회원 기능 <br> - Security <br> - Oauth                      |

|                                      이시화                                       |                                      이재원                                       |     |
| :-------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------: | :-: |
| <img height="160px" src="https://avatars.githubusercontent.com/u/132035158?v=4"/> | <img height="160px" src="https://avatars.githubusercontent.com/u/132035168?v=4"/> |     |
|                    [@sihwaaaaa](https://github.com/sihwaaaaa)                     |               [@flatspringjava](https://github.com/flatspringjava)                |     |
|                - 플로깅 기능 <br> - 데이터 마이닝 <br> - 추천경로                 |                        - 리워드 기능 <br> - 포인트 및 뱃지                        |     |

</div>

---

## 프로젝트 후기

**천은경**

> Backend SpringBoot와 Front React를 분리하여 기존과 다른 구현 방식을 경험할 수 있었습니다. 설계 과정에서 테이블과 Entity의 관계성을 익힐 수 있었고, 작업 과정에서 Spring JPA의 사용과 Security의 구조에 대한 이해도를 높일 수 있었습니다.
팀원의 갑작스런 공백, 구현 도구의 문제, 무료 api의 한계 및 미흡한 초기설계, 일정 지연 등 단순 구현의 예외 뿐만 아니라 팀과 프로젝트 전반의 상황을 팀장으로 맞닥뜨리면서, 초기 설계와 예외에 대한 대처 계획이 매우 중요함을 깨달았습니다.
여러 한계로 인해 완벽한 구현을 할 수는 없었지만 많은 것을 배울 수 있었고, 앞으로에 도전과 귀감이 되는 시간이었습니다.


**김민수**


> jpa를 사용하면서 더욱 간편하고 간결해졌지만 그만큼 사전지식을 매우 요하는 작업이었습니다. 
또한 리액트와 연동하고 조회, 삭제, 생성 을 구현하면서 리액트에 대한 지식과, js에 대한 이해도가 올라가는 동시에 
js에 대한 더욱 깊은 지식이 없다는것이 아쉬웠습니다. 
구현되었어야 할 부분이 같이 되었더라면 더욱 완성도 있는 챌린지를 만들 수 있었을거라는 아쉬움이 남습니다 


**박연재**


> 여러 징검다리 역할을 하고 있는 회원을 맡았는데 
여러 역할 중에서도 우선적으로 중요한 역할이다보니 좀 더 긴장이 되었습니다. 
시큐리티라는 보안 요소를 회원에 도입해서 구현을 한 것이 때로는 어렵기도 했지만 재미있었고
중요한 경험을 했다는 생각이 들었습니다.


**이시화**


> 프로젝트에서 어렵고 중요한 핵심 기능을 맡았고 api를 적극활용해야 했기에 어려움이 많았지만 
오히려 그만큼 성장할 수 있는 시간이었습니다. 
 또한 난이도가 높았던 만큼 재미도 있었기에 후순위였던 기능들도 꼭 나중에 구현해보고 싶습니다. 


**이재원**


> 이번 프로젝트를 진행하면서 데이터를 어떻게 가공시켜야 할지, 데이터간 관계를 설계하는 데 있어 
기초지식의 필요성을 느끼게 되었습니다.
jpa나 리액트의 기초를 적응해 가면서 좀 더 빨리 적응했더라면 완성도가 높아지지 않았을까하는 아쉬움이 남습니다.


<br>

---

## References

- 공공데이터포털
- [HexaDash](https://preview.themeforest.net/item/hexadash-svelte-multipurpose-admin-dashboard-template/full_screen_preview/42355059?_ga=2.89554585.387259422.1685417936-981929731.1684981092&_gac=1.15578564.1685417936.Cj0KCQjwmtGjBhDhARIsAEqfDEfSUxQge-4AImOmjLxF9yImP0oMmiQeSBaFLbDyNZcAgLma_X3wolsaAk-UEALw_wcB)
- README Template : [parkjiye](https://velog.io/@luna7182/%EB%B0%B1%EC%97%94%EB%93%9C-%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-README-%EC%93%B0%EB%8A%94-%EB%B2%95)
- Hit : [hit](https://hits.seeyoufarm.com/)
