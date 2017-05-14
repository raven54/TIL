### [생활코딩](https://opentutorials.org/course/1)  자바스크립트 과정

#### Today Topic
- [정규표현식](https://opentutorials.org/course/743/6580) (Regular Expression)

##### 자바스크립트 언어의 기능 중 하나로 문자열에서 특정한 문자를 찾는 도구이다.
<div style="font-size: 16px; margin-top: 10px;">언제 어떻게 사용가능한가?</div>
1. [추출](#extrac) - 패턴을 만들고, 그 패턴에 해당하는 정보를 추출할 때
2. [테스트](#test) - 정보가 패턴 안에 존재하는지, 존재하지 않는지 테스트 할 때
3. [치환](#sub) - 찾아낸 정보를 다른 정보로 치환할 때

###### - 문자열 객체의 몇몇 메소드는 정규표현식을 사용할 수 있다.

***

#### 정규표현식 생성
``` bash
var pattern = /a/;                // 정규표현식 리터럴
var pattern = new RegExp('a');   // 정규표현식 객체생성자
```
>두가지 모두 같은 결과를 만들지만 각자 장단점이 있다.

#### <a id="extrac">추출</a>
##### RegExp.exec()

``` bash
console.log(pattern.exec('abcdef')); // ["a"]
//  문자열 a를 값으로 하는 배열을 리턴한다.
```
``` bash
console.log(pattern.exec('bcdefg')); // null
// 인자 'bcdefg'에는 a가 없으므로 null을 리턴한다.
```

##### String.match()
>RegExp.exec()와 비슷하다

``` bash
var pattern = /a/;
var str = 'abcdef';
var str2 = 'bcdefg';

str.match(pattern);
["a"]
str2.match(pattern);
null
```

#### <a id="test">테스트</a>
##### RegExp.test()
>test는 boolean이다.

``` bash
console.log(pattern.test('abcdefg')); // true
console.log(pattern.test('bcedfg')); // false
```
#### <a id="sub">치환</a>
##### RegExp.replace()
``` bash
var pattern = /a/;
var str = 'abcdef';

str.replace(pattern,'A');
"Abcdef"
// a를 A로 치환
```
##### String.replace()
> 문자열에서 패턴을 검색해서 이를 변경한 후에 변경된 값을 리턴한다.

``` bash
console.log('abcdef'.replace(pattern, 'A')); // Abcdef
```
