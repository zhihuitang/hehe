1. Add a global “squash” alias from bash
```bash
git config --global alias.squash '!f(){ git reset --soft HEAD~${1} && git commit --edit -m"$(git log --format=%B --reverse HEAD..HEAD@{1})"; };f'
```
2. /.gitconfig should now contain this alias:
```bash
[alias]
    squash = "!f(){ git reset --soft HEAD~${1} && git commit --edit -m\"$(git log --format=%B --reverse HEAD..HEAD@{1})\"; };f"
```
3. How to use it?
```>git squash 2    