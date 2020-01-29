# Quest 01. Hello, HTML


## Introduction
* HTML은 HyperText Markup Language의 약자로, 웹 브라우저에 내용을 표시하기 위한 가장 기본적인 언어입니다. 이번 퀘스트를 통해 HTML에 관한 기초적인 사항들을 알아볼 예정입니다.

## Topics
* 브라우저의 역사
  * Mosaic
  * Netscape
  * Internet Explorer
  * Firefox
  * Chrome
  * Safari (for iOS)
  * Edge
* HTML 표준의 역사
  * HTML 4.01
  * XHTML 1.0, XHTML 1.1
  * XHTML 2.0
  * HTML5
    * HTML 5.3
* HTML 문서의 구조
* HTML 문서의 엘리먼트
  * Semantic elements
  * Block-level elements vs Inline elements

## Resources
* [MDN - HTML](https://developer.mozilla.org/ko/docs/Web/HTML)
* [모던 웹 디자인을 위한 HTML5+CSS3 입문](http://www.yes24.com/24/Goods/15683538?Acode=101), 한빛미디어
* [웹 디자인 2.0 고급 CSS](http://www.yes24.com/24/Goods/2808075?Acode=101), 에이콘출판사
* [StatCounter Global Stats](http://gs.statcounter.com/)

## Checklist
* HTML 4.x 이후의 HTML 표준의 변천사는 어떻게 되나요?

  * 이후 HTML 4.01 - XHTML 1.0(HTML 4,01을 XML로 다시 규정) - XHTML 1.1 - XHTML 2.0(하위 호환성 문제) - HTML 5(브라우저 업체들이 별도의 웹 표준을 제안하기 위해 WHATWG를 설립, Web Application 1.0을 제안하여 이를 기초로 HTML Working Group을 출범, 표준안의 명칭 HTML 5로 변경.)

* MS와 IE는 왜 역사에 오점을 남기게 되었을까요?

  * 

* `<section>`과 `<div>`, `<header>`, `<footer>`, `<article>` 엘리먼트의 차이점은 무엇인가요?

  * `<section>`, `<header>`,`<footer>`,`<article>`은 HTML 5에서 새롭게 추가된 태그, `<div>`포함해서 모두 블럭 레벨 엘리먼트.
  * `<section>`은 관련있는 내용을 묶어 표시, `<artcle>`은 관련성을 가지면서 동시에 독립적으로 의미를 가질 때 사용, `<header>`는 머리말, `<footer>`는 꼬리말의 역할 `<div>`는 단순한 영역 구분시 사용.

* 블럭 레벨 엘리먼트와 인라인 엘리먼트의 차이는 무엇일까요?

  * 블럭 레벨 엘리먼트 - 차지하는 부분이 줄 전체로, 블럭 요소 태그 사용 시 자동 줄넘김이 생김
  * 인라인 엘리먼트 - 컨텐츠 내용만큼의 영역을 차지, 나머지 공간에 다른 요소가 올 수 있기 때문에 한 줄에 여러 인라인 요소 표시 가능
  * display 속성으로 변경 가능

## Quest
* [이 그림](github.png)은 github의 웹사이트 레이아웃입니다. 이 레이아웃의 정보를 HTML 문서로 표현해 보세요.
* CSS를 전혀 사용하지 않고, 문서의 구조가 어떻게 되어 있는지를 파악하여 구현해 보세요.
  * [CSS Naked Day](http://meiert.com/en/blog/20150319/css-naked-day/)는 매년 4월 9일에 CSS 없는 웹 페이지를 공개하여 내용과 마크업에 집중한 HTML 구조의 중요성을 강조하는 행사입니다.
* 폴더에 있는 `skeleton.html` 파일을 바탕으로 작업해 보시면 됩니다.
