# HTML
#### DOCTYPE 이란 무엇인가요?
- doctype 선언: 웹문서가 어떤 버전의 html 언어로 작성되었는지 결정하는 기능이빈다
DTD를 통해서 현재의 웹문서가 어떤 버전의 html 기술로 작성되있는지 웹브라우저에 전달합니다.
- 선언의 목적: 문서간의 호환성을 높이기 위함 신버전과 구버전의 경우 호환 태그들이 있어 버전이 안맞을경우 문법 에러를 발생시킬수 있습니다 즉 선언이란 과거 html 버전에서 해당버전에 맞게 문법 검사를 하며 현재 버전에서 현재 기준에 맞게 검사하는 기능입니다.
- 문서의 최상단에서 독타입을 선언합니다, 구버전을 폐지하지 않는이유는 수많은 과거의 웹페이지의 자료들을 잃어버릴수 있기때문입니다 즉 보존때문입니다

# 여러 meta 태그들에 대한 질문

 - 시맨틱 태그란 무엇인가요? : 시맨틱 태그란 태그 이름자체로 브라우저나 긿 읽은 사람들, 아무튼 모든 사람들에게 의미를 전달할수 있는 태그,
 예를들어 시멘틱 태그가아닌 div,span등은 그내용이 무엇인지 알기 어려우나
 ```
 <header>,<nav>,<img>
 ```
 등은 들어도 어리짐작할수 있게 할수 있는 장점이있다

# CSS
- **position**에 대해 설명해주세요! : mdn에 따르면 문서상의 요소를 배치하는 방법을 지정하는 것입니다, 
예를들어
- **static**: 요소를 일반적인 흐름에 따라 배치하며 위치를 바꾸는 **top**,**right**,**left** ,**z-index** 속성이 아무런 영향을 주지 않습니다
- **relative**: 요소를 일반적인 문서 흐름에 따라 배치하고, 자기자신을 기준으로 **top**,**right**,**bottom**,**left**의 값에 따라 오프셋적용 ,오프셋은 다른요소에 영향을 주지 않습니다, 따라서 페이지 레이아웃에서 요소가 차지 하는 공간은 **static**일 때와 같습니다

- **display**: 디스플레이 속성은 요소를 어떻게 보여줄지를 결정하는것
  - none: 보이지않음
  - block : 블록박스 : div ,p h ,li태그등이 해당되며 
  기본적으로 가로 영역을 모두 채우며, block요소 다음에 등장하는 태그는 줄바꿈 된것처럼 보입니다. width, height를 지정할수 있으며 이전 요소의 오른쪽에 배치될때 항상 다음줄에 렌더링이 됩니다
  - inline: 인라인 박스 : span,b,i,a태그 등이 이에 해당됩니다.
  block 과 달리 줄바꿈이 안됨, width 와 height 를 지정 할 수 없습니다. **글자나 문장에 효과를 주기 위해 존재하는 단위**라고 할 수 있습니다.
  줄바꿈 되지않고 오른쪽에 표시됩니다.
  - inline-block :block 과 inline의 중간형태 : block과 inline 의 중간 형태이며 줄바꿈이 되지않지만 크기를 지정 할수 있습니다

- **flex** : 플렉스 속성은 하나의 플렉스 아이템이 자신의 컨테이너가 차지하는 공간을 맞추기 위해 크기를 키우거나 줄이는 방법을 설정하는 속성입니다

grid는 사용해보셨나요? <______

- **box model**: 컨텐츠 영역, padding(안쪽),border(테두리),margin(바깥쪽) 으로 나눠집니다

- **margin, padding**의 차이는 무엇인가요? : 적용해본다면 알수있듯이
 패딩은 안쪽 영역으로 안쪽의 여백을 조절하고 마진은 바깥쪽 여백을 조정에 위치나 크기를 조정할수 있다.


- **inline, block, inline-block의 차이점은 무엇인가요**?
   - inline: 예 span, w/h 조정불가 마진 패딩탑 바텀 적용불가
     line-height 를 원하는대로 사용불가
   - block : 한줄을 무조건 점유 다음태그는 줄바꿈됨, 예:div
   - inlin-block : 위의 중간의 형태 기본적인건 inline과 비슷하며 inline속성에서 할수 없었던 w/h 변경 및 line-height를 커스텀 적용할수 있음

- **reset.css, nomalize.css**는 무엇인가요? 
  - reset.css :브라우저간의 차이를 최대한 없애서, 스타일이 0인 상태에서 디자인을 만들어 나가기 위해 생겨난것이다. 
  ```js
*{
 margin:0;
padding:0;
border:none;
}
머리좋으신분들이 신경써줘서 요즘엔 거의 사용되지 않고 있는 방식
11년도가 최신상태이고 yui 는 14년 이후에 업데이트가 없다
  ```
  - nomalize.css
   가끔 reset css와 nomalize를 동일시하는 분들이 있는것 같지만, 비슷하지만 속을 들여다 보면, 조금 다르다는 것을 확인할수있다.
   
   ```js
 h1{
   font-size:2em;
   margin: 0.67em 0;
 }
   ```
  위 예제와 같이 초기화하지않고 지정하여 기본상태를 만들어주는것
  요즘은 **노말라이즈** 가 많이 사용되고 있다.

- **sass, css module, css in js에 대해, 각각 장단점.**
#### css
    **장점**: 
   1.기능확장성
     - 추가적인 sw나 플러그인이 필요없이 html 기능 확장
     - 설정하기 쉽고 단순한 규칙
     - w3c에서 웹표준으로 정의
   2.양식모듈화
     - 흐름이 같은 문서 약식으로 저네 구성가능
     - 디자인과 웹구조의 완벽한 분리로 하나의 html문서에 다양한 디자인 적용 가능
   3.간편성
    - 문서 형식을 손쉽고 다양하게 구성 가능
    - 코드 절약을 통한 작은 용량
    - 이해하기 쉬운 구조
   4.일관성
    - 사용 환경에 영향 받지 않습니다.
    - 웹페이지의 한가지 요소만 변경해도 전체페이지의 내용을 한꺼번에 변경할수 있습니다
   **단점**
   1. 브라우저와의 호환성 문제
  
  #### css in js
  **장점**:
   - css의 컴포넌트화로 스타일시트의 파일을 유지보수 할 필요가 없다. css 모델을 문서 레벨이 아닌 컴포넌트 레벨로 추상화한다(모듈성)
   - css-in-js는 JavaScript 환경을 최대한 활용 할 수 있다.
   - JavaSciprt와 Css사이의 상수와 함수를 쉽게 공유 할 수 있다
   - 현재 사용중인 스타일만 DOM에 포함된다
   - Css-in-js는 짧은 길이의 유니크한 클래스를 자동으로 생성 코드의 경량화
  **단점**:
  - 러닝커브
  - 새로운 의존성
  - 별도의 라이브러리 설치 로 번들 크기 커짐
  - 인터랙션한 페이지일 경우 css 파일을 따로 관리하는 방버에 비해 느린 성능을 보여줄 수 있다.
  
  #### scss
  **장점**:
   - 코드중복을 줄일수 있다. SASS 사용 전 코드(코드가 복잡할수록 유지보수 어려움(
   - 변수를 사용할수 있기 때문에 유지보수가 쉬워준다.
   **단점**:
   - 전처리기를 위한 도구가 필요하다.
   - 다시 컴파일 하는 데 시간이 걸린다.
   이런 전처리기기가 효율적인 코드를 작성할 수 있게 도와주지만 모든 코드에 필수적으로 사용하는것은 아니고 중첩, 변수, Mixin 등 기본적인 기능의 사용으로도 css로만 작성할 때 보다 편리한 코드를 작성할수있다 상황에 따라서 적용하다
   
    
    

#### **CSS를 head 위에 둬야하는 이유는 무엇인가요?**
**css link 태그를 head 태그 안에 넣는 것은 최적화된 웹사이트를 구출할 때 적절한 명세의 일부이다.** 페이지가 처음 load 되면 HTML과 CSS가 동시에 파싱됩니다. HTML은 DOM을 만들고, CSS는 CSSOM (CSS Object Model)을 만듭니다. 두 가지 모두 웹사이트에서 시각적인 부분을 만드는데 필요하므로, 빠른 "first meaningful paint"를 가능하게 합니다. 이 점진적 렌더링은 사이트의 성능 점수에서 측정되는 사이트 최적화의 범주입니다. 문서 최하단에 스타일 시트를 두는 것은 많은 브라우저에서 점진적 렌더링을 금지하게 되는 것입니다. 몇몇 브라우저는 스타일이 변경되면 페이지의 요소를 다시 그리는 것을 피하기 위해 렌더링을 차단합니다. 그렇게되면 사용자는 빈 하얀 페이지를 보게 됩니다.

그 외에도 상단에 배치하면 페이지가 점진적으로 렌더링되기 때문에 UX가 향상됩니다. 문서 맨 아래에 CSS를 두는 것은 Internet Explorer를 비롯한 많은 브라우저에서 점진적 렌더링을 금지시키는 것입니다. 몇몇 브라우저는 스타일이 변경되면 페이지의 요소를 다시 그리지 않아도 되도록 렌더링을 차단합니다.사용자는 빈 하얀 페이지에서 멈추게 됩니다. 또한, 스타일이 없는 내용이 잠깐 보이는 것을 방지합니다. 다른 경우에는 스타일되지 않은 내용이 깜빡일 수 있습니다.

```
- 이 점진적 렌더링은 사이트의 성능 

해당 화면을 레이아웃 잡아보세요.

이 화면을 만드려면 어떤식으로 해야할 것 같나요?
```

# JS 관련
#### JS를 body 맨 밑에 둬야 하는 이유는 무엇인가요?

- js코드가 무거울 경우 이 코드들을 불러오느라 html css가 렌더링되지 않아 대기 상태가 길어질수있어 사용자의 경우 오류로 판단할수 있다. 하지만 맨뒤에 선언할경우 html과 css가 모두 동작한 다음 불러와 미완성 상태가 길지 않을것이다 또한 문서의 dom구조가 완료된 시점에서 실행되기 때문에 따로 추가 설정할 필요가 없다.

head에 둬야 하는 경우가 있을까요? 어떨 때인가요?(defer async 제외)

var, let, const의 차이는 무엇인가요?

**scope 란**?
 - 유효범위 이며 모든 식별자(변수이름,함수이름,클래스 이름)는 자신이 선언된 위치에 의해 다른 코드가 식별자 자신을 참조할수 있는 유효 범위가 결정된다. 즉 이를 scope라고 하며 스코프는 식별자가 유효한 범위를 말한다
 - 스코프는 전역과 지역 스코프가 있다, 전역 에서 선언된 변수는 전역 스코프를 갖는 전역 변수, 지역에서 선언된 변수는 지역 스코프를 갖는 지역 변수이다
 - 전역변수는 어디서든지 참조가능하며, 지역변수는 자신의 지역 스코프와 하위 지역 스코프에서 유효하다
 
**함수레벨 scope?**
 
 - 함수 내에서 선언된 변수는 함수 내에서만 유효하며 함수 외부에서는 참조할 수 없다. 즉, 함수 내부에서 선언한 변수는 지역 변수이며 함수 외부에서 선언한 변수는 모두 전역 변수이다.

**block scope란 무엇인가요?**

 - 모든 코드 블록(함수,if문,for문,while문,try/catch문 등)내에서 선언된 변수는 코드 블록 내에서만 유효하며 코드 블록 외부에서는 참조할 수 없다. 즉, 코드 블록 내부에서 선언한 변수는 지역 변수이다.
 
 **렉시컬 환경?**
 
-  스크립트 전체, 실행중인 함수, 코드블록 등은 자신만의 렉시컬 환경을 갖는다. 렉시컬 환경은 환경레코드, 외부렉시컬 환경으로 구성된다.

```js
function na(a, b) {
	let name = 'lee' 
}

na()

환경레코드에 {name: 'lee', a: undefined } 이런식으로 저장되어 있다.
```

**외부 렉시컬 환경?**

- 현재 렉시컬 환경보다 더 상위의 렉시컬 환경이다. 스크립트는 최상위 렉시컬 환경이며 스크립트 내에 호출된 함수나 코드블록은 외부렉시컬 환경으로 스크립트 렉시컬 환경을 참조한다.

**이벤트 등록?**<캡틴판교>
```js
<button>add one item</button>
HTMLCopy
var button = document.querySelector('button');
button.addEventListener('click', addItem);

function addItem(event) {
	console.log(event);
}
```
- add one item 이라는 버튼을 쿼리셀럭터로 가져와서 버튼에 클릭 이벤트를 달아줍니다
버튼을 클릭하면 addItem이라는 함수가 실행되며 addItem 함수에 event인자가 넘어옵니다

"하위에서 상위 요소로의 이벤트 전파방식을 "Event Bubbling" 이라고 합니다.

**이벤트 버블링, 캡처링, 위임**

- 버블링?:
  - 하위의 요소중에 이벤트가 발생했을때 더상위의 화면 요소들에게 전달되는 것이다
  예를들어 리액트 에서 하위컴포넌트의 데이터가 상위컴포넌트에 전달된다는 의미랑 같다
  
  ```js
<body>
	<div class="one">
		<div class="two">
			<div class="three">
			</div>
		</div>
	</div>
</body>
HTMLCopy
var divs = document.querySelectorAll('div');
divs.forEach(function(div) {
	div.addEventListener('click', logEvent);
});
```
function logEvent(event) {
	console.log(event.currentTarget.className);
}
```
```
 
- 캡쳐?:
 
  - 이벤트 캡쳐는 이벤트 버블링과 반대 방향으로 진행되는 이벤트 전파 방식
  
  ```js
<body>
	<div class="one">
		<div class="two">
			<div class="three">
			</div>
		</div>
	</div>
</body>
HTMLCopy
var divs = document.querySelectorAll('div');
divs.forEach(function(div) {
	div.addEventListener('click', logEvent, {
		capture: true // default 값은 false입니다.
	});
});

function logEvent(event) {
	console.log(event.currentTarget.className);
}
  ```
- addEventListener() API에서 옵션 객체에 capture:true를 설정해주면 됩니다. 그러면 버블링과 반대 방향으로 탐색을 합니다

**이벤트 위임의 장점은 무엇인가요?**
- 이벤트 위임은 실제 바닐라 JS로 웹 앱을 구현할 때 자주 사용하게 되는 코딩 패턴입니다.
- 이벤트 위임을 한 문장으로 요약해보면 ‘하위 요소에 각각 이벤트를 붙이지 않고 상위 요소에서 하위 요소의 이벤트들을 제어하는 방식’입니다.
- ex: 예를들어 나중에 input을 추가했는데 일일이 또 달아줘야할까? no/ class에 등록된것을 전부 불러오고 거기에 이벤트를 달아주면됩니다

캡처링은 어떨 때에 쓸 수 있을까요?

**클로저란 무엇인가요?** : https://velog.io/@hi4190/JSClosure-%ED%81%B4%EB%A1%9C%EC%A0%80

**클로저는 어떨 때에 쓰이나요?**

 - 상태 유지 : 현재 상태를 기억하고 변경된 최신 상태를 유지하는데 사용할 수 있다. 상태는 클로저가 소멸될 때까지 유지됩니다. 리액트의 useState를 생각해보자. 초깃값을 받아 setState외부의 변수에 저장해두고, 이를 변경하며 최신의 값으로 유지시키지않는가.

- 전역 오염 방지 : 외부 함수에 변수를 숨겨놓고 내부 함수에서 접근하도록 해서 의도치 않은 변경을 막을 수 있습니다. (외부 함수에 있는 변수는 그 밖에서는 접근할 수 없으므로)

- 정보 은닉 : 외부 함수에 this에 프로퍼티를 바인딩하지 않고 변수를 선언하면 내부 함수에서만 접근할 수 있는 private 키워드를 흉내낼 수 있습니다.

**이벤트 루프란 무엇인가요?**

 - 모든 코드는 실행을 누르면 스택에 쌓인다

스택이 비워져야 해결이 완성이되는데

콜백을 받아야할 요청건을 webapis로 보내지고 스택에선 제거가 된다

스택이 제거된후 webapis 쌓연던게 해결이되면

콜백큐로 넘어가게 되고 스택이 비워져있다면 

스택으로 이 콜백들이 넘어가고 실행이되고 스택이 사라진다

동기적 코드들이 너무 시간을 잡게 만들어서 비동기가 느리게 만들어선 안되겠다는 첫번재 생각이다


**프로토타입이란 무엇인가요?**

 - 원형, 나는 유전이라 부르겠다. 자바스크립트는 프로토타입을 지원하는데
 부모 객체가 있고 거기서 상속을 받을 수있다. 우리가 쓰는 sort(),length등
 전부 프로토타입 상속으로 받고 있는것이며 
 예를들어 
 ```js
let arr = new Array(1,2,3) 이라고 했을때 자바스크립트는 현재 Array라는 배열을 만들수 있는 기능이 존재한다 이것또한 상속으로 가져다 쓸수있는것이며

arr.sort()를 했을때 정렬이 될텐데 검사로 arr.prototype 이라는걸 해보면

sort()라는 것들이 포함되어있다 이것또 한 생성되면서 다른것들과 합쳐지고 유전으로 내려오는것들을 우리는 쓰고 있는것이다. 

무언가를 우리가 객체로 만들었을때 가져다 쓴다고 해보고 바로 윗단계에서 찾는게 없다면 계속 위로 올라가면서 찾게 된다 이것이 프로토타입체인이다
 ```

**프로토 타입의 장단점은 무엇인가요?**

장점 :
- 공통 되는 부분을 prototype에 정의 함으로써 재사용성이 높아지고, 메모리를 절약할 수 있다.

- 프로그래머 역량에 따라 무척이나 유연한 프로그래밍이 가능하다.

단점

- 없을거라고 판단했던 속성이 프로토타입에 있어서 예상치 못하게 동작할 수 있다. 즉, 정확성, 예측성 및 안정성이 클래스형 보다 떨어질 수 있음.

- class형에 익숙한 개발자들이 처음에 이해하기 어렵다.


**프로토타입을 실제로 사용해볼 일은 잘 없는데 어디에 사용할 수 있을까요?**
 
 - 항상 프로토타입을 쓰고 있다고 생각하면된다 왜냐하면 내장 함수들은 전부 프로토 타입 체인으로 이루어져 가져다가 쓰고있기때문이다
 - 직접 만들어서 쓸수있다 만들어져있는 객체에 .prototype 으로 수정을 해서 
  예를들어 .prototype.func 라고 1을 리턴하는 함수를 만들었다 치고 array.func() 이런식으로 수정해서 사용할수있다.


- **호이스팅은 무엇인가요?***

- 호이스팅은 함수가 실행되기전에 선언된 변수 들을 유효범위의 최상단으로 끌어올림을 말합니다. 또 한 자바스크립트 엔진은 이것들을 메모리에 먼저 탐색후 저장해줍니다
예를들어 
```js
console.log(a)
var a = 1
console.log(a)

```
를 실행한다고 했을때 자바스크립트에서는 첫번째를 undfined,2번쨰는 1이라고 출력해줍니다

이것은 호이스팅시 선언된것들을 초기화 시키는데 첫번째 콘솔로그는 아직 할당이 되지않았고 
2번째는 할당이 되기때문입니다 .

여기서 이제 let const가 나오게 됬을때 var는 초기화가 되지만 let과 const는 초기화가 되지않아서 호이스팅은되지만 참조에러를 발생해줍니다. 그래서 var는 정말 잘쓸수 있는 사람들빼고는 es6이후에는 잘 쓰지 않습니다.

또한 var는 함수만 지역변수로 호이스팅되고 나머지는 전부 호이스팅된다

**호이스팅은 개발자가 이해하기 어려운데 왜 만들었을까요? 일어나는 이유가 뭘까요?**

- 현재로써는 크게 도움이 안되지만 자바스크립트의 초창기 구동원리이고 
JS의 기본적인 동작 방식을 추상화한 것이기 때문에 사라지지 않고 남아있지 않나싶다.
공부하면 자바스크립트를 이해하는데 도움이 된다

- 호이스팅이 발생하는 원인은 자바스크립트 변수 생성과 초기화(선언과 할당)가 분리되어 진행되기 때문입니다.



**실행 컨텍스트란 무엇인가요?**

- 자바스크립트의 동적 언어로서의 성격을 가장 잘 파악할 수 있는 개념
- 실행 컨텍스트란 실행 코드에 제공할 정보들을 모아 놓은 객체입니다.
https://velog.io/@hi4190/Execution-Context%EC%8B%A4%ED%96%89%EC%BB%A8%ED%85%8D%EC%8A%A4%ED%8A%B8

**== 과 === 의 차이가 무엇인가요?**

 - 자바스크립트는 엄격한 비교와 유형변환 비교를 모두 지원하므로, 어떤 연산자가 어떤 비교조건에 사용되는지가
 - 중요하다. === 은 변수 유형을 고려하는 반면, == 는 변수 값을 기반으로 유형을 수정
 - 엄격한 관리를 위해서 === 을 쓰자
 - ex null 은 사용자가 임의로 없는값을 지정하는것이고 undfined는 엔진이 찾지 못하면 결정을 해준다 근데 ==은 뜻에 상관없이 없는값이기에 true를 해주는방면
 - === 은 false를 반환해준다

**NaN 과 NaN을 비교하면 어떻게 되나요? 어떻게 확인할 수 있나요?**

NaN 판별
NaN은 다른 모든 값과 비교(==, !=, ===, !==)했을 때 같지 않으며, 다른 NaN과도 같지 않습니다. NaN의 판별은 Number.isNaN() 또는 isNaN()을 사용하면 제일 분명하게 수행할 수 있습니다. 아니면, 오로지 NaN만이 자기자신과 비교했을 때 같지 않음을 이용할 수도 있습니다.

```js
NaN === NaN;        // false
Number.NaN === NaN; // false
isNaN(NaN);         // true
isNaN(Number.NaN);  // true

function valueIsNaN(v) { return v !== v; }
valueIsNaN(1);          // false
valueIsNaN(NaN);        // true
valueIsNaN(Number.NaN); // true
```
그러나 isNaN()과 Number.isNaN()의 차이를 주의해야 합니다. isNaN은 현재 값이 NaN이거나, 숫자로 변환했을 때 NaN이 되면 참을 반환하지만, Number.isNaN은 현재 값이 NaN이어야만 참을 반환합니다.
```js
isNaN('hello world'); // true
Number.isNaN('hello world'); // false
```
덧붙여서, 일부 배열 메서드는 NaN을 찾을 수 없습니다.

```js
let arr = [2, 4, NaN, 12];
arr.indexOf(NaN);                      // -1 (false)
arr.includes(NaN);                     // true
arr.findIndex(n => Number.isNaN(n));   // 2
```


**setTimeout(callback, 0) 은 어떻게 동작하나요?** : 이벤트 루프의 구동방식과 똑같다

**Promise란 무엇인가요? async await 또한**,

 - 자바스크립트의 비동기처리를 위한 객체입니다,또한 콜백 지옥을 피하기 위해 나온것이며 기존 콜백에서는 무조건 콜백함수 안에서 데이터 처리를 해야되서 데이터연결을 짓다가 콜배지옥을 많이 만나게 되지만 프로미스 객체가 나온뒤로는 피할수있습니다
 리졸브와 리젝티드 로 데이터와 에러를 내보낼수있고 then()처리로 데이터를 따로 처리할수 있습니다. 여기서
 더발전된 async await가 있는데 단점을 보완하고 가독성을 높이기 위해 나온 기술입니다. 프로미스에서도 비동기처리를 하려면
 콜백 처리를 해줘야하는데 asnyc await는 콜백처리를 따로 하지않아 가독성 면에서 매우 훌륭합니다.
 결론적으로 코드를 많이 줄일수 있습니다

**ES6에 추가된 문법에 대해 말해주세요.**

- 화살표 문법 : =>
- classes : 
  - ES6의 클래스는 프로토타입 기반 객체지향패턴을 더 쉽게 사용할 수 있는 대체재.
  - 익명 또는 기명일 수 있으며, 기명인 경우 클래스명은 본체에서 지역 범위임.

- Template Strings
  - 백틱을 사용해 문법적으로 string을 생성할수 있어서 간편함

- Destructuring(구조분해할당)
  - 배열이나 객체의 속성을 해체하여 거기에 있는 속성들을 개별적인 변수에 담을 수 있는 선언방식.
  - 배열과 객체에 패턴 매칭을 통한 데이터 바인딩을 제공함.
- Default, Rest, Spread 
  - Default parameters : 파라미터에 기본값 설정.
  
  - Rest parameters : -가변인자 사용가능, 배열로 치환. 다수의 값들을 배열로 묶어냄.(나머지들을 배열로 묶음)
  
 - Spread :
    
    - -함수 호출 시 배열을 일련의 인자에 나누어 주입. 하나의 입력값을 받을 때 유용.
 
 - let, const : var를 대체 좀더 명확한 변수 생성
 
 - For ... of문
   - 배열을 관리할때 포문처럼 사용해주는(Iterator 기반의 컬렉션 전용 반복문. 반복 가능한 객체를 대상으로 각 개별 속성값에 대한 반복문 수행.)
   
- JS Clousure : 윗 클로저 참조

**NULL 병합 연산자는 무엇인가요?**
?? 은 왼쪽 연산자가 null or undefined 라면 오른쪽 을 아니면 왼쪽을 반환 한다

**optional chaning의 장점은 무엇인가요?**
 - 남용한다면 디버깅이 어려워질수 있다 제일 앞의 오브젝트의 선언은 되어있는 상태에서 쓰자


**for of 는 어떻게 동작하나요?**
https://velog.io/@hi4190/for-...-of

**iterator에 대해 설명해주세요.**
https://velog.io/@hi4190/jsiterable

**generator에 대해 설명해주세요.**
https://velog.io/@hi4190/js%EC%A0%9C%EB%84%88%EB%A0%88%EC%9D%B4%ED%84%B0generator

**JS의 GC는 무엇인가요?**
가비지 컬렉션(쓰레기수집) 은 현재 엔진 안에서 실행되고 있는 코드들을 전부 순회를 해봅니다.
 - generational collection(세대별 수집) – 객체를 '새로운 객체’와 '오래된 객체’로 나눕니다. 객체 상당수는 생성 이후 제 역할을 빠르게 수행해 금방 쓸모가 없어지는데, 이런 객체를 '새로운 객체’로 구분합니다. 가비지 컬렉터는 이런 객체를 공격적으로 메모리에서 제거합니다. 일정 시간 이상 동안 살아남은 객체는 '오래된 객체’로 분류하고, 가비지 컬렉터가 덜 감시합니다.
- incremental collection(점진적 수집) – 방문해야 할 객체가 많다면 모든 객체를 한 번에 방문하고 mark 하는데 상당한 시간이 소모됩니다. 가비지 컬렉션에 많은 리소스가 사용되어 실행 속도도 눈에 띄게 느려지겠죠. 자바스크립트 엔진은 이런 현상을 개선하기 위해 가비지 컬렉션을 여러 부분으로 분리한 다음, 각 부분을 별도로 수행합니다. 작업을 분리하고, 변경 사항을 추적하는 데 추가 작업이 필요하긴 하지만, 긴 지연을 짧은 지연 여러 개로 분산시킬 수 있다는 장점이 있습니다.
- idle-time collection(유휴 시간 수집) – 가비지 컬렉터는 실행에 주는 영향을 최소화하기 위해 CPU가 유휴 상태일 때에만 가비지 컬렉션을 실행합니다.
등을 하면서 마크를 해나가고 도달할 수 없는(마크할수 없는) 객체들을 가비지컬렉션이 수집을하고 이것들을 메모리 상에서 지워 최상의 메모리 상태로 만들어 느려지지 않게 하는것입니다

GC의 순환참조 문제를 어떻게 해결할 수 있나요?

this란 무엇인가요?

apply, call, bind의 차이는 무엇인가요?

bind를 apply, call로 어떻게 구현할 수 있을까요? 구현해보세요.
그러면서 

throttle과 debounce에 대해 설명해주세요.

mutable과 immutable에 대해 설명해주세요.

불변하게 만들 수 있는 방법은 어떤게 있나요? Object.freeze 말고는 없나요?

CSS애니메이션과 JS 애니메이션의 차이는 무엇인가요?

requestAnimationFrame이 무엇인가요?

setTimeout이란 어떤 차이가 있길래 raf는 16fps를 보장할 수 있나요?

nodejs와 그냥 js의 차이점은 무엇인가요?

**웹팩이 뭔가요? 왜 사용하나요?**
https://velog.io/@hi4190/jswebpack

**바벨이 뭔가요? 왜 사용하나요?**
https://velog.io/@hi4190/js-%EB%B0%94%EB%B2%A8

polyfill이란 무엇인가요?

Promise나 async await를 es5로 트랜스파일하면 어떻게 되나요?

타입스크립트의 장점은 무엇인가요?

type과 interface의 차이는 무엇인가요?

어떨 때에 JS를 쓰고 어떨 때에 TS를 쓰는 것이 좋을까요?

enum은 무엇인가요? object와의 차이점은?

React 관련
여러 프레임워크들이 있는데 왜 React를 쓰셨나요?

React의 라이프사이클에 대해 설명해주세요.

React의 장점은 무엇이있나요?

virtual Dom에 대해 설명해주세요.

virtual dom은 트리가 바뀐지 어떻게 비교하나요?

hook이 뭔가요? 일반 함수랑 어떤차이가 있나요.

state를 왜 쓰나요? 그냥 변수를 쓰는 것과 어떤 차이가 있나요?

React의 key는 무엇인가요?

useEffect에 대해 설명해주세요.

useEffect의 두번째 인자인 dependecny는 어떻게 바뀌었는지 비교 하나요?

useCallback, useMemo 차이는 무엇인가요?

React.memo란?

리액트의 에러바운더리에 대해 아시나요?

함수 컴포넌트의 장점이 무엇인가요?

함수형 컴포넌트라고 안 부르고 함수컴포넌트라고 부르는데 그 이유가 무엇인가요?

SSR과 CSR의 차이는 무엇인가요? 어느 것이 더 속도가 빠른가요?

Next.js 처럼 서버에서 렌더링을 할 경우 부하가 많아지면 어떻게 해결 할 수 있을까요?

왜 Redux를 쓰셨나요?

Redux와 Mobx 중에 Redux를 쓰신 이유? (또는 Mobx를 쓴 이유)

Redux 미들웨어는 뭐 쓰셨나요?

미들웨어를 만들어본 적 있나요?

thunk와 saga의 차이는 무엇인가요?

saga의 장단점은 무엇인가요?

웹 관련
URL을 입력했을 때 어떤식으로 동작하게 되나요?

index.html을 읽어서 그려지는 과정을 설명해주세요.

해당 과정에서 병목현상이 일어나는 구간이 어디인가요?

Reflow, Repaint에 대해 설명해주세요.

최적화를 하는 방법에 어떤 것들이 있을까요?

이미지 스프라이트란 무엇인가요?

크로스 브라우징 어떻게 하나요?

http란 무엇인가요?

http method에 대해 설명해주세요.

REST API란 무엇인가요?

http 1.1 과 http 2.0의 차이는 무엇인가요?

쿠키, 로컬스토리지, 세션스토리지 차이는?

쿠키세션, JWT, OAUTH에 대한 내용

메신저 앱에서 메시지를 보낸 다음 서버에서 어떤 방식으로 모든 방 사람들에게 뿌려줄 수 있는걸까요?

XSS, CSRF는 무엇인가요?

하드웨어 가속이란?

프로젝트 관련
왜 해당 기술을 썼나요?

로그인 처리는 어떻게 하셨나요?

팀원간의 불화는 없었나요? 갈등은 어떻게 해결했나요?

어떤 역할을 하셨나요?

가장 어려웠던 부분은 어디인가요?

어떤 기술적인 고민을 하셨나요?

최적화에 대해 신경써보셨나요?

자신의 기여도가 얼마정도 된다고 생각하는지?

팀원에게 받은 긍정적/부정적 피드백은?

약간의 기술? + 인성 관련
자기소개

롤 모델이 있나요? (개발자든 비개발자든 상관없습니다.)

우리 팀에 들어와서 몇 년뒤 당신의 축하파티가 열렸다면 어떤 일일 것 같나요?

우리 팀에 들어와서 어떤 일을 하고 싶나요?

최근에 가장 관심 있는 기술은 무엇인가요?

팀원 간의 갈등이 있을 때 어떻게 해결할 것인가요?

다른 팀원의 잘못된 코드를 봤을 때 어떻게 할 것인가요?

팀원이 계속해서 자기게 맞다고 우기면 어떻게 할 것인가요?

취미는 무엇인가요?(개발 빼고)

어떤 분야(핀테크, 소셜, 게임, 커머스 등)에 많이 지원하셨나요?

다른 회사에도 지원을 하셨나요?

자신의 장단점에 대해 말해주세요.

살면서 가장 힘들었던 일이 무엇인가요?

자신은 누군가에게 도움을 주는 사람이었나요? 어떤 도움을 주었나요?

반대로 누군가 자신에게 가장 도움이 됐던 일은 무엇인가요?

커리어의 목표가 무엇인가요?

왜 프론트엔드 개발자가 되고 싶으신가요?

프론트엔드 개발자에게 가장 중요한 것은 무엇이라고 생각하시나요?

빠른 코드와 가독성 높은 코드 중에서 어떤 것을 택하실 건가요?

어떤 개발자가 좋은 개발자일까요?

리더형인가요? 팔로우형인가요?

가장 재밌었던 전공 과목은 무엇인가요?

페어프로그래밍, 코드리뷰에 대한 생각

백엔드도 해보셨나요?

도커, 쿠버네티스 사용해보셨나요?

함수형 프로그래밍이란 무엇인가요?

테스트에 대해 어떻게 생각하나요? 꼭 해야 하나요?

왜 당신을 뽑아야하나요?

열심히 일하는 편인가요? 영리하게 일하는 편인가요?

영어 강의를 본적이 있나요? 최근에 본 영어 강의는?

자바스크립트 어떻게 공부했나요?

개발이 재밌어서 하는 건가요?

배포는 해보았나요? 어떤식으로 해봤나요?

자신이 어느정도의 실력이라고 생각하시나요?

개발말고 다른 것에 열정적으로 해본 것이 있나요?

개발자가 사용자의 ux를 향상 시키기 위한 방법은 어떤 것이 있나요?


