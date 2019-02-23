# Hello, world

```racket
#!/usr/bin/env racket
#lang racket/base
"hello, world"
```

Racket 코드는 다음 세 가지 방법으로 실행 가능하다

* 쉘 스크립트
* 인터프리터
* 바이너리

## Shell script

```bash
$ chmod +x hello.rkt
$ ./hello.rkt
"hello, world"
```

* 소스 코드의 첫 줄인 `#!/usr/bin/env racket`에 의해 즉시 해석된다

## 인터프리터

```bash
$ racket hello.rkt
"hello, world"
```

## 바이너리

```bash
$ raco exe hello.rkt
$ ./hello
"hello, world"
```

의존하는 모듈을 모두 바이너리에 때려넣기 때문에 사이즈를 관리하는 것이 중요하다.

* `#lang racket` -> 7.7MB
* `#lang racket/base` -> 1.2MB
* racket/base + racket/list -> 1.3MB
* racket/base + racket/system -> 1.2MB
* racket/base + json -> 5.1MB
* racket/base + threading -> 4.9MB
* racket/base + json + threading -> 5.2MB
* racket(base + list + list) + json + threading -> 5.2MB

아래는 다양한 라이브러리를 사용하는 예제

```racket
#lang racket/base
(require json threading racket/list racket/system)
(~>  "curl https://api.github.com"
  process
  first
  read-json
  (hash-ref 'current_user_url))
```

그리고 실행 결과

```bash
$ ./github  
"https://api.github.com/user"
$ ll -h github
-rwxr-xr-x  1 kson  263744041   5.2M Feb 21 09:24 github
```
