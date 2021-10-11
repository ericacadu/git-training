# Git Training

Practice git skills according to the tasks.

### Basic Task
1. mkdir { date }
2. touch main.html
3. `git add .`
4. `git commit -m 'record description'`
5. `git log` # search commit record

### Cancel Index
1. touch reset.html
2. `git add reset.html`
3. `git reset HEAD` / `git reset HEAD reset.html`
<br>\# Rest index record before commit

### Rcover File
1. edit main.html to add some text
2. `git checkout main.html` # Rest main.html to latest commit
3. `git add .`
4. `git reset --hard` # Rest all record to latest commit
5. `git reset --hard HEAD^` # Delete latest commit
6. `git reset --hard ORIG_HEAD` # Recover deleted latest commit
7. `git reset --soft HEAD^` # Delete latest commit but keep the content
8. `git commit --amend` # Add content to latest commit

### Branch

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