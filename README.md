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
