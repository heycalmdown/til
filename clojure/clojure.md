# 자료 구조 읽고 쓰기

```clojure
(edn/read-string (slurp "xxx.edl"))
(spit "xxx.edl" (pr-str xxx))
```

# keyword as a function

```clojure
(def xx {:a "a" :b "B"})
(xx :a)
(:a xx)
```

둘 다 "a"를 반환하는데 '키워드를 함수로 쓰는 게 좋다'고 어디서 들었다. 이유를 몰랐는데 자료 구조가 외부에서 전달될 경우 nil 일 수 있어서 그럴 경우 nil을 함수로 쓰면 `NullPointerException`이 나니까. 라는 것이었음.
