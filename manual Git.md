<h1>Basic</h1>
<h2>1. Initialization</h2>

```
git init
```

git start to view this directory
<br><br>

<h2>2. Add File</h2>

```
git add 파일명
git add 파일명1 파일명2
git add .
```

save the file's current state<br>
(e.g. `git add './how to use Git.md'`)
<br><br>

<h2>3. File Commit (with memo)</h2>

```
git commit -m '메모 내용'
```

File commit to your repository and memo about file<br>
if inquiry the history, memo will help<br>
(e.g. `git commit -m 'this is git manual`)<br><br>

**When you save the file**<br>
'2. Add File' and '3. File Commit' are fulfil together!

<br><br>

<h1>Restore</h1>
<h2>1. Restore Code</h2>

```
git restore 파일명
git restore --source 커밋아이디
```

restore recent commit version and restore specific commit version
<br><br>

<h2>2. Cancle Staging</h2>

```
git restore --staged
```

Cancle 'git add'(staging)

<h2>3. Delete Commit</h2>

```
git revert HEAD // Delete recent commit
git revert 커밋아이디
git revert 커밋아이디1 커밋아이디2
```

'commit delete' commit
<br><br>

<h2>4. Completely Restore Commit</h2>

```
git reset --hard 커밋아이디
```

restart from that Commit ID

<br><br><br>

<h1>Branch</h1>
<h2>1. Make branch</h2>

```
git branch 브랜치명
```

make to most recent commit's copy
<br><br>

<h2>Switch branch</h2>

```
git switch 브랜치명
git switch main
```

move to recent commit's copy file<br>
type terminal `git status`, you can recognize what branch you choose
<br><br>
![BranchImg](imgOfBranch.png)
this status, your work is always saving at branch
<br><br>

<h2>Combine branch</h2>

<h3>Merge</h3>

```
git merge (기준 브랜치에)합치고 싶은 브랜치 이름
```

**first thing first** need to move the standard branch

**case 1 `3 way merge`** at the each branch<small>(기준 브랜치 and 합치고 싶은 브랜치)</small> are create new commit

**case 2** 기준 브랜치 and 합치고 싶은 브랜치 overlap same file & same line, you need to choose which code you want to select

**case 3 `fast forward merge`** at main branch don't have new commit and new branch have new commit, this case new branch is changed to main branch
<br><br>

<h3>Rebase and merge</h3>

```
//need to run in order
git rebase 중심브랜치명
git merge 새로운브랜치명
```

**first thing first** if want to use `rebase`, need to switch sub branch <small>(instead of main branch)</small>

at the each branch are created new commit, if want to _fast forward merge_ instead of _3 way merge_<br>
last main branch + new branch's start commit<br>
(if branchs are too many, Using rebase instead of merge, branch is more clearly)

<br>
<h3>Squash and merge</h3>

```
git merge --squash 새로운브랜치명
```

main branch's new commit is sum of new branch's all commit

<br><br>

<h2>Delete branch</h2>

```
git branch -d 브랜치명 // after merge
git branch -D 브랜치명 // no merge (like created by mistake)
```

after the merge is done, normaly, delete branch

<br><br><hr/><br><br>

<h1>Additional Command</h1>
<h2>Status</h2>

```
git status
```

<br>
<h2>Check about Commit breakdown</h2>

```
git log --all --oneline
git log --all --oneline --graph
```

<br>
<h2>Check different of commit file and current file</h2>

```
git difftool
```

Compare _commit file_ and _current file_ using Vim<br>
`:qa`: quit Vim editor
<br><br>

```
git difftool 커밋아이디
```

Compare _specific commit file_ and _current file_<br><br>

```
git difftool 커밋아이디1 커밋아이디2
```

Compare _specific commit file1_ and _specific commit file2_<br><br>

<h3>Open file to VSCode instead of Vim</h3>

```
git config --global diff.tool vscode git config --global difftool.vscode.cmd 'code --wait --diff $LOCAL $REMOTE'
```

<br><br>

<h2>Convenient VSCode Extension</h2>

`gitlens` Check Git breakdown(who, when, why change this code)<br>
`git history`<br>
`git graph` upgrade version of 'git diff', _Source Control_(at left nav bar), at the top of nav bar _View Git Graph_ <br>

```

```
