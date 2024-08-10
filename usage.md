### Usage

Add to your .bashrc or .zshrc or an alias file where it will be sourced into your shell. Then symlink your latest project or laravel install to `~/.valet/Sites/latest`
```
laravel new repro-bug-for-issue-119 --git --branch=main && cd repro-bug-for-issue-119
```

```bash
valet link latest
```

```bash
wip
```
```
  “ Knowing is not enough; we must apply. Being willing is not enough; we must do. ”
  — Leonardo da Vinci
On branch main

nothing to commit, working tree clean
```
You can optionally pass commit message, otherwise the inspiring quote will be used as the commit message.
