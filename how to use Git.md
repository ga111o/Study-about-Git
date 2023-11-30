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


<h2>Status</h2>

```
git status
```
<br>
<h2>Check about Commit breakdown</h2>

```
git log --all --oneline
```