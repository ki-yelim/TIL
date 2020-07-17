# Git

> Git은 분산버전관리시스템(DVCS)이다. Distributed version Control System
>
> 소스코드의 버전 및 이력을 관리할 수 있다.

## 준비하기

윈도우에서 git을 활용하기 위해서  git bash를 설치한다. 

git을 활용하기 위해서 GUI 툴인 `source tree`, `github desktop` 등을 활용할 수도 있다. 

초기 설치를 완료한 이후에 컴퓨터에 autor 정보를 입력한다. 

``` bash
$ git config --global user.name {user name}
$ git config --global user.email {user email}
```



## 로컬 저장소(Repository) 활용하기

### 1. 저장소 초기화

```bash
$ git init
Initialized empty Git repository in C:/Users/kimsj/temp/.git/
```

- `.git` 폴더가 생성되며, 여기에 git과 관련된 모든 정보가 저장된다. 

- git bash 에 `(master)` 라고 표시되는데, 이는 현재 폴더가 git으로 관리되고 있다는 뜻이며, `master` `branch`에 있다는 뜻이다. 

### 2. `add` 

`working directory`, 즉 작업공간에서 변경된 사항을 이력으로 저장하기 위해서는 반드시`staging area`를 거쳐야한다. 

```bash
$ git add {파일 또는 폴더}
$ git add markdown.md 	# 파일 
$ git add images/ 		# 폴더
$ git add . 			# 현재 디렉토리에 있는 모든 파일과 폴더
```

- markdown.md 파일이 폴더에 새롭게 작성되었으나, 아직 git 으로 관리되지 않고, add 전 상태

``` bash
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        markdown.md
        
nothing added to commit but untracked files present (use "git add"bas
```

- markdown.md 파일이 add 후에 staging area로 올라간 상태

```bash
$ git status
on branch master

No commits yet

changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   markdown.md
```

  

### 3. `Commit`

Commit은 **이력을 확정짓는 명령어**로, 해당 시점의 스냅샷을 기록한다. 

커밋시에는 반드시 메시지를 작성해야 하며, 메시지는 변경사항을 알 수 있도록 명확하게 작성한다. 

```bash
$ git commit -m "마크다운 정리"
[master (root-commit) 6c84015] 마크다운 정리
 1 file changed, 170 insertions(+)
 create mode 100644 markdown.md
```

커밋 이후에는 아래의 명령어를 통해 지금까지 작성된 커밋 이력을 확인한다. 

```bash
$ git log 
commit 6c840158f44a51f40c02f08d226289d899a6c904 (HEAD -> master)
Author: edujason-hphk <edujason.hphk@gmail.com>
Date:   Fri Jul 17 14:17:22 2020 +0900

    마크다운 정리
    
$ git log --oneline
6c84015 (HEAD -> master) 마크다운 정리		#한줄로 표시해줌
```

커밋은 해시값을 바탕으로 구분된다. 



## 원격 저장소(remote repository) 활용하기

원격저장소 기능을 제공하는 다양한 서비스 중에 github을 기준으로 설명한다. 

### 0. 준비사항

- Github에 repository 생성



### 1. 원격 저장소 등록

```bash
$ git remote add origin {github url}
```

- 원격저장소(remote)로 origine이라는 이름으로 girhub url을 등록(add)한다. 

- 등록된 원격 저장소를 보기 위해서는 아래의 명령어를 활용한다.

- ```bash
  $ git remote -v
  origin  http://github.com/ki-yelim/TIL.git (fetch)
  origin  http://github.com/ki-yelim/TIL.git (push)
  ```

  

### 2. Push - 원격 저장소로 업로드

```bash
$ git bush origine master
```

origine 이라는 이름의 원격저장소로 commit 기들을 없로드 한다. 

이후, 변경사항이 생길 때 마다,` add `- `commit` -` push` 를 반복한다. 



### 3. 추가내용