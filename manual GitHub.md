<h1>Concept of GitHub</h1>
<h2>1. Repository</h2>

_git_ is saved at folder <small>(`git init` folder)</small><br>
this _git_ folder is called **Repository**

<h2>2. Online Repository</h2>

Store _local git repository_ in _Other Server_<br>
this called **Online Repository**

**GitHub** is most popular Online Repository
<br><br>

<h1>Use GitHub</h1>
<h2>0. Main Branch Name</h2>
**GitHub's basic branch name is must be _main_**

```
git branch -M main
```

change basic branch name to **main**
<br><br>

<h2>1. Back up local repository to GitHub</h2>

```
git push 원격저장소주소 업로드할브랜치명
git push -u 원격저장소주소 업로드할브랜치명
git push -u https://github.com/ga111o/주소 main
```

Upload **Local Repository's Main Branch** at GitHub's Repository

(`-u`: remind address.<br>After type `-u` command, `git push` will work as `git push 원격저장소주소 업로드할브랜치명`)
<br><br>

<h2>1-1. put 원격저장소주소 in Variable</h2>

```
git remote add 변수명 원격저장소주소
git remote add origin 원격저장소주소
```

`git push -u 원격저장소주소 업로드할브랜치명`<br>
at this code, _원격저장소주소_ is too long.<br>
for this reason, put _원격저장소주소_ in _Variable_

normaly, Variable name is called _origin_
