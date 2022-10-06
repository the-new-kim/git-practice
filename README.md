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
