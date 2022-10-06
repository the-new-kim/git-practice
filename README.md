# Git practice

---

## 1. Setting

#### username & email

```
$ git config --global user.name "Kim"
$ git config --global user.email "email@email.com"
```

confirm

```
$ git config --global user.name
> Kim
```

#### default branch name

```
$ git config --global init.defaultBranch main
```

List config settings

```
$ git config --list
> init.defaultBranch=main
> user.name=Kim
> user.email=email@email.com
```

---

## 2. Repository

Inspecting

```
$ git status
```

Saving changes & Commit

```
$ git add README.md
$ git commit
```

#### VI mode

- `esc` : Switch to Command mode.
- `i` : Switch to Insert mode.
- `:q` + `enter` : Quit without saving
- `:q!` + `enter` : Quit force without saving
- `:wq` + `enter` : Save and Quit

ex) `git commit` -> `i` -> `first commit` -> `esc` -> `:wq` + `enter`

`$ git log` : Shows the commit logs 그동안 커밋한 내용을 보여줌

`$ git diff` : Show changes between commits, commit and working tree, etc

- `k` : up
- `j` : down
- `:q`/`q` : quit

```
$ git add .
$ git commit -m "Add text"
```

shortcut without untracked file

```
$ git am -add new line to text"
```

#### [How to Write a Git Commit Message](https://cbea.ms/git-commit/)

##### 1. 대문자로 시작할것 :

- `Fix typo in text`👍
- `fix typo in text`🚫

##### 2. 마지막에 점을 붙이지 말것 :

- `Replace curry from pizza`👍
- `Replace curry from pizza.`🚫

##### 3. 명령형으로 쓸것 :

- `Add new line to pizza`👍
- `Added new line to pizza`🚫
- `Adding new line pizza`🚫

---

## 3. Reset & Revert

```
$ git reset --hard HASH
$ git revert HASH
```

📝 만약에 revert로 파일이 생성된 시점으로 돌아가게 되면  
파일을 삭제할건지 추가할건지 물어본다. 이때 둘중 하나를 선택  
`$ git add <file name>` / `$ git rm <file name>`  
그리고 컨티뉴 해주면 됨
`$ git revert --continue`  
아니면 중단
`$ git revert --abort`

파일의 내용이 바뀐 경우, 예를 들어 txt파일에 새로운 라인 생성/삭제가 아닌,  
같은 라인에서 변화가 생겼을 경우, current/incoming/both change 를 accept 할 건지 물어봄.

## 4. Branch

List

```
$ git branch
```

Create 👉 [Branching Naming Convention](https://codingsight.com/git-branching-naming-convention-best-practices/)

```
$ git branch <branch-name>
```

Switch (checkout으로부터 분리되어 옴. checkout -> switch, restore)

```
$ git switch <branch-name>
```

Create & Switch

```
$ git switch -c <branch-name>
```

Delete

```
$ git branch -d <branch-name>
```

Rename

```
$ git branch -m <old-name> <new-name>
```

Merge

```
$ git merge <branch-name>
```

reset 으로 merge 이전으로 돌아갈수 있음!
merge 된 branch 는 삭제

Rebase

```
$ git rebase <branch-name>
```

Pull (no rebase will just merge)

```
$ git pull --no-rebase
```

```
$ git pull --rebase
```
