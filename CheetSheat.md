---
title:  "Cheat Sheet"
layout: post
---


### Tmux
```bash
(sudo) apt install tmux # for Ubuntu
tmux new -s mysession
tmux attach -t mysession
tmux detach
tmux ls
tmux kill-session -t mysession
tmux rename-session -t old-session-name new-session-name
```

### Conda
```bash
conda env list
conda create -n py311 python=3.11
conda remove --name ENVIRONMENT --all
```

### Git
```bash
# local
git config user.name "Your Name Here"
git config user.email your@email.example
# global
git config --global user.name "Your Name Here"
git config --global user.email your@email.example
```

### Shell
```bash
# substr
string='My long string'
if [[ $string == *"My long"* ]]; then
  echo "It's there!"
fi

# file exists
if [ -e tmp.txt ]
then
    echo "exist"
else
    echo "not exist"
fi

# memory size
grep MemTotal /proc/meminfo

# basename of a file
stem=$(basename "${file}" .gz)
$(basename NAME [SUFFIX])
$(basename OPTION NAME)
```
