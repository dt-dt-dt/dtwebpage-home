# dtweb.page
dtweb.page is a personal archive of my projects and ideas. This repository is a GitHub mirror of Nekoweb Git for dtweb.page. It pushes to both remotes.

## How to push to both?

> [!note]
> This is mostly for my own personal reference.
> Courtesy of https://stackoverflow.com/a/58394489.

First, Git repo from Nekoweb is cloned onto my machine.
```
git clone https://git.nekoweb.org/XXXX
```

Then, set remotes to both Nekoweb and GitHub. 
```
git remote set-url github git@github.com:username/repo.git
```

Better check if it's there.
```
git remote -v
```

Edit .gitconfig to include "both" repos.
```
cd
nano .gitconfig
```

```
[remote "origin"]
        url = first.git
        url = second.git
        fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
        remote = origin
        merge = refs/heads/master
```

Running `git push` will now push to both.

# Licence

This project is licensed under the MIT Licence. See LICENCE.txt for more.