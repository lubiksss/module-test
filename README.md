* https://wormwlrm.github.io/2020/08/12/History-of-JavaScript-Modules-and-Bundlers.html
* nodejs는 기본적으로 모듈 형태로 commonjs를 사용한다.
* 그러나 ES6이상에서 제공하는 import/export를 사용하고 싶다면 package.json에 type: module을 추가해주면 된다.
* html위에서는 기본적으로 commonjs, ESM모두 사용할 수 없다.
* 하지만 src태그에 type: module을 추가하면 html에서도 ESM을 사용할 수 있다.
* module문제는 babel이랑 다른 문제이다. babel은 ES6이상의 문법을 ES5이하의 문법으로 변환해주는 도구일뿐 모듈관련 개념이 아니다.
* 기본적으로 브라우저에 디펜던시가 얽힌 js코드를 첨부할때는 번들링하는게 좋다.
* browserify는 ESM이 정의되기 전에 만들어져서 import/export를 지원하지 않는다.
* 어쨋거나 commonjs든 ESM이든 디펜던시가 얽힌 js코드를 첨부하려면 웹팩을 쓰자
* 웹팩은 모듈 번들러이다. 모듈 번들러는 모듈을 하나의 파일로 합쳐주는 도구이다.