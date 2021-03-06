## git fetch

[Содержание](/readme.md)

Команда `git fetch` загружает коммиты, файлы и ссылки из удаленного репозитория в ваш локальный репозиторий.

```bash=
git fetch <remote>
```

Это команда извлечения всех веток из репозитория. При этом также загружаются все необходимые коммиты и файлы из другого репозитория.

```bash=
git fetch <remote> <branch>
```

Аналогично команде выше, но данные извлекаются только для указанной ветки.

```bash=
git fetch --all
```

Мощная команда, которая извлекает все зарегистрированные удаленные репозитории и их ветки.

```bash=
git fetch --dry-run
```

Опция `--dry-run` выполняет демонстрационный прогон команды. Она выводит на экран действия, которые были бы выполнены при извлечении, не выполняя их на самом деле.

[Содержание](/readme.md)