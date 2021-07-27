# Useful git scripts

- **Delete all local merged branches**
  ```bash
  git branch --merged | egrep -v "(^\*|master|main|dev)" | xargs git branch -d
  ```
- **Show differences between remote & local branch**
  ```bash
  git diff origin/master .
  ```
