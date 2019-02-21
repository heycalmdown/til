# ReasonML

이 주제에 대해서는 특별히 시간순으로 쓴다.

![reason](https://reasonml.github.io/img/reason.svg)

## 함수형 언어

* 함수형 언어를 평소에 자주 써서 손에 붙여놓고 싶었다
* 언젠가 뭔가 해야할 일이 생길 때 바로 꺼내쓸 수 있도록
* 자주 쓰려면 가장 좋은 방법은 쉘 스크립트 대용으로 쓰는 것이다
* 그 전에 공부하던 언어는 [Clojure](https://github.com/heycalmdown/til/tree/master/clojure)인데 (언어 자체는 재밌었지만) 기동 속도 때문에 닭 잡기에는 너무 큰 칼이었다

## 대안들

* 의외로 Elixir가 빨랐다 - Erlang과 VM을 노나 쓰기 때문에 Clojure 만큼은 아니라도 풍부한 라이브러리가 제공됐다
* ReasonML - 페이스북에서 만들고 있고, 컴파일 속도가 매우 빠르며, JavaScript 또는 OCaml과 생태계를 공유하고 있다
* [Racket](../racket/README.md) - 좀 고루한 느낌이고 최초에는 생각이 안 났음
 
## 좋은 첫인상

* 함수형 언어들이 CS 박사님들이 나이가 들어선지 취향이 늙어선지 전반적으로 웹페이지가 고루한 편
* Reason은 [깔끔한 느낌](https://reasonml.github.io)
* 구닥다리 IDE들 대신 vscode에 찰떡같이 잘 붙는다
* 페이스북에서 만들고 있다
* 컴파일 언어이고, 컴파일이 빠르며, incremental build 할 때 매우 빠르다
* JavaScript로 transpile 되거나, Native로 컴파일 할 수 있다
* JavaScript로 transpile 되는 경우 npm을 쓸 수 있고, Native일 경우 OCaml 생태계를 활용할 수 있다
* 원래 이름은 Reason인데 너무 일반적인 단어라서 필요하면 ReasonML이라고 부르는 듯(Go와 golang의 관계처럼)

## 참고할만한 페이지

* [메인 페이지](https://reasonml.github.io)
* [Q&A 포럼](https://reasonml.chat)
* [그 외 커뮤니티](https://reasonml.github.io/docs/en/community)
* ReasonML 팀에서 직접 만든 코드는 [여기](https://github.com/reasonml)
* 커뮤니티에서 만든 코드는 [여기](https://github.com/reasonml-community)
* 깊이 들여다보려면 [Exploring ReasonML](http://reasonmlhub.com/exploring-reasonml/toc.html)
* Reason 전용 [npm 패키지 - Redex](https://redex.github.io)
* 괜찮은 [블로그](https://til.hashrocket.com/reasonml)
* [awesome-reasonml](https://github.com/vramana/awesome-reasonml)

## 재밌다!

* 문서가 굉장히 잘 되어 있다
* [What & Why](https://reasonml.github.io/docs/en/what-and-why) 부터 따라가며 다 읽으면 굉장히 재밌는 시도라는 게 느껴진다
* 언어를 만들면서 어떤 고민을 했고 왜 이런 선택을 했는지 잘 나와 있어서 흥미롭다
* Reason은 OCaml과 거의 같은 언어이다
* 의미적으로는 완전히 동일하며(같은 AST를 사용), 문법적으로만 20% 정도 차이난다
* 많은 선택지에서 매일매일의 업무에 바로 도움이 될 수 있도록 결정했다
* JavaScript로 번역되게 한 결정이나 NPM 툴체인을 그대로 쓸 수 있게 한 것도 당장 쓸 수 있게 하려고 했던 결정이다
* 페이스북 [Messenger](messenger.com)의 50%를 2017년에 이미 [Reason으로 다시 썼다고](https://reasonml.github.io/blog/2017/09/08/messenger-50-reason) 한다
* 페이스북이 [immutable-js](https://github.com/immutable-js/immutable-js)를 만들었던 것이나, [React](https://reactjs.org)의 핵심이 불변성인 것과도 잘 어울린다
* [React](https://reasonml.github.io/docs/en/what-and-why#why-ocaml-as-the-backing-language-why-not-my-favorite-language)와 Reason의 창시자가 동일하다
* React와 Reason의 철학이 서로 잘 맞기 때문에 [ReasonReact](https://reasonml.github.io/reason-react/)가 개발되고 있다

## 걸림돌

세상에 좋은 일만 있을 순 없겠죠?

* [BuckleScript](https://bucklescript.github.io)를 알아야 한다
  * OCaml 언어를 JavaScript로 번역해주는 컴파일러이자 환경
  * Reason과 OCaml이 거의 같은 언어이므로 BuckleScript는 Reason 컴파일러이기도 하다
  * 처음에는 애써 무시하고 시작해봤지만 많은 곳에서 막힌다
  * 그냥 BS는 내 친구라고 생각하고 시작하는 게 좋겠다
* Native 컴파일 가능하다는 건 말이 그렇다는 것이다
    * Reason과 OCaml이 거의 같은 언어이고 OCaml은 바이너리를 생성하는 언어이므로 말이 그렇다는 것이다
    * OCaml 개발 환경에서 문법만 Reason을 사용해야 한다
    * 툴체인이 아직 [초보 단계다](https://reasonml.github.io/docs/en/native?fbclid=IwAR3rJeK34C5ejv1EnNcQzGc2czcyqZsozRrryuWFvEqi0asz07jOmeiGqow)
    * 그럴거면 그냥 OCaml을 쓰자
    * 불길을 한 번 지나가보려면 아래를 참고
        * https://esy.sh
        * https://github.com/jordwalke/pesy
        * https://github.com/reasonml/ReasonNativeProject
        * https://opam.ocaml.org/packages/
* 둘 다 지원한다고 해서 동시에 쓸 수 있다는 말은 아니다
    * Clojure와 ClojureScript를 공부하면서도 같은 것을 느꼈는데
    * 언어가 다양한 Backend를 지원한다는 것을 주의할 필요가 있다
    * 같은 코드가 돌아가긴 하지만 라이브러리는 한 쪽만 쓸 수 있다
    * 대부분의 코드를 직접 짜지 않는 한 타겟을 하나만 정해서 쓰는게 속 편하다
* 기존의 생태계를 사용할 수 있다는 것이 쉽다는 뜻은 아니다
    * Clojure가 JVM에서 돌아가기 때문에 방대한 Java 패키지를 공짜로 얻을 수 있었지만, 패러다임 차이 때문에 쉽지 않았다
    * Reason에는 패러다임 차이에 더해 타입 문제까지 있다
    * Reason은 오래 검증된 완전한 타이핑이 강점이다
    * JavaScript에는 타입이 없다
    * [DefinitelyTyped](https://github.com/DefinitelyTyped/DefinitelyTyped)와 [Flow](https://flow.org)의 대결에서 장렬히 패배했던 기억이 떠오른다

## 쉘 스크립팅

그래도 한 번 써보자

* 쉘 스크립트 대신 써야 하니까 핵심은 subprocess 실행

```Reason
Node.Child_process.execSync("ls", Node.Child_process.option(~encoding="utf-8", ())) -> Js.log
```

그만 써보자...
