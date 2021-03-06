# ldd

Python 언어를 마스터하고 이후 여러분이 컴파일 언어를 다루는 프로젝트에 일할 때쯤 ldd를 자주 사용하게 될것 같습니다.
ldd는 실행파일과 연관된 라이브러리를 출력하는 명령어예요.

우리가 자주 사용하는 `ls` 명령어가 있습니다.
이 명령어가 사용하는 라이브러리 한번 확인해보죠.

```bash
$ /bin
$ ldd ls
```

결과는 아래와 같이 출력됩니다.
```
	linux-vdso.so.1 =>  (0x00007ffe99e74000)
	libselinux.so.1 => /lib64/libselinux.so.1 (0x00007f5df9a9d000)
	libcap.so.2 => /lib64/libcap.so.2 (0x00007f5df9898000)
	libacl.so.1 => /lib64/libacl.so.1 (0x00007f5df968f000)
	libc.so.6 => /lib64/libc.so.6 (0x00007f5df92c2000)
	libpcre.so.1 => /lib64/libpcre.so.1 (0x00007f5df9060000)
	libdl.so.2 => /lib64/libdl.so.2 (0x00007f5df8e5c000)
	/lib64/ld-linux-x86-64.so.2 (0x00007f5df9cc4000)
	libattr.so.1 => /lib64/libattr.so.1 (0x00007f5df8c57000)
	libpthread.so.0 => /lib64/libpthread.so.0 (0x00007f5df8a3b000)
```

과거에 설치된 제가 만든 trans 라고 하는 명령어도 ldd 테스트를 해보겠습니다.
```
$ ldd ~/bin/trans
```

결과는 아래와 같습니다.
```
	동적 실행 파일이 아닙니다.
```

용량을 체크해보면 약 6.5메가정도의 실행파일입니다.
```
-rwxr-xr-x   1 woong woong 6.5M 10월  7 21:51 trans
```

trans는 명령어를 실행하기위해 필요한 추가 라이브러리가 실행파일 내부에 내장되어있습니다.
이 뜻은 trans 명령어 자체 하나로 프로그램이 잘 돌아간다는 뜻이며 저는 이런 특징을 위해서 trans 명령어를 제작할 때 Go라는 언어를 이용해서 프로그래밍 했습니다. 일반적으로 저는 간단한 것들은 Python을 이용하지만 오래 두고 써야하는 프로그램들은 의존성을 위해서 Go로 작성하는편 입니다. 모든 OS에서 오래 두고(어쩌면 평생..) 사용할 수 있기 때문이죠. 저는 클라우드를 준비하기 위해서 Go를 배웠었어요. 여러분도 추후 이런 기술들에 관심이 간다면 한번 배워보세요.

우리는 현재 파이썬을 이용해서 대부분의 수업을 배우고 있지만 이러한 특징에 대해서 관심이 생긴다면 꼭 Go 언어도 다루어보길 희망합니다.