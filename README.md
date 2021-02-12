# git101

##  커밋 취소법

### 가장 간단한 명령어
```
$ git reset HEAD~1
```

### 상세 내용

```
 
//  commit을 취소 + 파일들은 staged 상태로 보존
$ git reset --soft HEAD^

//  commit을 취소 + 파일들은 unstaged 상태로 보존
$ git reset --mixed HEAD^ // 기본 옵션
 
// 위와 동일
$ git reset HEAD^ 

// 위와 동일(한것으로 추정됨)
$ git reset HEAD~1

$ git reset HEAD~2 // 마지막 2개의 commit을 취소

// commit을 취소 + 파일들은 unstaged 상태 작업 폴더에서 모두 제거
$ git reset --hard HEAD^
```
참고: https://gmlwjd9405.github.io/2018/05/25/git-add-cancle.html


```
git reset --soft
```
HEAD^ will remove last local (unpushed) commit but will keep changes you have done

특정 파일의 commit 을 취소하려면
