```
tmux new -s cursor
srun --pty --account=cml --partition=cml-cpu --gres=gpu:0 --cpus-per-task 4 --mem=16G --qos=cml-cpu --time=5:00:00:00 bash
hostname
CTRL+b d
tmux -a -t cursor
tmux kill-session -t cursor
```

Don't forget to update `~/.ssh/config` to include the `slurmnode` as per the new hostname.
