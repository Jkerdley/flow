# flow

Git Flow

1. Создаем реп на хабе + копировать на компьютер (git clone) + cd name
2. git branch dev - создать ветку разработки dev
3. git checkout develop - переключиться в dev
4. git push origin dev - передать в гитхаб ветку dev
   Нужно делить фичи на разные ветки, затем пушить их в dev ветку.
5. git branch feature/main-page - создать ветку
6. git checkout feature/main-page - переключиться в ветку. Затем внести изменения в проект.
7. git add . - выгрузить изменения всех файлов в stage
8. git commit -m '' - коммит
9. git push origin feature/main-page - передать ветку на гитхаб
10. git checkout dev - перейти в ветку dev чтобы от нее создать новую ветку.
11. git checkout -b feature/about-page - создает новую ветку и сразу переходит в нее
12. создаем изменения и пушим на гитхаб.
13. Чтобы сделать merge с dev нужно перейти в dev и написать git merge feature/main-page (переходим в целевую ветку и пишем какую
    ветку подсоединить).
14. git push origin dev - передать изменения в гитхаб из ветки dev (которая уже получила изменения от ветки feature/main-page)
15. На гитхабе создаем pull request и делаем merge с веткой feature/about-page
16. В ветке dev делаем git pull origin dev - получаем итоговую ветку dev (из гитхаба) в локальную ветку dev
    Создание ветки release/0.1.2 (версия) - создается от dev когда время подходит к релизу. В ветке релиза не допускаются новые фичи
    (только фиксы багов). Ветка релиз (когда готова) мерджится в main и develop, и удаляется
17. git checkout -b release/0.1.2 - создаем и переключаемся на ветку релиза. Пушим изменения на гитхаб.
18. git checkout main
19. git merge release/0.1.2
20. git checkout dev
21. git merge release/0.1.2
22. git branch -d release/0.1.2 - удаляем ветку
23. gut push origin main - пушим главную ветку
