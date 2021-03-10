# Svelte-new-componet-script
Script for making svelte component
```
#!/usr/bin/env bash
if [[ -z "$1" ]]
then
echo "Не задано имя компонента"
exit 1
else
name=$1
touch "${name}".svelte
touch "${name}".coffee
touch "${name}".styl
# shellcheck disable=SC2129
echo "<script src=\"$name.js\"></script>" >> "${name}".svelte
echo "<style src=\"$name.css\"></style>" >> "${name}".svelte
echo "<template lang=\"pug\">" >> "${name}".svelte
echo "    " >> "${name}".svelte
echo "</template>" >> "${name}".svelte
echo "Компонент $name создан"
fi
exit 0
```
