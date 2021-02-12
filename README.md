# 101.git

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

* 첨언: `-hard` 옵션은 모든 것을 취소시켜버리므로 주의해야 함

* 첨언: `-mixed` 가 기본 옵션/설정 임

```
git reset --soft
```
HEAD^ will remove last local (unpushed) commit but will keep changes you have done

특정 파일의 commit 을 취소하려면
