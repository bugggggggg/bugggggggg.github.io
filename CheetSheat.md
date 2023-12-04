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

### Slurm
```bash
# show idle cpus and free memory
sinfo -o "%n %e %m %a %c %C"
# show resources the job uses
scontrol show job [job_id]
```

### Shell
```bash
tar -czvf name-of-archive.tar.gz /path/to/directory-or-file

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

# wget till success
while true;do
  wget -T 15 -c http://example.com && break
done
```

### HugginceFace

```bash
# ssh config
eval `ssh-agent -s`
ssh-add ~/.ssh/id_ed25519

git lfs track *.parquet

git@hf.co:<username>/<name of model> 
```

### Markdown
[cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)