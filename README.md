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
  ```
- addEventListener() API에서 옵션 객체에 capture:true를 설정해주면 됩니다. 그러면 버블링과 반대 방향으로 탐색을 합니다

**이벤트 위임의 장점은 무엇인가요?**
- 이벤트 위임은 실제 바닐라 JS로 웹 앱을 구현할 때 자주 사용하게 되는 코딩 패턴입니다.
- 이벤트 위임을 한 문장으로 요약해보면 ‘하위 요소에 각각 이벤트를 붙이지 않고 상위 요소에서 하위 요소의 이벤트들을 제어하는 방식’입니다.
- ex: 예를들어 나중에 input을 추가했는데 일일이 또 달아줘야할까? no/ class에 등록된것을 전부 불러오고 거기에 이벤트를 달아주면됩니다

캡처링은 어떨 때에 쓸 수 있을까요?

클로저란 무엇인가요?

클로저는 어떨 때에 쓰이나요?

이벤트 루프란 무엇인가요?

프로토타입이란 무엇인가요?

프로토 타입의 장단점은 무엇인가요?

프로토타입을 실제로 사용해볼 일은 잘 없는데 어디에 사용할 수 있을까요?

호이스팅이 무엇인가요?

호이스팅은 개발자가 이해하기 어려운데 왜 만들었을까요? 일어나는 이유가 뭘까요?

실행 컨텍스트란 무엇인가요?

== 과 === 의 차이가 무엇인가요?

NaN 과 NaN을 비교하면 어떻게 되나요? 어떻게 확인할 수 있나요?

setTimeout(callback, 0) 은 어떻게 동작하나요?

Promise란 무엇인가요? async await 또한,

ES6에 추가된 문법에 대해 말해주세요.

NULL 병합 연산자는 무엇인가요?

optional chaning의 장점은 무엇인가요?

for of 는 어떻게 동작하나요?

iterator에 대해 설명해주세요.

generator에 대해 설명해주세요.

JS의 GC는 무엇인가요?

GC의 순환참조 문제를 어떻게 해결할 수 있나요?

this란 무엇인가요?

apply, call, bind의 차이는 무엇인가요?

bind를 apply, call로 어떻게 구현할 수 있을까요? 구현해보세요.

throttle과 debounce에 대해 설명해주세요.

mutable과 immutable에 대해 설명해주세요.

불변하게 만들 수 있는 방법은 어떤게 있나요? Object.freeze 말고는 없나요?

CSS애니메이션과 JS 애니메이션의 차이는 무엇인가요?

requestAnimationFrame이 무엇인가요?

setTimeout이란 어떤 차이가 있길래 raf는 16fps를 보장할 수 있나요?

nodejs와 그냥 js의 차이점은 무엇인가요?

웹팩이 뭔가요? 왜 사용하나요?

바벨이 뭔가요? 왜 사용하나요?

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





