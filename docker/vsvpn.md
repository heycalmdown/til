# Docker vs VPN

## 진퇴양난

* VPN을 split tunneling으로 켜면 /etc/resolv.conf가 바뀌지 않는다
* 이 상태에서 docker-machine을 다시 띄우면 컨테이너 안에서 회사망에 접속할 수 없다
* VPN을 full tunneling으로 켜면 search domain과 dns가 바뀐다
* 이 상태에서 docker-machine을 다시 띄우면 VPN과 NAT의 충돌 때문에 도커 서버에 연결되지 않는다

## 해결

* full tunneling으로 docker-machine을 띄운 뒤에 VPN을 다시 split으로 바꾸면 되지롱
