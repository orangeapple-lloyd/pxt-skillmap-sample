# 加入燃料系統

## 簡介 @unplugged

該補充燃料囉!

在這份教學中,我們會幫你的太空船加上一條燃料計量表,當你飛行時燃料會逐漸減少。

記得要去接補給道具,讓你的太空船不會半路拋錨!

![燃料補給!](/static/skillmaps/space/eat-gas.gif "下的是...塔可雨嗎?")


## 步驟 1
😵 起始的程式碼已經佔了不少空間! 別擔心,Arcade 的工作區會自動延伸。只要往上、往旁邊捲動 (或往下、往旁邊) 就能繼續組裝積木。
<hr/>

🔲 看看新的 ``||statusbars:Status Bars||`` 類別。 你會找到 ``||variables:set [statusbar] to create status bar sprite width [20] height [4] kind [Health]||``。 把它拖到 ``||loops:on start||`` 容器的最後面。

🔲 為了追蹤還剩下多少 *燃料*,把 **statusbar** 的 kind 參數改成 **Energy**。
<hr/>
>> *小提示: ``||statusbars:Status Bars||`` 類別是一個 [__擴充套件__](#extendo "提供 MakeCode 延伸功能的類別")。 想看看還能用哪些擴充套件,從你的圖庫打開一個遊戲, 點選 ``||statusbars:˅ Advanced||`` 然後選擇 ``||extension:Extensions||``*

```block
let statusbar = statusbars.create(20, 4, StatusBarKind.Energy)
```

## 步驟 2
如果我們希望這條計量表顯示 **mySprite** 的狀態,就要把這兩個東西連結起來。
<hr/>

🔲 把 ``||statusbars:attach [statusbar] to [mySprite] ⊕||`` 拖到 ``||loops:on start||`` 容器的最後面。

🔲 點擊新積木上的 **⊕** 來展開選項, 可以調整計量表相對於 **mySprite** 的位置。 你能找到方法把計量表顯示在太空船 *下方* 嗎?

<br/>

```block
let statusbar = statusbars.create(20, 4, StatusBarKind.Energy)
// @highlight
statusbar.attachToSprite(mySprite, -25, 0)
```

## 步驟 3
⏰ 在空中飛得越久,消耗的燃料就越多 ⏰  

接下來教你怎麼讓燃料隨著時間流逝慢慢減少。
<hr/>
🔲 拖一個 ``||game:on game update every [500] ms||`` 容器到工作區。 把時間參數調整成 **300 ms**。

🔲 把 ``||statusbars:change [statusbar] [value] by [0]||`` 積木放進 **game update** 容器裡。

🔲 把計量表變化量從 **0** 改成 **-1**。
<hr/>

>> *小提示: 把這個步驟記在心裡。如果之後玩遊戲時發現燃料消耗得太快, 你可以回來調整這些積木。*


```blocks
let statusbar: StatusBarSprite = null
game.onUpdateInterval(300, function () {
    statusbar.value += -1
})
```

## 步驟 4
⛽ 補充燃料時間 ⛽

你可以掉落汽油桶、能量水晶,或是多汁的漢堡...只要符合你太空船的設定就好。

掉落燃料的程式碼跟掉落敵人的程式碼很像。 如果忘記怎麼做了,在工作區裡找出 **myEnemy** 的積木參考一下。
<hr/>
🔲 拖一個 _新的_ ``||game:on game update every [500] ms||`` 容器 到工作區,把間隔時間改成 **5 秒 (5000 ms)**。

🔲 把 ``||variables:set [projectile2] to||`` ``||sprites:projectile [ ] from side with vx [50] vy [50]||`` 積木接在最新的 **on game update** 容器裡。

🔲 點擊 ``||variables:[projectile2]||`` 把角色名稱改成 ``||variables:[myFuel]||``。

🔲 點擊那個灰色方塊打開角色編輯器, 畫出燃料角色 (或從圖庫挑一個)。

🔲 調整燃料的 **vx** 和 **vy** 參數,直到它能以適當的速度直直往下掉。

<br/>


```blocks
game.onUpdateInterval(5000, function () {
    let myFuel = sprites.createProjectileFromSide(img`
        5 5 5 5 5 5 5 5 5 5 5 5 5 5 5 5
        5 . . . . . . . . . . . . . . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 . . . . 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 . . 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 5 . 5 5 5 5 . 5
        5 . 5 5 5 5 . . . . 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . . . . . . . . . . . . . . 5
        5 5 5 5 5 5 5 5 5 5 5 5 5 5 5 5
        `, 0, 50)
})
```
## 步驟 5

就像敵人一樣,我們希望燃料從畫面上方的隨機位置掉下來。
<hr/>
🔲 把一個 ``||sprites:set [mySprite] [x] to [0]||`` 積木接在 ``||game:on game update every [5000] ms||`` 容器的最下面。

🔲 為了確認我們是在對正確的角色操作,點開新積木上的下拉選單, 把 ``||variables:mySprite||`` 改成 ``||variables:myFuel||``。

🔲 為了讓燃料的 [__*x*__](#setX "水平位置") 是隨機的, 拿一個 ``||Math:pick random [0] to [10]||`` 積木, 把它接到 ``||sprites:set [mySprite] [x] to [0]||`` 積木裡取代 **0** 參數。

🔲 把 ``||Math:pick random [0] to [10]||`` 積木的最小參數改成 **5**, 最大參數改成 **155**。
<hr/>

```blocks
namespace SpriteKind {
    export const Gas = SpriteKind.create()
}

game.onUpdateInterval(5000, function () {
    let myFuel = sprites.createProjectileFromSide(img`
        5 5 5 5 5 5 5 5 5 5 5 5 5 5 5 5
        5 . . . . . . . . . . . . . . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 . . . . 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 . . 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 5 . 5 5 5 5 . 5
        5 . 5 5 5 5 . . . . 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . . . . . . . . . . . . . . 5
        5 5 5 5 5 5 5 5 5 5 5 5 5 5 5 5
        `, 0, 50)
        // @highlight
    myFuel.x = randint(5, 155)   
})
```

## 步驟 6

現在我們要把 **myFuel** 角色歸類到 _gas_ 這個類別。
<hr/>
🔲 把一個 ``||variables:set [mySprite] kind to [Player]||`` 積木 接在最新的 **on game update** 容器最下面。

🔲 把 ``||variables:mySprite||`` 改成 ``||variables:myFuel||``。

🔲 點擊 ``||sprites:Player||`` 打開選單,然後選 ``||sprites:Add a new kind...||`` 並建立 **Gas** 這個類型。
<br/>

```blocks
namespace SpriteKind {
    export const Gas = SpriteKind.create()
}

game.onUpdateInterval(5000, function () {
    let myFuel = sprites.createProjectileFromSide(img`
        5 5 5 5 5 5 5 5 5 5 5 5 5 5 5 5
        5 . . . . . . . . . . . . . . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 . . . . 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 . . 5 5 5 5 . 5
        5 . 5 5 5 5 . 5 5 . 5 5 5 5 . 5
        5 . 5 5 5 5 . . . . 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . 5 5 5 5 5 5 5 5 5 5 5 5 . 5
        5 . . . . . . . . . . . . . . 5
        5 5 5 5 5 5 5 5 5 5 5 5 5 5 5 5
        `, 0, 50)
    myFuel.x = randint(5, 155) 
    // @highlight  
    myFuel.setKind(SpriteKind.Gas)
})
```


## 步驟 7
當你的太空船跟燃料重疊時,我們希望燃料消失,同時油箱也補滿。
<hr/>  

🔲 拖一個 ``||sprites:on [sprite] of kind [Player] overlaps [othersprite] of kind [Player]||`` 容器到工作區。

🔲 把最後一個參數從 ``||sprites:Player||`` 改成 ``||sprites:Gas||``。

🔲 為了在抓到燃料後補滿計量表,抓一個 ``||statusbars:set [statusbar] [value] to [0]||`` 積木 接到最新的 **overlaps** 容器裡。把數值從 **0** 改成 **100**。

🔲 最後,要讓被使用掉的燃料消失,把一個 ``||sprites:destroy [mySprite] ⊕||`` 積木 接到同一個 **overlaps** 容器的最下面,並把 ``||variables:mySprite||`` 改成 ``||variables:otherSprite||``

![從積木抓取變數](/static/skillmaps/space/give-var.gif "原來是這樣做的!")

<br/>


```blocks
namespace SpriteKind {
    export const Gas = SpriteKind.create()
}

let statusbar: StatusBarSprite = null
sprites.onOverlap(SpriteKind.Player, SpriteKind.Gas, function (sprite, otherSprite) {
    statusbar.value = 100
    otherSprite.destroy()
})
```

## 步驟 9
🌌 如果燃料用完了,你就會被困在太空中! 🌌

威脅可是很真實的喔。
<hr/>
🔲 為了讓計量表歸零時有相應的後果,拖一個 ``||statusbars:on status bar kind [Health] zero [status]||`` 容器到工作區。

🔲 把計量表的 kind 改成 **Energy**。

🔲 把一個 ``||game:game over <LOSE>||`` 積木接進去當作最終的結局。

<hr/>
這樣就完成了! 你應該已經有一個完整可運作的遊戲,可以存到你的專案圖庫並分享給朋友!

但是...你不用就此打住。一旦你的遊戲進入圖庫之後,你可以盡情實驗工具箱裡的所有積木,發掘更多刺激又特別的方式來打造屬於你的冒險。
<br/>

```blocks
statusbars.onZero(StatusBarKind.Energy, function (status) {
    game.over(false)
})
```

```template

controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    let projectile = sprites.createProjectileFromSprite(img`
3 3 3 3 3 3 3 3
3 . . . . . . 3
3 . 3 3 3 3 . 3
3 . 3 . . 3 . 3
3 . 3 . . 3 . 3
3 . 3 3 3 3 . 3
3 . . . . . . 3
3 3 3 3 3 3 3 3
    `, mySprite, 0, -70)
    projectile.startEffect(effects.ashes)
})
sprites.onOverlap(SpriteKind.Projectile, SpriteKind.Enemy, function (sprite, otherSprite) {
    sprite.destroy(effects.bubbles, 500)
    otherSprite.destroy(effects.smiles, 500)
})
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    info.changeLifeBy(-1)
    otherSprite.destroy(effects.disintegrate, 500)
})
let myEnemy: Sprite = null
effects.starField.startScreenEffect()
let mySprite = sprites.create(img`
    . . . . . . . 9 9 . . . . . . .
    . . . . . . 9 . . 9 . . . . . .
    . . . . . . 9 . . 9 . . . . . .
    . . . . . 9 . 9 9 . 9 . . . . .
    . . . . . 9 . 9 9 . 9 . . . . .
    . . . . 9 . 9 9 9 9 . 9 . . . .
    . . . . 9 . 9 9 9 9 . 9 . . . .
    . . . 9 . 9 9 9 9 9 9 . 9 . . .
    . . . 9 . 9 . . . . 9 . 9 . . .
    . . 9 . 9 9 . 9 9 . 9 9 . 9 . .
    . . 9 . 9 9 . . . . 9 9 . 9 . .
    . 9 . 9 9 9 . 9 9 9 9 9 9 . 9 .
    . 9 . 9 9 9 . 9 9 9 9 9 9 . 9 .
    9 . 9 9 9 9 9 9 9 9 9 9 9 9 . 9
    9 . . . . . . . . . . . . . . 9
    9 9 9 9 9 9 9 9 9 9 9 9 9 9 9 9
`, SpriteKind.Player)
controller.moveSprite(mySprite)
mySprite.setFlag(SpriteFlag.StayInScreen, true)
game.onUpdateInterval(500, function () {
    myEnemy = sprites.createProjectileFromSide(img`
        2 2 2 2 2 2 2 2 2 2 2 2 2 2 2 2
        2 . . . . . . . . . . . . . . 2
        2 . 2 2 2 2 2 2 2 2 2 2 2 2 . 2
        . 2 . 2 2 2 . . . . 2 2 2 . 2 .
        . 2 . 2 2 2 . 2 2 2 2 2 2 . 2 .
        . . 2 . 2 2 . . . 2 2 2 . 2 . .
        . . 2 . 2 2 . 2 2 2 2 2 . 2 . .
        . . . 2 . 2 . . . . 2 . 2 . . .
        . . . 2 . 2 2 2 2 2 2 . 2 . . .
        . . . . 2 . 2 2 2 2 . 2 . . . .
        . . . . 2 . 2 2 2 2 . 2 . . . .
        . . . . . 2 . 2 2 . 2 . . . . .
        . . . . . 2 . 2 2 . 2 . . . . .
        . . . . . . 2 . . 2 . . . . . .
        . . . . . . 2 . . 2 . . . . . .
        . . . . . . . 2 2 . . . . . . . 
        `, 0, 50)
    myEnemy.x = randint(5, 155)
    myEnemy.setKind(SpriteKind.Enemy)
})

```

```ghost
statusbar.positionDirection(CollisionDirection.Bottom)
```

```package
pxt-status-bar=github:jwunderl/pxt-status-bar
```
