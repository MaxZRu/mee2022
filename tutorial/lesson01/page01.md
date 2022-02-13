# Восстановление забора

## {Introduction @showdialog}

Учимся строить линию из блоков

Задача: Построить 4 блока забора


## {Step 2}

Обеспечим нашего агента материалами, нам нужно 4 блока забора
---
Создам блок обеспечения материалов ``||agent.агент ставит блок или предмет (деревянный забор) в количестве (4) штуки в ячейку инвентаря (1) ||``

```blocks
player.onChat("run", function () {
    agent.setItem(OAK_FENCE, 4, 1)
})
```
## {Step 3}

Чтобы удобно было строить разместим нашего агента рядом с забором.
---
Добавим блок движения агента ``||agent.агент: переместиться (влево) на (1) блок ||``

```blocks
player.onChat("run", function () {
    agent.setItem(OAK_FENCE, 4, 1)
    agent.move(LEFT, 1)
})
```

## {Step 3}

Нужно построить 4 блока забора - создадим цикл
---
Добавим блок цикла  ``||loops.Повторить (4) раза делать||``

```blocks
player.onChat("run", function () {
    agent.setItem(OAK_FENCE, 4, 1)
    agent.move(LEFT, 1)
    for (let index = 0; index < 4; index++) {
    }
})
```

## {Step 4}

Разметим блок справа от Агента
---
Добавим блок размещения  ``||agent.Разметить (вправо)||``

```blocks
player.onChat("run", function () {
    agent.setItem(OAK_FENCE, 4, 1)
    agent.move(LEFT, 1)
    for (let index = 0; index < 4; index++) {
        agent.place(RIGHT)    
    }
})
```

## {Step 5}

Двигаемся вперед
---
Добавим блок движения агента  ``||agent.переместиться (вперед) на (1) блок||``

```blocks
player.onChat("run", function () {
    agent.setItem(OAK_FENCE, 4, 1)
    agent.move(LEFT, 1)
    for (let index = 0; index < 4; index++) {
        agent.place(RIGHT)    
        agent.move(FORWARD, 1)
    }
})
```

## {Congrats}

Програму мы закончили нужное её запустить и в консоли выполнить команту **run**

## {Finale}

Тестируйте нажмите ">" и в консоли **run**


```blocks
player.onChat("run", function () {
    agent.setItem(OAK_FENCE, 4, 1)
    agent.move(LEFT, 1)
    for (let index = 0; index < 4; index++) {
        agent.place(RIGHT)
        agent.move(FORWARD, 1)
    }
})

```


