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
echo 'export PATH=/path/to/anaconda3/bin:$PATH' >> ~/.bashrc
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
# linter
autopep8 --in-place --aggressive --aggressive <filename>

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

### Markdown
[cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)