## ReactJS 기초 공부
- [자바스크립트 학습계획](https://rhostem.github.io/posts/2016-12-19-A-Study-Plan-To-Cure-JavaScript-Fatigue/)에 따른 리액트 공부

##### 강좌
- [Codecademy](https://www.codecademy.com/learn/react-101) 리액트JS 파트 1

##### 리액트란?
- 페이스북에서 개발한 UI 개발을 위한 자바스크립트 라이브러리
- 컴포넌트가 모인 어플리케이션
- 리액트의 장점은 빠른 반응과 높은 재사용성, 자바스크립트의 유지보수 문제를 해결할 수 있다는 점이다.


##### 1. JSX
- 리액트는 JSX 사용을 권한다. (순수 리액트로 코드를 작성하는 방법도 알아야함)
- 컴파일러가 없으면 Javascript로 자동 변환된다.
- Javascript와 달리 자동으로 닫히는 태그가 없다. 무조건 닫아줘야함.
ex) ``` <br /> ```


##### 2. 리액트
- 태그 안에서 자바스크립트 문법을 사용할 땐 중괄호 {}로 감싼다.
``` bash
ReactDOM.render(
  <h1>{2+3}</h1>
  document.getElementById('app')
);
```

- Class를 만드는 명령어, 객체가 전달되어야 한다.
``` bash
var Helloworld = React.createClass(
{
  render : function(){
    return <h1>Hello world</h1>
    }
});
// 중괄호 뒤에 ;를 붙이면 Syntax error
```

- 객체의 속성 가져오기
``` bash
var title = {
               title: "Excellent",
               src : "https://omg.com"
               };
var Title = React.createClass ({
     render : fuction() {
     return (
              <img src={title.src} />   //{변수.속성}으로 불러올 수 있다.
            );
          }
});
```

- if문 사용하기
``` bash
var React = require('react');
var ReactDOM = require('react-dom');
var fiftyFifty = Math.random() < 0.5;
// React.createClass call begins here:
var TonightPlan = React.createClass ({
  render : function() {
  if (fiftyFifty = true) {
    return (
      <h1>Tonight I'm going out WOOO</h1>
        )   
  }
  else {
  return (
      <h1>Tonight I'm going to bed WOOO</h1>
      )}   
  }
});
ReactDOM.render(
<TonightsPlan />,
document.getElementById('app')
);
```
