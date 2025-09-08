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

# new window
Ctrl+B C

# kill pane
Ctrl+B &
```

### Python

```bash
conda activate /path/to/python-path
conda env list
conda create -n py311 python=3.11
conda remove --name ENVIRONMENT --all
echo 'export PATH=/path/to/anaconda3/bin:$PATH' >> ~/.bashrc

source .venv/bin/activate
deactivate

poetry env use python3.10
```

### Git

```bash
# local
git config user.name "Your Name Here"
git config user.email your@email.example
# global
git config --global user.name "Your Name Here"
git config --global user.email your@email.example

git remote remove origin
# push a existing local repo to remote
git remote add origin git@github.com:<username>/<reponame>.git
git branch -M main
git push -u origin main

# move changes from current branch to another
git stash
git checkout correct-branch
git stash pop

# reset commit
git reset --soft HEAD~1

git lfs version
sudo apt install git-lfs
git lfs install
git lfs fetch
git lfs checkout
huggingface-cli lfs-enable-largefiles .
git lfs track "*.your_extension"

# ssh over http
https://docs.github.com/en/authentication/troubleshooting-ssh/using-ssh-over-the-https-port
```

### Slurm

```bash
# show idle cpus and free memory
sinfo -o "%n %e %m %a %c %C"
# show resources the job uses
scontrol show job [job_id]
# run execution time of a finish job
sacct --format=JobID,JobName,Elapsed,Start,End
sacct -j 119311 --format=JobID,JobName,MaxRSS,Elapsed
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
free -g

# basename of a file
stem=$(basename "${file}" .gz)
$(basename NAME [SUFFIX])
$(basename OPTION NAME)

# wget till success
while true;do
  wget -T 15 -c http://example.com && break
done

ls -lrt | awk '{ total += $5 }; END { print total }'

# support emoji render in linux
# sudo apt install fonts-noto-color-emoji
https://gist.github.com/arafathusayn/3d384adfbbdfe0b6a12868e9046e9a23

# linux version
cat /etc/lsb-release
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

[foldable markdown](https://gist.github.com/pierrejoubert73/902cc94d79424356a8d20be2b382e1ab)
[cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Torch

```bash
python -m torch.utils.collect_env 
```

## Docker

```bash
# bash into a docker container, useful for debugging
docker exec -it $CONTAINER_ID sh

docker logs $CONTAINER_ID

# if permission denied
sudo chmod 666 /var/run/docker.sock

# restart
sudo systemctl restart docker

# https://www.nhr.kit.edu/userdocs/horeka/containers/
# docker image -> image file
enroot import -o mmlm-240914.sqsh dockerd://mmlm-240914:latest

# image file -> docker image
# unsquashfs mmlm-240914.sqsh
# tar -czvf mmlm-240914.tar.gz squashfs-root/
# cat mmlm-240914.tar.gz | docker import - mmlm-240914:latest
```
