## git revert

[Содержание](/readme.md)


Можно сказать, что команда `git revert` представляет собой типичную команду отмены. Однако вместо удаления коммита из истории проекта эта команда отменяет внесенные в нем изменения и добавляет новый коммит с полученным содержимым. В результате история в *Git* не теряется, что важно для обеспечения целостной истории версий и надежной совместной работы.

Отмена с помощью команды `revert` необходима, когда нужно обратить изменения, внесенные в некоем коммите из истории проекта. Это может быть полезно, если баг появился в проекте из-за конкретного коммита. 

Распространенные опции включают следующие:

```bash=
    -e
    --edit
```
Это параметр по умолчанию, указывать его необязательно. Он открывает настроенный системный редактор, в котором вам будет предложено изменить комментарий к коммиту перед выполнением отмены.

```bash=
    --no-edit
```
Действие этого параметра обратно действию `-e`. Редактор во время выполнения отмены не откроется.

```bash=
    -n
    --no-commit
```

При передаче этого параметра команда `git revert` не будет создавать новый коммит, обратный целевому по своему содержанию. Вместо этого обращенные изменения будут добавлены в раздел проиндексированных файлов и рабочий каталог. Это другие деревья, с помощью которых *Git* управляет состоянием репозитория.

Например, можно откатить конкретные коммиты, перечисляя их хэши через пробел (хэши можно получить в истории изменений):

```bash=
    git revert a867b4af 25eee4ca 0766c053
```





[Содержание](/readme.md)