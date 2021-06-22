# Git basic

git의 기초를 배워요



## WARNING

1. Home폴더(~)를 리포로 업그레이드 하지 않는다.
2. 리포안에 리포를 만들지 않는다. (리포 안의 폴더에서 `git init`하지 않는다)

## 저장소 초기화 하기

```
$ git init
```

폴더를 '리포'로 업그레이드

부모가 리포면 자식도 리포

.git 처럼 . 으로 시작되는 이름은 숨김처리 되있음

##  저장소를 일반 디렉토리로 되돌리기

```
$ rm -rf .gif
```



## STAGE에 올리기 (staging)

특정 파일만 스테이지에 올리기

```
$ git add 파일명.확장자
```

현재 위치의 모든 파일을 스테이지에 올리기

```
$ git add .
```



## commit을 통해 스냅샷 저장하기

```
$ git commit -m '남길 메세지'
```



## vim <파일이름>으로 편집기로 이동

1. [i] 눌러 편집모드
2. 편집
3. [esc] 눌러서 명령모드
4. :w 입력후 enter -> 저장
5. :q , enter ->  종료
6. :wq , enter -> 저장&종료
7. :q   ,   enter -> 강제종료



## 현재 상태 확인하기

```
$ git status
```

- 빨간색으로 표시되는 파일은 commit에 포함되지 않음

- 초록색으로 표시되는 파일은 commit에 포함 됨
- 변경사항이 없는 파일은 표시되지 않음



##  커밋 로그 확인하기

```
$ git log
```



## 주요 구문

- `cd ..`         ---부모 디렉토리가기
- `cd  (원하는 디렉토리 주소)`  --- 원하는 디렉토리가기
- `touch`                                --- 파일 만들기
- `mkdir`                                ---새로운 디렉토리 만들기
- `start  파일이름`   파일실행
- `rm`     파일 지우기, 휴지통 거치지 않고 삭제
- `-`       Optional한 표현
- `touch start rm^c`
- `mkdir cd rm -r^c`  

## 리모트 연결하기

```
$ git remote add <name> <URL>

# 리모트 삭제하기
$ git remote remove <name>

# 리모트 이름바꾸기
$ git remote rename <old-name> <new-name>
```



## 리모트에 PUSH하기

리모트에 업로드

```
$ git push <name> <branch>
```



## 리모트에서 최초 CLONE 받기

리모트 리포 내용을 그대로 복제

```
$ git clone <URL>
```



## 리모트에서 PULL 하기

리모트에서 다운로드

