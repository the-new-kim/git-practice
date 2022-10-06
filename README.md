# Git practice

## Setting

### username & email

```
$ git config --global user.name "Kim"
$ git config --global user.email "email@email.com"
```

- confirm

```
$ git config --global user.name
> Kim
```

### default branch name

```
$ git config --global init.defaultBranch main
```

- list config settings

```
$ git config --list
> init.defaultBranch=main
> user.name=Kim
> user.email=email@email.com
```

## Repository

- inspecting

```
$ git status
```

- Saving changes

```
$ git add README.md
$ git add .
```

# Git practice

## Setting

### username & email

```
$ git config --global user.name "Kim"
$ git config --global user.email "email@email.com"
```

- confirm

```
$ git config --global user.name
> Kim
```

### default branch name

```
$ git config --global init.defaultBranch main
```

- list config settings

```
$ git config --list
> init.defaultBranch=main
> user.name=Kim
> user.email=email@email.com
```

## Repository

- inspecting

```
$ git status
```

- Saving changes & Commit

```
$ git add README.md
$ git commit
```

### VI mode

- `esc` : Switch to Command mode.
- `i` : Switch to Insert mode.
- `:q` + `enter` : Quit without saving
- `:q!` + `enter` : Quit force without saving
- `:wq` + `enter` : Save and Quit

ex) `git commit` -> `i` -> `first commit` -> `esc` -> `:wq` + `enter`

```
$ git log
```

```
$ git diff
```

- `k` : up
- `j` : down
- `:q`/`q` : quit

```
$ git add .
$ git commit -m "add text"
```

- shortcut without untracked file

```
$ git am -add new line to text"
```

## Reset & Revert

```
$ git reset --hard HASH
$ git revert HASH
```
