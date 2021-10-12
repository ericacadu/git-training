# Git Training

Practice git skills according to the tasks.


## Git Flow
1. `git branch develop`
2. `git checkout develop`
3. `git branch feature/view`
4. `git checkout feature/view`
5. Do something
6. `git checkout develop`
7. `git merge feature/view`
8. `git checkout master`
9. `git merge develop`

---

## Git

### Basic Task
1. mkdir { date }
2. touch main.html
3. `git add .`
4. `git commit -m 'content'`
5. `git log` # List commit logs

### Cancel Index
1. touch reset.html
2. `git add feature.html`
3. `git reset HEAD` / `git reset HEAD feature.html`
<br>\# Rest index record before commit

### Reset Commit
1. edit main.html to add some text
2. `git checkout main.html` # Rest main.html to latest commit
3. `git add .`
4. `git reset --hard` # Rest all record to latest commit
5. `git reset --hard HEAD^` # Delete latest commit
6. `git reset --hard ORIG_HEAD` # Recover deleted latest commit
7. `git reset --soft HEAD^` # Delete latest commit but keep the content

### Stash
1. `git stash` # Temporarily save records
2. `git stash list`
3. `git stash pop` # Recall the saved record
4. `git stash list`
5. `git stash drop` # Delete latest stash
6. `git stash clear`

### Branch
1. `git branch feature`
2. `git checkout feature` # Edit somthing and commit
3. `git checkout master` # Edit somthing and commit
4. `git merge feature` # Resolve conflict then commit
5. `git branch -D feature` # Delete branch

### Rebase
1. `git commit --amend`
<br>\# Add content to latest commit
<br>\# If there is no index, enter the commit edit mode
2. `git rebase -i xxxx` # Compile commit use squash

* [Difference between git merge and git rebase](https://hackmd.io/@lalarabbits/Hk2egItt_)

---

### Install iTerm2 and Oh my zsh to make you interface more beautiful.
1. Download iTerm2 from [iTerm2 Official Website](https://iterm2.com/)
2. Install oh my zsh
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
echo $SHELL # Check if the default shell is changed to zsh
```

3. Change interface
* You can find the theme from [here](https://github.com/ohmyzsh/ohmyzsh/wiki/themes)
```
vim ~/.zshrc 
# input i to edit
# find ZSH_THEME=robbyrussell to blank ZSH_THEME=""
# you can use theme { sorin } to ZSH_THEME="sorin" or others
# press ESC key to end editing
# type :wq to leave
```