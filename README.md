# Описание проекта
Это проект для изучения Git

## Отрабатываю команды add / restore
1. `$ git add .` - добавляет в индекс
2. `$ git restore --staged .` - убирает из индекса

## Проверка commit
### 1. Просмотр конкретного commit по hash 
`$ git show <hash>`

### 2. Просмотр список файлов, измененных в commit
`$ git diff-tree --no-commit-id --name-only -r <хеш>`

### 3. Просмотреть историю изменений
`$ git log --online --stat`

### 4. Сравнение commit
`$ git diff <хеш>^ <хеш>`
`$ git diff HEAD^ HEAD` - показывает изменения между предыдущим и текущим коммитом

### 5. Отмена commit (до `$ git push`)
`$ git reset --soft HEAD~1` - commit удаляется из истории, изменения поступают в индекс
`$ git reset HEAD~1` - commit удаляется и изменения остаются в рабочей диреткории, а не в индексе
`git reset --hard HEAD~1` - commit удаляется, а так же удаляются все изменения!!!

