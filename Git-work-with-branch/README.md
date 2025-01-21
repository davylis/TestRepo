# How to use branches with remote repo

### clone repo
```
git clone https://github.com/user/test.git
```

### Make branch and switch to it
```
git switch -c develop
git push -u origin develop
```

### Make your own feature branch and switch to it
```
git switch -c feature/liisa
```

### Save edits
```
git add scrum-guide.md
git commit -m "Lisätty Sprintit-osio"
```

### Send edits to origin
```
git push origin feature/otsikko-tai-muutos
```

### Merge feature branch with develop branch
```
git switch develop
git pull origin develop
git merge --no-ff feature/liisa -m "Merge"
git push origin develop
```

### Publish ready version to main branch
```
git switch main
git pull origin master
git merge --no-ff develop -m "Release version 1.0"
git tag -a v1.0 -m "First release of Scrum guide"
git push origin v1.0
git push origin master
```

