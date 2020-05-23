# Set Faster Repository

Ubuntu를 처음 설치하면 인터넷 환경에따라 업데이트 속도가 느리다.

통신이 원활한 저장소로 바꾸어 주면 해결 할 수 있다.

대체로 mirror.kakao.com을 쓰는데, 다른 mirror 저장소도 테스트하여 자신에게 맞는 저장소를 택하자.



sed 명령어를 통하여 빠르게 저장소를 바꿀 수 있다.

`s/[찾을 문자열]/[바꿀 문자열]/`로 문자열을 바꿀 수 있고 `g`를 통해 모든 라인에 적용 할 수 있다

```text
sed -i 's/kr.archive.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list
sed -i 's/security.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list
sed -i 's/extras.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list

# kr이 빠진 경우도 있다
sed -i 's/archive.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list
```

