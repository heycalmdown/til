[doc.angularjs.org](https://docs.angularjs.org/api/ng/type/$rootScope.Scope)

$emit하고 $broadcast 차이가 뭔지 야밤에 디버깅 하다가 갑자기 궁금해져서 검색해봤다.

* $emit()은 현재 스코프에서 시작해서 부모로 전파된다
* $broadcast()는 현재 스코프에서 자식으로 전파된다
