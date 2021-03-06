# Git-alias CheatSheet

* g=git
* ga='git add'
    * gaa='git add --all'
    * gapa='git add --patch'
    * gau='git add --update'
    * gav='git add --verbose'
* gap='git apply'
* gb='git branch'
    * gbD='git branch -D'
    * gba='git branch -a'
    * gbd='git branch -d'
    * gbda='git branch --no-color --merged | command grep -vE "^(\*|\s*(master|develop|dev)\s*$)" | command xargs -n 1 git branch -d'
    * gbnm='git branch --no-merged'
    * gbr='git branch --remote'
* gbl='git blame -b -w'
* gbs='git bisect'
    * gbsb='git bisect bad'
    * gbsg='git bisect good'
    * gbsr='git bisect reset'
    * gbss='git bisect start'
* gc='git commit -v'
    * 'gc!'='git commit -v --amend'
    * gca='git commit -v -a'
    * 'gca!'='git commit -v -a --amend'
    * gcam='git commit -a -m'
    * 'gcan!'='git commit -v -a --no-edit --amend'
    * 'gcans!'='git commit -v -a -s --no-edit --amend'
    * gcmsg='git commit -m'
    * 'gcn!'='git commit -v --no-edit --amend'
    * gcs='git commit -S'
    * gcsm='git commit -s -m'
* gco='git checkout'
    * gcb='git checkout -b'
    * gcd='git checkout develop'
    * gcm='git checkout master'
* gcf='git config --list'
* gcl='git clone --recurse-submodules'
* gclean='git clean -fd'
* gcount='git shortlog -sn'
* gcp='git cherry-pick'
    * gcpa='git cherry-pick --abort'
    * gcpc='git cherry-pick --continue'
* gd='git diff'
    * gdca='git diff --cached'
    * gdct='git describe --tags `git rev-list --tags --max-count=1`'
    * gdcw='git diff --cached --word-diff'
    * gds='git diff --staged'
    * gdt='git diff-tree --no-commit-id --name-only -r'
    * gdw='git diff --word-diff'
* gf='git fetch'
    * gfa='git fetch --all --prune'
    * gfo='git fetch origin'
* gg='git gui citool'
    * gga='git gui citool --amend'
* ggpush='git push origin $(git_current_branch)'
* ggsup='git branch --set-upstream-to=origin/$(git_current_branch)'
* ghh='git help'
* gignore='git update-index --assume-unchanged'
* gignored='git ls-files -v | grep "^[[:lower:]]"'
* git-svn-dcommit-push='git svn dcommit && git push github master:svntrunk'
* gk='\gitk --all --branches'
* gke='\gitk --all $(git log -g --pretty=%h)'
* gl='git pull'
    * glum='git pull upstream master'
    * gup='git pull --rebase'
    * gupa='git pull --rebase --autostash'
    * gupav='git pull --rebase --autostash -v'
    * gupv='git pull --rebase -v'
    * ggpull='git pull origin $(git_current_branch)'
* glg='git log --stat'
    * glgg='git log --graph'
    * glgga='git log --graph --decorate --all'
    * glgm='git log --graph --max-count=10'
    * glgp='git log --stat -p'
    * glo='git log --oneline --decorate'
    * glod='git log --graph --pretty='\''%Cred%h%Creset -%C(auto)%d%Creset %s %Cgreen(%ad) %C(bold blue)<%an>%Creset'\'
    * glods='git log --graph --pretty='\''%Cred%h%Creset -%C(auto)%d%Creset %s %Cgreen(%ad) %C(bold blue)<%an>%Creset'\'' --date=short'
    * glog='git log --oneline --decorate --graph'
    * gloga='git log --oneline --decorate --graph --all'
    * glol='git log --graph --pretty='\''%Cred%h%Creset -%C(auto)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'\'
    * glola='git log --graph --pretty='\''%Cred%h%Creset -%C(auto)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'\'' --all'
    * glols='git log --graph --pretty='\''%Cred%h%Creset -%C(auto)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'\'' --stat'
    * glp=_git_log_prettily
* gm='git merge'
    * gma='git merge --abort'
    * gmom='git merge origin/master'
    * gmt='git mergetool --no-prompt'
    * gmtvim='git mergetool --no-prompt --tool=vimdiff'
    * gmum='git merge upstream/master'
* gp='git push'
    * gpd='git push --dry-run'
    * gpf='git push --force-with-lease'
    * 'gpf!'='git push --force'
    * gpoat='git push origin --all && git push origin --tags'
    * gpsup='git push --set-upstream origin $(git_current_branch)'
    * gpu='git push upstream'
    * gpv='git push -v'
* gr='git remote'
    * gra='git remote add'
    * grmv='git remote rename'
    * grrm='git remote remove'
    * grset='git remote set-url'
    * grup='git remote update'
    * grv='git remote -v'
* grb='git rebase'
    * grba='git rebase --abort'
    * grbc='git rebase --continue'
    * grbd='git rebase develop'
    * grbi='git rebase -i'
    * grbm='git rebase master'
    * grbs='git rebase --skip'
* grh='git reset'
    * grhh='git reset --hard'
    * gru='git reset --'
    * gpristine='git reset --hard && git clean -dfx'
* grm='git rm'
    * grmc='git rm --cached'
* gsh='git show'
    * gsps='git show --pretty=short --show-signature'
* gst='git status'
    * gsb='git status -sb'
    * gss='git status -s'
    * gsta='git stash save'
    * gstaa='git stash apply'
    * gstall='git stash --all'
    * gstc='git stash clear'
    * gstd='git stash drop'
    * gstl='git stash list'
    * gstp='git stash pop'
    * gsts='git stash show --text'
* gts='git tag -s'
    * gtv='git tag | sort -V'
* grt='cd $(git rev-parse --show-toplevel || echo ".")'
* gsd='git svn dcommit'
* gsi='git submodule init'
* gsu='git submodule update'
* gsr='git svn rebase'
* gunignore='git update-index --no-assume-unchanged'
* gunwip='git log -n 1 | grep -q -c "\-\-wip\-\-" && git reset HEAD~1'
* gwch='git whatchanged -p --abbrev-commit --pretty=medium'
* gwip='git add -A; git rm $(git ls-files --deleted) 2> /dev/null; git commit --no-verify -m "--wip-- [skip ci]"'
