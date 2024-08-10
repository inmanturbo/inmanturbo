### Inspiring `wip` commit message for artisans

```bash
wip () {
        if [ -f ~/.valet/Sites/latest/artisan ]
        then
                INSPIRE_MESSAGE="$(php ~/.valet/Sites/latest/artisan inspire)" 
        else
                INSPIRE_MESSAGE="wip" 
        fi

        echo "${INSPIRE_MESSAGE}"

        MESSAGE="${1:-$INSPIRE_MESSAGE}"

        git add .
        git commit -m "${MESSAGE}"
}
```

### Usage

Add to your .bashrc or .zshrc or an alias file where it will be sourced into your shell. Then symlink your latest project or laravel install to `~/.valet/Sites/latest`

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
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```
You can optionally pass commit message, otherwise the inspiring quote will be used as the commit message.
