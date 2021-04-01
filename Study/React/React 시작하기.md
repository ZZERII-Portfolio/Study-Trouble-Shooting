# 🐣React 시작하기

💻👨‍💻👩‍💻👩🏻‍💻👨🏻‍💻🐾🐤❣❤◾◽🗨💬🗯💭❓❔❗❕

## 🐥사전준비

### ◾ node JS

Node.js 는 자바스크립트가 브라우저 밖(ex. 서버)에서도 동작하게 하는 환경을 의미한다.

```
> node -v
v14.16.0
```

◽ 설치하기: https://nodejs.org/en/

**React 애플리케이션은 웹 브라우저에서 실행되는 코드**이므로 Node.js와 직접적인 연관은 없지만, **프로젝트를 개발하는 데 필요한 주요 도구들(ex. babel, 웹팩)이 Node.js 기반이기 때문에 반드시 설치**해야 한다.

### ◾ npm

npm 은 Node Packaged Manager의 줄임말로 Node로 만들어진 pakage 들을 관리해주는 툴

다양한 패키지를 설치하고 버전을 관리할 수 있다.

(python의 pip)

```
> npm -v
6.14.11
```

### ◾ npx

npm의 5.2.0 버젼부터 새로 추가된 도구

```
> npx -v
6.14.11
```

설치하기:

```
> npm install npx -g
```



## 🐤React App 생성하기



### ◾ CRA(Create-React-App)

**: React 프로젝트를 시작하는데 필요한 개발 환경을 세팅 해주는 도구(toolchain)**

React는 UI 기능만 제공한다. 따라서 개발자가 직접 구축해야하는 것들이 많다.

CRA를 이용하면 하나의 명령어로 React 개발환경을 구축할 수 있다.

CRA에는 babel이나 webpack과 같이 React 애플리케이션 실행에 필요한 다양한 패키지가 포함되어 있다. 

>react 를 사용하다보면 ES의 최신버전까지 사용해야 하는 경우가 존재한다.
>
>하지만 몇몇 브라우저에서는, 특히 IE 에서는 최신버전을 지원해주지 않는다.
>
>그렇기 때문에 webpack 이나 babel 등 과 같은 몇몇 방법이 필요하다.

 테스트 시스템, ES6+ 문법, CSS 후처리 등 거의 필수라고 할 수 있는 개발 환경도 구축해 준다.

이러한 개발 환경을 직접 구축할 경우 시간이 오래 걸릴 뿐 아니라 유지 보수도 해야한다. CRA를 이용하면 개발 환경 세팅을 해주기 때문에 기존 기능을 개선하거나 새로운 기능을 추가했을 때 패키지 버전만 올리면 된다.

> ### ◾ ES (EMCAScript)
>
> EMCA에서 만든 JavaScript표준안/ 스크립트 규격, 표준
>
> #### 버전 별 특징
>
> ##### ◽ ES3
>
> - 흔히 말하는 자바스크립트
>
> ##### ◽ ES5
>
> - 배열에 forEach, map, filter, reduce, some과 같은 메소드 지원
> - Object에 대한 getter / setter 지원
> - JSON 지원
>
> ##### ◽ ES6 (ES 2015)
>
> - let, const 키워드 추가
>   - 기존의 변수는 함수 scope를 가진 var 키워드를 이용하였습니다. 때문에 block scope를 가진 let과 const 키워드를 추가했습니다.
> - arrow 문법 지원
>   - arrow 문법은 두가지 장점이 있습니다. 첫째, 편하고 간결해진 코드를 작성할 수 있습니다. 둘째 this를 바인딩 하지 않습니다.
> - iterator / generator 추가
> - module import / export 추가
> - Promise 도입
>
> ##### ◽ ES8 (ECMA 2017)
>
> - async - await 도입



### ◾ npm으로 생성하기

npx 가 존재하지 않았을 경우에는 npm을 통해 react app 을 생성

```
npm install -g create-react-app
```

`-g`를 통해 전역적으로 `create-react-app`가 설치됨으로서 **여러 문제점 발생**

- CRA의 무거운 의존성 라이브러리들이 컴퓨터에 남는다
- CRA버전 업데이트 시, 전역적으로 설치된 CRA를 재설치 해야 한다.



### ◾ npx로 생성하기

```
npx create-react-app {app이름}
```

최신 CPA패키지가 다운로드 되고 설정들을 세팅한 후에 CRA패키지는 제거된다.

그러므로 무거운 의존성 라이브러리들도 남지 않고 함께 제거되는 이점이 있다.



### ◾ CRA기본 폴더 및 파일 구성

#### ◽ 초기 폴더 및 파일 세팅 구성

##### :: node.modules / package.json / .gitignore

![image-20210325203809615](https://user-images.githubusercontent.com/61822411/112605132-4e7dcc00-8e5a-11eb-94f6-7079a00b6d43.png) 

**1) node.modules**

- CRA 를 구성하는 모든 **패키지 소스 코드가 존재**하는 폴더

![image-20210325204045968](https://user-images.githubusercontent.com/61822411/112605134-4f166280-8e5a-11eb-881a-a879e11e1273.png) 


**2) package.json**

- CRA 기본 패키지 외 추가로 설치된 라이브러리/패키지 정보(종류, 버전)가 기록되는 파일

- 모든 프로젝트마다 package.json 하나씩 존재

- `"dependencies"`

  ![image-20210325204316937](https://user-images.githubusercontent.com/61822411/112605136-4f166280-8e5a-11eb-952b-50dfe42980f4.png)  

  - **리액트를 사용하기 위한 모든 패키지 리스트, 버전 확인 가능**
  - 실제 코드는 `node.modules` 폴더에 존재

  

  - **왜 node.modules 와 package.json 에서 이중으로 패키지를 관리할까?**

    - 실제 내가 작성한 코드, 내가 설치한 패키지는 내 로컬에만 존재한다.

    - github 에 올릴 때 내가 작성한 코드와 함께 package.json(추가로 설치한 패키지 정보)을 넘긴다.

    - 다른 사람이 그것을 (pull) 받아서 **npm install 만 입력하면 package.json 에 기록되어 있는 패키지의 이름과 버전 정보를 확인하여 자동으로 설치한다.**

    - 이때, github 에 올릴 때, node.modules 는 올리면 안된다. (불필요한 용량 차지),

      ![image-20210325204658042](https://user-images.githubusercontent.com/61822411/112605137-4faef900-8e5a-11eb-8126-37d08ae27ba0.png) 

    - .gitignore 파일에 github 에 올리고 싶지 않은 폴더와 파일을 작성할 수 있다.

      

- **참고) 새로운 Library(package) 설치 시**

  - 누군가 만든 소스코드를 다운받는 것
  - npm으로 설치 (ex. npm install slider)
  - 설치 시 node modules 에 자동으로 설치됨.
  - 하지만 **package.json - dependencies 에 추가 자동으로 되는 건 아님**.
  - 그래서, `npm install slider --save`
  - --save 까지 작성해야 dependencies 에 추가됨
  - (npm 버전이 업그레이드 됨에 따라 자동으로 추가되는 경우가 많지만 여전히 불안한 패키지들이 존재하기 때문에 패키지 설치 시 **--save 까지 입력하는 것을 권장**.)

- `"scripts"`

  ![image-20210325205222605](https://user-images.githubusercontent.com/61822411/112605129-4de53580-8e5a-11eb-85a7-5357885b5af9.png) 

  - `run` : 프로젝트를 development mode(개발 모드) 실행을 위한 명령어. 

    `npm run start`.

  - `build` : 프로젝트 production mode(배포 모드) 실행을 위한 명령어. 서비스 상용화.

- 참고) [package.json vs. package-lock.json](https://www.youtube.com/watch?v=P2CtFD6xa54)

**3) package-lock.json**

- 패키지 내부의 패키지 버전까지 관리해주는 파일
- pull 이후 충돌을 막는다.

**4) .gitignore**

- `.gitignore` 파일에 **github 에 올리고 싶지 않은 폴더와 파일을 작성**할 수 있다.
- `push` 를 해도 `.gitignore` 파일에 작성된 폴더와 파일은 올라가지 않는다.



##### :: public / src

**1) public 폴더**

- index.html
- images - 이미지 파일 관리
- data - mock data 관리

**2) src 폴더**

- components - 공통 컴포넌트 관리
- pages - 페이지 단위의 컴포넌트 폴더로 구성
- styles 폴더
  - `reset.scss` - css 초기화
  - `commom.scss` - 공통으로 사용하는 css 속성 정의 (ex. font-family, theme color)
- 참고) components vs. pages
  - 여러 페이지에서 동시에 사용되는 컴포넌트의 경우 components 폴더에서 관리함.
    (ex. Header, Nav, Footer)
  - 페이지 컴포넌트의 경우 pages 폴더에서 관리함.
  - 해당 페이지 내에서만 사용하는 컴포넌트의 경우 해당 페이지 컴포넌트 폴더 하위에서 관리함.



##### :: index.html / index.js / App.js
