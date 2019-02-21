# Racket

![Logo](https://upload.wikimedia.org/wikipedia/commons/8/8c/Racket-logo.png)

* LISP-Scheme 계열의 방언(DrScheme = DrRacket)
* [공식 페이지](https://racket-lang.org) - 좀 늙어보인다
* [공식 문서](https://docs.racket-lang.org) - 굉장히 잘 돼 있다. 검색도 편하지만 뭘 찾아야될지 모를 때는 구글에서 그냥 racket 키워드를 포함해서 찾으면 잘 나온다
* [유저 그룹](https://groups.google.com/forum/?hl=en#!forum/racket-users)
    * 아재들답게 당당하게 [메일링 리스트](https://lists.racket-lang.org)를 소개하고 있다
    * 심지어 gmane mirror 링크는 다 깨져있다
    * IRC와 Slack이 있는데 냄새나서 IRC는 안 들어가봄
* Online book - [Beautiful Racket](https://beautifulracket.com)
* [awesome-racket](https://github.com/avelino/awesome-racket)

## 첫인상

* 아재 냄새 난다
* 그런 것 치고는 `raco`가 꽤 훌륭하다
* 오래된 언어라서 그런지 core library가 충실하다
* 패키지 설치도 빠르다
* 언어를 [쉘 스크립트로 사용](https://docs.racket-lang.org/guide/scripts.html)할 수도 있고, [REPL](https://docs.racket-lang.org/xrepl/index.html)도 있고, 즉시 실행할 수도 있고, 바이너리로 굽는 것도 간단하다

## 주의

* Racket은 언어일 뿐 아니라 언어 해석기이다
* Racket으로 실행할 수 있는 언어가 [Racket 만이 아니기 때문에](https://www.reddit.com/r/Racket/comments/29ag9o/list_of_racket_languages/) 검색 결과에 주의하자 - 좋은 함수를 찾았다고 생각했지만 언어가 다를 수 있다
* 심지어 초반에 나오는 [The Racket Guide](https://docs.racket-lang.org/guide/languages.html)에서 새로운 언어를 만드는 법을 소개하고 있다
* [패키지](https://pkgs.racket-lang.org/index.html)가 많지 않다 (1000여개)


## 설치

```bash
$ brew cask install racket
```

* cask를 빼먹고 `brew install` 하면 `minimal-racket`이 깔린다

## 기본

### racket

```bash
$ racket
Welcome to Racket v7.2.
>

$ racket hello.rkt
world
```

* racket은 인터랙티브 쉘을 포함한 실행 명령(=python =node)

### raco

  raco: Racket Command-Line Tools

```bash
$ raco pkg install xrepl-lib
Resolving "xrepl-lib" via https://download.racket-lang.org/releases/7.2/catalog/
Using cached15505514171550551417269 for https://download.racket-lang.org/releases/7.2/pkgs/xrepl-lib.zip
raco pkg install: package is currently installed in a wider scope
  package: xrepl-lib
  installed scope: installation
  given scope: user

$ raco exe hello.rkt
$ ./hello
world
```

* (=pip =npm)
* REPL이 원체 꼬졌기 때문에 `xrepl`을 꼭 깔아주자
    * 얼마나 꼬졌냐면 `^p`나 `^n`도 심지어 방향키도 안 먹는다
* 패키지 이름이 packagename-lib 형태로 되어 있다. 문서에는 packagename까지만 나와 있으니 주의
    * xrepl -> xrepl-lib
    * threading -> threading-lib
