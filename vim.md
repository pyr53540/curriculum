# Vim
터미널에서 사용되는 텍스트 에디터중 하나입니다.
리눅스, macOS에 기본적으로 설치되어있기 때문에 익혀두면 좋습니다.
입력에 필요한 기본적인 기능만 익혀보겠습니다.

### 파일생성

```
$ vim test.sh
```

#### 커서이동
- j : 아래로
- k : 위로
- h : 앞으로
- l : 뒤로

#### 입력모드
`i` 키를 누르면 입력을 할 수 있습니다.

#### 검색
esc 를 누릅니다.
```
/검색어
```
를 타이핑 합니다. `n`키를 눌러서 다음 검색어로 이동이 가능합니다.

#### 줄이동
esc를 누릅니다. 아래처럼 타이핑하면 100째 줄로 이동됩니다.
```
:100
```

#### 선택
Shift + v

#### 잘라내기
선택된 상태에서 `x`

#### 붙혀넣기
이미 선택된 문장이라면 `p`

#### 삭제
`d`

#### 줄삭제
빠르게 `dd` 를 누릅니다.

#### 반복
`.`을 누르면 전에 했던 행동이 반복 됩니다.

#### 종료
esc키를 누릅니다.
```
:q
:wq
```


#### Reference
- Vim 책중에 유명한 책 입니다. https://www.amazon.com/Practical-Vim-Edit-Speed-Thought-ebook/dp/B018T6ZVPK/ref=sr_1_1?s=digital-text&ie=UTF8&qid=1540733339&sr=1-1&keywords=vim