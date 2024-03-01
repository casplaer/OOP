# Top-Down Shooter на движке Unity
 **Sapronenko Vyacheslav, gr. 253504**
 
 Проект представляет собой игру жанра шутер с видом сверху наподобие Hotline Miami, Enter the Gungeon, Nuclear Throne, Helldivers и др. В игре будет представлена возможность прохождения в локальном кооперативе, используя локальный мультиплеер. 

 В игре не предусмотрена возможность прохождения, так как подразумевается бесконечное увеличение сложности до смерти игрока. Игра является PVE-ориентированной с случайной генерацией уровней и увеличивающейся сложностью. 
 
Игроки смогут создавать свои уровни делиться ими со всеми игроками, отправляя их в общий список созданных игроками уровней. Созданные людьми уровни можно будет фильтровать по сложности и продолжительности.

Игрокам будут предоставлены несколько персонажей на выбор с различными характеристиками и уникальными способностями.

## Описание классов и их функций

+ Spawner: Класс для генерации основной локации, врагов и игрока. Имеет три метода: spawnEnemies для установки места появления врагов на установленных координатах, spawnPlayer для создания персонажа игрока в стартовой комнате и spawnLocation для создания основной локации для последующей генерации в ней комнат.
+	Enemy: Класс, представляющий собой вражескую сущность, имеющую четыре основных свойства: тип врага, здоровье, скорость передвижения и его оружие.
+	Player: Класс, реализующий основной функционал игрока. Имеет следующий свойства: Никнейм для записи авторства уровня и для внутриигровых надписей, здоровье игрока, его выносливость, скорость передвижения, особая способность (класс Ability) и текущее оружие. Имеет два метода levelUp для улучшения характеристик персонажа и interact, позволяющий взаимодействовать с окружением и подбирать оружие.
+	Ability: Класс, реализующий систему способностей для каждого персонажа, имеет в себе название способности (свойство Name), описание работы способности (свойство Description) и метод вызывающий способность useAbility.
+	Weapon: Класс для оружия. Имеет свойство AttackSpeed, задающее скорость атаки конкретного оружия, свойство Damage, определяющее урон этого оружия.
+	Location: Использует список заготовленных комнат (RoomPrefabs), стартовой комнаты (StartingRoom) и уже существующих на уровне комнат (SpawnedRooms), а также свойство Difficulty для определения сложности данного уровня. Имеет метод spawnRooms, отвечающий за расположение комнат на этом уровне.
+	Room: Пока имеет одно свойство Doors. Определяет направление и количество выходов из каждой комнаты.

![image](https://github.com/casplaer/OOP/assets/73721625/6cdcbe02-f550-4653-b24d-6cbb5e7a4846)
