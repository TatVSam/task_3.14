## git push

[Содержание](/readme.md)

Команда `git push` используется для выгрузки содержимого локального репозитория в удаленный репозиторий. Она позволяет передать коммиты из локального репозитория в удаленный. Эта команда симметрична команде [git fetch](fetch.md): при извлечении с помощью *fetch* коммиты импортируются в локальные ветки, а при публикации с помощью push коммиты экспортируются в удаленные ветки. Настроить удаленные ветки можно с помощью команды [git remote](./remote.md). Команда *push* может перезаписать изменения, поэтому при ее использовании следует соблюдать осторожность. 

```bash=
    git push <remote> <branch>
```
Публикация указанной ветки в удаленном репозитории вместе со всеми необходимыми коммитами и внутренними объектами. Эта команда создает локальную ветку в репозитории назначения. Чтобы предотвратить перезапись коммитов, *Git* не позволит опубликовать данные, если в репозитории назначения нельзя выполнить ускоренное слияние.

```bash=
    git push <remote> --force
```

Аналогично приведенной выше команде, однако данные будут опубликованы принудительно, даже если нельзя выполнить ускоренное слияние. Не используйте флаг `--force`, если вы не уверены в своих действиях.

```bash=
    git push <remote> --all
```
Публикация всех локальных веток в указанном удаленном репозитории.

```bash=
    git push <remote> --tags
```
При публикации ветки или использовании опции `--all` теги не публикуются автоматически. Флаг `--tags` отправляет все локальные теги в удаленный репозиторий.

[Содержание](/readme.md)