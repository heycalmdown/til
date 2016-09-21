https://docs.docker.com/engine/reference/builder/#/add

느린 디스크가 붙어있거나 호스트와의 IO 성능이 좋지 않은 가상 머신에서 빌드할 때는 .dockerignore를 아무리 덕지덕지 잘 써놔도 오래 걸린다. 이럴 때는 그냥 빌드 컨텍스트를 화이트리스트로 찍어서 STDIN으로 넣어주는게 빠르다.

```
$ tar -zcvf aa.context.tar.gz Dockerfile xxx/xxx yyy/yyy zzz
$ docker build - < aa.context.tar.gz

