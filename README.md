# Онлайн игра "Points" (Точки) на 2-7 игроков.

##### Геймплей: Захватить как можно больше врагов или образовать как можно больше территорию.

#### Игровые правила:
- Игроки ходят по очереди.

- У каждого есть не более N времени на ход.

- На поле имеется поле наполненное ярко-серыми точками. Это места для создания пункта.

- За ход можно создать 1 пункт.

- Если пункты образуют замкнутую цепь и внутри есть хотя бы 1 вражеский пункт, то эта территория считается захваченной

- На захваченной территории нельзя ставить другие пункты.

- Захваченную территорию можно захватить также как и пункты (просто замкнуть цепь вокруг этой территории)

- По желанию лидера лобби может присутствовать таймер до конца игры для каждого игрока отдельно. То есть какой либо игрок может играть лишь N время (например как в шахматных часах).

Игровой процесс происходит на одном из устройств, а другие игроки к нему подключаются.

#### Будет 2 типа карт:
1. Неограниченная
2. Ограниченная

#### И 2 типа целей:
1. Получить наибольшую площадь своей территории (или достигнуть S значения)
2. Захватить как можно больше вражеских пунктов (или достигнуть E значения)

Перед началом игры лидер лобби может эти правила менять

#### Также для каждого из игроков будет сохраняться его статистика которая будет например включать:
1. Уровень
2. Победы/Поражения
3. Среднее время хода
4. Кол-во игр
5. Максимальная территория
6. Максимальное число захваченных пунктов

#### Задачи

1. Создать презинтацию `branch: demonstration`
2. Реализовать заготовки для всех активностей которые будут в приоритете (Внешний вид сделать примерный)
   1. GameActivity `branch: feature/GameActivity`
   2. MainActivity `branch: feature/MainActivity`
   3. PlayOfflineActivity `branch: feature/PlayOfflineActivity`
   4. SettingsActivity `branch: feature/SettingsActivity`
   5. PlayOnlineActivity `branch: feature/PlayOnlineActivity`
   6. LobbyActivity `branch: feature/LobbyActivity`
   7. AccountActivity `branch: feature/AccountActivity`
3. Создать ScrollMap в GameActivity на GameView `branch: feature/scrollMap`
   1. Возможность перемещать её
   2. Приближать и отдалять
   3. Отрисовка для ограниченной карты
   4. Отрисовка для неограниченной карты
4. Создать сущность Player'а и Team'ы (но Team в минимальном варианте)
5. Игровые объекты
    1. Пункты (Точки)
       1. Отрисовка
       2. Установка по нажатию на необходимое место
    2. Стены
       1. Отрисовка
       2. Автоматическое собирание если рядом союзный пункт
       3. Собирание при условии что они образуют замкнутую цепь заключающие хотя бы 1 врага
    3. Территория
       1. Отрисовка
       2. Автоматическое создание
6. Сделать игровые правила
   1. Сделать смену игроков каждый ход
   2. Таймер хода
   3. Обработка победы и поражения
7. Настройки игры (Доработать SettingsActivity). Добавить возможность применять эти настройки в самой игре
8. Доработать AccountActivity
   1. Добавить возможность изменять никнейм
   2. Добавить возможность изменять аватар
9. Добавить сбор статистики из игры в локальную базу данных
10. Доработать AccountActivity
    1. Отображать статистику за всё время используя локальную базу данных
11. Сетевая игра
     1. Поиск и создание лобби
     2. Доработать LobbyActivity
     3. Добавить в GameView режим работы для Online в качестве хоста и клиента