# 加入太空中的相遇

## 簡介 @unplugged

你的宇宙現在還相當空蕩。讓我們加入一些東西,讓你的太空船在旅途中可以遇見!可能是行星、小行星,或是其他太空船留下的太空殘骸,也或許你會遇到其他旅人,甚至外星人的火箭!

## 加入陣列

首先,點擊工具箱中的 **Advanced**。從 ``||arrays:Arrays||`` 中,拖出 ``||variables:set list to||`` 積木,接到 ``||loops:on start||`` 裡面。

```blocks
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
// @highlight
let list = [1, 2, 3]
```

## 畫一些行星

接下來,再次打開 **Advanced**,從 ``||images:Images||`` 中拖出灰色的圖片方框。在陣列的每個位置都放上一個,然後點擊灰色方框畫出你的太空物件。

```blocks
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
scene.cameraFollowSprite(mySprite)
// @highlight
let list = [img`
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3
    3 . . . . . . . . . . . . . . 3
    3 . 3 3 3 3 3 3 3 3 3 3 3 3 . 3
    3 . 3 3 3 3 3 . . 3 3 3 3 3 . 3
    3 . 3 3 3 3 . . . 3 3 3 3 3 . 3
    3 . 3 3 3 3 3 . . 3 3 3 3 3 . 3
    3 . 3 3 3 3 3 . . 3 3 3 3 3 . 3
    3 . 3 3 3 3 3 . . 3 3 3 3 3 . 3
    3 . 3 3 3 3 3 . . 3 3 3 3 3 . 3
    3 . 3 3 3 3 3 . . 3 3 3 3 3 . 3
    3 . 3 3 3 3 3 . . 3 3 3 3 3 . 3
    3 . 3 3 3 3 3 . . 3 3 3 3 3 . 3
    3 . 3 3 3 3 . . . . 3 3 3 3 . 3
    3 . 3 3 3 3 3 3 3 3 3 3 3 3 . 3
    3 . . . . . . . . . . . . . . 3
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3
    `, img`
    6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6
    6 . . . . . . . . . . . . . . 6
    6 . 6 6 6 6 6 6 6 6 6 6 6 6 . 6
    6 . 6 6 6 . . . . . 6 6 6 6 . 6
    6 . 6 6 . 6 6 6 6 . . 6 6 6 . 6
    6 . 6 6 . 6 6 6 6 . . 6 6 6 . 6
    6 . 6 6 6 6 6 6 6 . . 6 6 6 . 6
    6 . 6 6 6 6 6 6 . . . 6 6 6 . 6
    6 . 6 6 6 6 6 . . . 6 6 6 6 . 6
    6 . 6 6 6 6 . . . 6 6 6 6 6 . 6
    6 . 6 6 6 . . . 6 6 6 6 6 6 . 6
    6 . 6 6 . . . 6 6 6 6 6 6 6 . 6
    6 . 6 6 . . . . . . . . 6 6 . 6
    6 . 6 6 6 6 6 6 6 6 6 6 6 6 . 6
    6 . . . . . . . . . . . . . . 6
    6 6 6 6 6 6 6 6 6 6 6 6 6 6 6 6
    `, img`
    4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4
    4 . . . . . . . . . . . . . . 4
    4 . 4 4 4 4 4 4 4 4 4 4 4 4 . 4
    4 . 4 4 4 4 . . . . . 4 4 4 . 4
    4 . 4 4 4 . 4 4 4 4 . . 4 4 . 4
    4 . 4 4 4 4 4 4 4 4 . . 4 4 . 4
    4 . 4 4 4 4 4 4 4 4 . 4 4 4 . 4
    4 . 4 4 4 4 4 4 . . 4 4 4 4 . 4
    4 . 4 4 4 4 4 4 4 4 . 4 4 4 . 4
    4 . 4 4 4 4 4 4 4 4 . . 4 4 . 4
    4 . 4 4 4 4 4 4 4 4 . . 4 4 . 4
    4 . 4 4 4 . 4 4 4 . . . 4 4 . 4
    4 . 4 4 4 4 . . . . . 4 4 4 . 4
    4 . 4 4 4 4 4 4 4 4 4 4 4 4 . 4
    4 . . . . . . . . . . . . . . 4
    4 4 4 4 4 4 4 4 4 4 4 4 4 4 4 4
    `]
```


## 加入遊戲更新

現在我們真的要把這些行星加進遊戲了!把 ``||game:on game update every||`` 積木放到工作區,並把間隔改成 **2000**。

```blocks
game.onUpdateInterval(2000, function () {
})
```

## 生成行星

從 ``||sprites:Sprites||`` 中拖出 ``||variables:projectile from side||``,放進 ``||game:on game update every||`` 裡面。把 ``||sprites:vx||`` 的值設為 `0`。

```blocks
game.onUpdateInterval(2000, function () {
    let projectile = sprites.createProjectileFromSide(img`.`, 0, 50)
})
```

## 設定行星圖片

你剛剛已經畫好了行星,所以我們要從陣列中抓出這些圖片。在 ``||arrays:Arrays||`` 中找到 ``||arrays:get value at||``,把它拖到 ``||variables:projectile from side||`` 積木裡的灰色圖片方框上。點擊提示確認你的程式是否正確!

```blocks
game.onUpdateInterval(2000, function () {
    let projectile = sprites.createProjectileFromSide(list[0], 0, 50)
})
```

## 設定行星位置
在 ``||variables:set projectile to||`` ``||sprites:projectile||`` 積木的正下方放上 ``||sprites:set position to||`` 積木。在下拉選單中把變數改成 ``||variables:projectile||``。你應該會看到一排行星(或是小行星、外星太空船)從遊戲畫面的左側往下走。

```blocks
game.onUpdateInterval(2000, function () {
    let projectile = sprites.createProjectileFromSide(img`.`, 0, 50);
    projectile.x = 0
})
```
## 加入隨機性

讓畫面再刺激一點!

拖出 **兩個** ``||math:pick random 0 to 10||`` 積木。把第一個放進 ``||arrays:get value at||`` 裡面,並把第二個數字改成 **2**。這是 **你清單中的行星數量減一**。

把第二個放進 ``||sprites:set position to||`` 裡面,並把第二個數字改成 **160**,也就是螢幕的寬度。現在你旅行的途中就會不斷有行星出現了!

```blocks
game.onUpdateInterval(2000, function () {
    let projectile = sprites.createProjectileFromSide(list[randint(0, 2)], 0, 50)
    projectile.x = randint(0, 160)
})
```

```template
namespace SpriteKind {
    export const Gas = SpriteKind.create()
}

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

game.onUpdateInterval(5000, function () {
    let fuel = sprites.createProjectileFromSide(img`
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
    fuel.setKind(SpriteKind.Gas)
    fuel.x = randint(0, 160)
})

let statusbar = statusbars.create(20, 4, StatusBarKind.Energy)
statusbar.attachToSprite(mySprite, 3, 0)
game.onUpdateInterval(200, function () {
    statusbar.value += -1
})

sprites.onOverlap(SpriteKind.Player, SpriteKind.Gas, function (sprite, otherSprite) {
    statusbar.value = 100
    otherSprite.destroy()
})

statusbars.onZero(StatusBarKind.Energy, function (status) {
    game.over(false)
})
```

```package
pxt-status-bar=github:jwunderl/pxt-status-bar
```