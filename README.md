**1. Project Information:** 
> 이 프로젝트는 React의 useState, useEffect, useRef 등의 Hooks를 실습할 수 있는 프로젝트이다. 총 4개의 LAB이 존재하며 각 LAB마다 Hooks를 적절히 조합하여 타이머와 입력창 제어 등을 구현하고, 동작 원리를 이해하는데 도움을 주는 프로젝트이다. 
>
**2. Installation:**
> 설치 및 실행 방법 & 코드 수정 전 실행화면: <br>
> git clone -> 폴더로 이동(cd) -> npm install -> npm run dev 
> ![코드 수정 전 실행화면](./run_image.png)
>
**3. Source Code Exploration:**
> **주요 파일 구조** 
> 1. App.jsx : 페이지의 전체적인 구조를 구성하고, 각 LAB의 정보를 저장하는 객체 배열 `labs`를 정의한다. 또한 사용자가 선택한 LAB에 해당하는 컴포넌트를 화면에 표시하는 기능을 담당한다.
> 2. Lab1_EffectTimer.jsx : useState와 useEffect를 이용하여 1초마다 숫자가 자동으로 증가하는 타이머를 구현한다. 또한 Cleanup을 통해 타이머를 정리할 수 있다.
> 3. Lab2_TimerControl.jsx : useState와 useEffect를 이용하여 타이머를 시작, 중지, 초기화하는 기능을 구현한다. 
> 4. Lab3_InputFocus.jsx : useRef를 이용해 입력창에 focus()를 적용하고 입력된 내용을 삭제하는 기능을 구현한다.
> 5. Lab4_RefTimer.jsx : useRef를 이용하여 타이머의 ID를 관리하고, 타이머의 시작, 중지, 초기화 기능을 구현한다. 또한 Cleanup을 이용하여 타이머를 정리한다.
>
> **useEffect**
> - Effect : useEffect가 실행될 때 특정 동작을 하는 수행한다. Timer 실행 및 정리, 브라우저 이벤트 등록 및 제거 등의 작업에 사용된다.
> - Dependency Arry : useEffect의 실행 시점을 제어하는 배열이다. 배열을 생략하거나 []로 지정하는 등 사용 형태에 따라 Effect의 실행 시점이 달라진다.
> - Cleanup : 컴포넌트가 언마운트 되거나 의존성 변경으로 Effect가 다시 실행되기 전에 기존 작업을 정리한다. 예를 들어 setInterval을 사용하여 실행 중인 타이머를 종료할 수 있다.
>
> **useRef** <br>
> useRef는 .current 속성에 값을 저장할 수 있다. useState와 동일하게 리렌더링 후에도 값이 유지되지만, useRef는 .current의 값이 변경되어도 리렌더링이 발생하지 않는다는 것이 특징이다. 
>
> **Code Analysis**
> 