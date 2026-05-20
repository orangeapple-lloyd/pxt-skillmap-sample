# 敵人 AI

```jres
{
    "transparency16": {
        "data": "hwQQABAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA==",
        "mimeType": "image/x-mkcd-f4",
        "tilemapTile": true
    },
    "tile1": {
        "data": "hwQQABAAAADMzMzMzMzMzLy7u7u7u7vLvMvMzMzMvMu8vMzMzMzLy7zMy8zMvMzLvMy8zMzLzMu8zMzLvMzMy7zMzLzLzMzLvMzMvMvMzMu8zMzLvMzMy7zMvMzMy8zLvMzLzMy8zMu8vMzMzMzLy7zLzMzMzLzLvLu7u7u7u8vMzMzMzMzMzA==",
        "mimeType": "image/x-mkcd-f4",
        "tilemapTile": true
    },
    "tile2": {
        "data": "hwQQABAAAAAiIiIiIiIiIkJEREREREQkQiIiIiIiIiRCIiIiIiIiJEIiREQiIiIkQkJERCIkJCRCQiREJCQkJEJCREQiQiIkQkJERCRCIiRCQiREIiQkJEIiREQkJCQkQiIiIiIiIiRCIiIiIiIiJEIiIiIiIiIkQkRERERERCQiIiIiIiIiIg==",
        "mimeType": "image/x-mkcd-f4",
        "tilemapTile": true
    },
    "tile3": {
        "data": "hwQQABAAAAB3d3d3d3d3d1dVVVVVVVV1V3d3d3d3d3VXd3d3d3d3dVdXVVVVVXd1V1dXV3d3d3VXV3VVd3d3dVdXV1d3d3d1V3d1dXV3d3VXd1VXdXd3dVd3dXV1d3d1V3dVVXV3d3VXd3d3d3d3dVd3d3d3d3d1V1VVVVVVVXV3d3d3d3d3dw==",
        "mimeType": "image/x-mkcd-f4",
        "tilemapTile": true
    },
    "tile4": {
        "data": "hwQQABAAAABERERERERERFRVVVVVVVVFVEREREREREVURFRFRERERVRERVRERERFVFRVVUVEREVUVFVVVURFRVRUVVVVVUVFVFRVVVVVRUVUVFVVVURFRVRUVVVFRERFVERFVEREREVURFRFRERERVRERERERERFVFVVVVVVVUVERERERERERA==",
        "mimeType": "image/x-mkcd-f4",
        "tilemapTile": true
    },
    "tile5": {
        "data": "hwQQABAAAACqqqqqqqqqqrq7u7u7u7uruqqqqqqqqqu6qqqqqqqqq7qqqqqqqqqruqqqqqqqqqu6qrurqqqqq7q6u7u7uqururq7u7u6q6u6qrurqqqqq7qqqqqqqqqruqqqqqqqqqu6qqqqqqqqq7qqqqqqqqqruru7u7u7u6uqqqqqqqqqqg==",
        "mimeType": "image/x-mkcd-f4",
        "tilemapTile": true
    },
    "level": {
        "id": "level",
        "mimeType": "application/mkcd-tilemap",
        "data": "MTAxZTAwMGEwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDIwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDA0MDAwMDAwMDAwMDAwMDQwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAzMDAwMDAwMDEwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMTAxMDEwMDAwMDEwMDAwMDUwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDEwMTAxMDEwMTAxMDEwMTAxMDEwMDAwMDAwMDAwMDUwMDAwMDAwMDAwMDUwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAyMDAwMDIwMDAwMDAwMDAwMDAwMDAwMDIwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMjIwMjIwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDIwMjIyMjIyMjIwMjAwMDAwMDAwMDAyMDIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMg==",
        "tileset": [
            "myTiles.transparency16",
            "myTiles.tile1",
            "myTiles.tile3",
            "myTiles.tile4",
            "myTiles.tile5",
            "myTiles.tile2"
        ]
    },
    
    "level2": {
        "id": "level2",
        "mimeType": "application/mkcd-tilemap",
        "data": "MTAxZTAwMGEwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDQwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDIwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDQwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAzMDAwMDAwMDAwMTAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwNDAwMDAwMDAwMDAwMDAwMDAwMTAxMDUwMDAwMDEwMTAwMDAwMDAwMDEwMDAwMDAwMDAwMDAwMTAwMDAwMDAwMDUwMTAxMDEwMDAwMDEwMDAxMDUwNTAxMDEwMTAwMDAwMDAxMDEwMDAwMDAwMDAwMDAwMTAxMDAwMDAwMDAwMDAwMDEwMTAxMDEwMTAxMDUwNTAxMDAwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTAxMDEwMTA1MDUwNTA1MDAwMTAwMDEwMDAxMDUwNTAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMjAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMjAwMDAwMDAwMDAwMDAwMDAwMDAwMDIwMDAwMDAwMDAwMDAyMDAwMDAwMDAwMjIwMDIwMDIwMDIwMDAwMDAwMDIwMDAwMjIwMjIwMjAwMDIyMDIwMDIyMDAwMDAwMjIwMDAwMDAyMjIyMjIwMDAyMjIyMjIyMjIyMjIyMjIyMjAwMDAyMDIwMjAwMA==",
        "tileset": [
            "myTiles.transparency16",
            "myTiles.tile1",
            "myTiles.tile3",
            "myTiles.tile4",
            "myTiles.tile5",
            "myTiles.tile2"
        ]
    },

    "*": {
        "mimeType": "image/x-mkcd-f4",
        "dataEncoding": "base64",
        "namespace": "myTiles"
    }
}
```




 

```template
scene.onOverlapTile(SpriteKind.Player, myTiles.tile2, function (sprite, location) {
    game.over(false)
})
scene.onOverlapTile(SpriteKind.Player, myTiles.tile4, function (sprite, location) {
    startNextLevel()
})
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.vy = -200
})
function startNextLevel () {
    for (let value of sprites.allOfKind(SpriteKind.Enemy)) {
        value.destroy()
    }
    currentLevel += 1
    if (currentLevel == 1) {
        scene.setBackgroundColor(11)
        tiles.setTilemap(tilemap`level`)
    } else if (currentLevel == 2) {
        scene.setBackgroundColor(9)
        tiles.setTilemap(tilemap`level2`)
    } else {
        game.over(true)
    }
    tiles.placeOnRandomTile(mySprite, myTiles.tile3)
    for (let value of tiles.getTilesByType(myTiles.tile5)) {
        myEnemy = sprites.create(img`
            a a a a a a a a a a a a a a a a 
            a b b b b b b b b b b b b b b a 
            a b a a a a a a a a a a a a b a 
            a b a a b b a a a a b b a a b a 
            a b a a a a b a a b a a a a b a 
            a b a a a a a a a a a a a a b a 
            a b a a a b a a a a b a a a b a 
            a b a a a b a a a a b a a a b a 
            a b a a a a a a a a a a a a b a 
            a b a a a a a a a a a a a a b a 
            a b a a a b b b b b b a a a b a 
            a b a a b a a a a a a b a a b a 
            a b a a a a a a a a a a a a b a 
            a b a a a a a a a a a a a a b a 
            a b b b b b b b b b b b b b b a 
            a a a a a a a a a a a a a a a a 
            `, SpriteKind.Enemy)
        tiles.placeOnTile(myEnemy, value)
        myEnemy.follow(mySprite, 30)
    }
}
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    otherSprite.destroy()
    if (sprite.bottom < otherSprite.y) {
        sprite.vy = -100
    } else {
        info.changeLifeBy(-1)
    }
})
let myEnemy: Sprite = null
let currentLevel = 0
let mySprite: Sprite = null
mySprite = sprites.create(img`
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    3 1 1 1 1 1 1 1 1 1 1 1 1 1 1 3 
    3 1 3 3 3 3 3 3 3 3 3 3 3 3 1 3 
    3 1 3 3 3 3 3 3 3 3 3 3 3 3 1 3 
    3 1 3 3 3 3 3 3 3 3 3 3 3 3 1 3 
    3 1 3 3 1 1 1 3 3 3 1 3 3 3 1 3 
    3 1 3 3 1 3 3 1 3 1 1 3 3 3 1 3 
    3 1 3 3 1 3 3 1 3 3 1 3 3 3 1 3 
    3 1 3 3 1 1 1 3 3 3 1 3 3 3 1 3 
    3 1 3 3 1 3 3 3 3 3 1 3 3 3 1 3 
    3 1 3 3 1 3 3 3 3 1 1 1 3 3 1 3 
    3 1 3 3 3 3 3 3 3 3 3 3 3 3 1 3 
    3 1 3 3 3 3 3 3 3 3 3 3 3 3 1 3 
    3 1 3 3 3 3 3 3 3 3 3 3 3 3 1 3 
    3 1 1 1 1 1 1 1 1 1 1 1 1 1 1 3 
    3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 3 
    `, SpriteKind.Player)
mySprite.ay = 500
controller.moveSprite(mySprite, 100, 0)
scene.cameraFollowSprite(mySprite)
info.setLife(3)
startNextLevel()

```

## Start @unplugged

是不是覺得上一個遊戲裡的敵人有點⋯⋯嗯⋯⋯笨笨的?

在這節課裡,我們會學習如何用簡單的 [_**AI**_](#fakeSmart "人工智慧") 讓敵人變得更聰明。

![關卡與函式](/static/skillmaps/platformer/platformer5.gif "來點全新的東西!也有一點和以前一樣的部分。")



## AI 規則 @unplugged

這個專案的程式碼會從紫色的 **[ ! ]** 圖塊產生敵人。
敵人一出現就會立刻往左移動,然後被牆壁卡住⋯⋯所以我們要加入邏輯,避免敵人被擋下來。
<hr/>
**敵人需要遵守兩條規則:**

1. **如果敵人快要撞到牆,就會嘗試跳過去**  
2. **如果敵人真的撞到牆,就會轉身**

<hr/>

這兩條規則都有一個 *條件* 和一個 *動作*。  

當條件成立時,就會執行對應的動作。
我們需要寫程式持續檢查這兩個條件是否成立。

## 迴圈 pt. 1

首先,我們需要一個 **on game update** 容器,每當遊戲中有東西改變時就會觸發程式碼。在容器內,我們會用一個迴圈來逐一檢查每個敵人。
<hr/>

🔲 拖出一個 ``||game:on game update||`` 積木,放到工作區。

🔲 把一個 ``||loops: for element [value] of [list]||`` 積木扣進
**on game update** 容器裡。

```blocks
let list: number[] = [];
game.onUpdate(function () {
    for (let value of list) {
    }
})
```

## 迴圈 pt. 2

每次更新時,我們希望迴圈去檢查遊戲中的每一個敵人。
要做到這件事,我們會用和前面教學一樣的方法。
<hr/>

🔲 從 ``||sprites:Sprites||`` 分類中,從 **set sprite list to** 積木裡面抓出
``||sprites:array of sprites of kind||`` 積木。


🔲 把它放進 **for element** 迴圈裡,取代 ``||variables: list||`` 變數。

🔲 把「kind」下拉選單改成 **Enemy**。  
<br/>

```blocks
game.onUpdate(function () {
    for (let value of sprites.allOfKind(SpriteKind.Enemy)) {
    }
})
```

## 跳躍 pt. 1

讓我們開始寫第一條規則的程式碼:

> 1. **如果敵人快要撞到牆,就會嘗試跳過去**  
<hr/>

🔲 我們需要檢查 **if**(如果) 某件事是真的。要做到這件事,把
一個 ``||logic: if <true> then||`` 邏輯容器拖進空的 **on game update** 容器裡。

🔲 接著要確認敵人沒有正在跳躍,把空的 **if/then** 標頭裡的
``||logic: <true>||`` 替換成 ``||scene: is [mySprite] hitting wall [left]||``。

🔲 把 ``||variables: mySprite||`` 換成 ``||variables: value||``,確保檢查的是目前這個敵人。

🔲 把 **left** 改成 **bottom**,檢查角色的底部是不是踩在地上。


```blocks
game.onUpdate(function () {
    for (let value of sprites.allOfKind(SpriteKind.Enemy)) {
        if (value.isHittingTile(CollisionDirection.Bottom)) {
           
        }
    }
})
```

## 跳躍 pt. 2

現在我們知道敵人在地上了,接下來有兩種情況需要讓它跳起來。
 - 如果它往左移動,而且左邊有牆
 - 如果它往右移動,而且右邊有牆

我們會用一個新的 **if/then** 來判斷其中哪一種情況發生。
<hr/>

🔲 拖出另一個 ``||logic:if <true> then||`` 積木,把它放進 **for element** 迴圈裡
那個已經存在、還是空的 **if/then** 裡面。

🔲 要同時檢查兩件事是不是都成立(往左移動 **而且** 左邊有牆),
拉一個 ``||logic: < > and < >||`` 來取代新的 **if/else** 裡的 ``||logic:<true>||`` 參數。

🔲 在右邊的空格(也就是 **=** 右邊)扣上一個 ``||scene: tile to the [left] of [mySprite] is [ ]||``。

🔲 把 ``||variables: mySprite||`` 換成 ``||variables: value||``,並把空白圖塊換成 **[X]**。

🔲 在 **=** 的左邊塞進一個 ``||logic: [0] [<] [0]||`` 積木。
下一步我們會繼續處理它。  

<br/>

```blocks
game.onUpdate(function () {
    for (let value of sprites.allOfKind(SpriteKind.Enemy)) {
        if (value.isHittingTile(CollisionDirection.Bottom)) {
            if (0 < 0 && value.tileKindAt(TileDirection.Left, myTiles.tile1)) {
               
            } 
})
```

## 跳躍 pt. 3

我們已經會檢查左邊下一個圖塊是不是牆了,
但這件事只有在敵人往左移動時才有意義。

接下來來加上判斷敵人有沒有往左移動的程式碼。
<hr/>
在 Arcade 系統裡,左邊是負的,右邊是正的。要確認角色
正在往左移動,就要確認它在 x 方向的速度
是負值。

🔲 抓一個 ``||sprites: [mySprite] [x]||`` 參數積木,取代 ``||logic: [0] [<] [0]||`` 裡的第一個 **0**。

🔲 把 ``||variables: mySprite||`` 換成 ``||variables: value||``,然後把
**x** 改成 **vx (velocity x)**。   
<br/>


```blocks
game.onUpdate(function () {
    for (let value of sprites.allOfKind(SpriteKind.Enemy)) {
        if (value.isHittingTile(CollisionDirection.Bottom)) {
            if (value.vx < 0 && value.tileKindAt(TileDirection.Left, myTiles.tile1)) {
            }    
        }
    }
})
```


## 跳躍 pt. 6

如果電腦執行到這一行,就代表
是讓敵人跳起來的時候了。
<hr/>

🔲 在剛剛建立好的 **if/else** 裡面,接上一個 ``||sprites:set [mySprite] [x] to [0]||`` 積木。

🔲 把 ``||variables: mySprite||`` 換成 ``||variables: value||``,然後把
``||sprites: x||`` 換成 ``||sprites: vy (velocity y)||``。

🔲 把 **0** 改成 **-150**。  
<br/>

```blocks
game.onUpdate(function () {
    for (let value of sprites.allOfKind(SpriteKind.Enemy)) {
        if (value.isHittingTile(CollisionDirection.Bottom)) {
            if (value.vx < 0 && value.tileKindAt(TileDirection.Left, myTiles.tile1)) {
                value.vy = -150
            } 
    }
})
```


## 跳躍 pt. 7

接著,我們要在右邊也加上類似的程式碼。
<hr/>

🔲 在剛剛完成的最內層 **if/else** 底部,點兩次 **⊕** 按鈕,
先新增一個 **else**,再新增一個 **else if** 子句。

🔲 把整個 **and** 條件複製一份,然後把複製的這份放進 **else if** 子句的標頭。

🔲 在新的子句裡,把 **<** 改成 **>**,把 **left** 改成 **right**。

🔲 複製 ``||sprites:set [value] [vy (velocity y)] to [-150]||`` 積木,
把複製的這份扣進空的 **else if** 裡面。

🔲 這個 **if/else if** 已經處理完了,你可以點 **else** 子句旁邊的
**⊖** 按鈕,把它從積木上移除。

<br/>

```blocks
game.onUpdate(function () {
    for (let value of sprites.allOfKind(SpriteKind.Enemy)) {
        if (value.isHittingTile(CollisionDirection.Bottom)) {
            if (value.vx < 0 && value.tileKindAt(TileDirection.Left, myTiles.tile1)) {
                value.vy = -150
            } else if (value.vx > 0 && value.tileKindAt(TileDirection.Right, myTiles.tile1)) {
                value.vy = -150
            }
        } 
    }
})
```


## 撞牆反彈 pt. 1

我們已經完成規則 #1 的程式碼,現在來看規則 #2。

> 2. **如果敵人真的撞到牆,就會轉身**

<hr/>
敵人在地上行走且沒有撞牆的情況已經處理好了。
接下來要加上敵人已經在跳躍時、左邊或右邊撞到牆
的情況。

🔲 在最外層 **if/else**(**if <is value hitting wall bottom> then**)的底部,
點三次 **⊕** 按鈕,新增一個 **else** 和兩個 **else if** 子句。

🔲 把 ``||scene: is [value] hitting wall [bottom]||`` 參數複製兩份,
分別放進兩個新的 **else if** 標頭裡。

🔲 在第一個 **else if** 裡把 **bottom** 改成 **left**。

🔲 在第二個 **else if** 裡把 **bottom** 改成 **right**。  
<br/>

```blocks
game.onUpdate(function () {
    for (let value of sprites.allOfKind(SpriteKind.Enemy)) {
        if (value.isHittingTile(CollisionDirection.Bottom)) {
            if (value.vx < 0 && value.tileKindAt(TileDirection.Left, myTiles.tile1)) {
                value.vy = -150
            } else if (value.vx > 0 && value.tileKindAt(TileDirection.Right, myTiles.tile1)) {
                value.vy = -150
            }
        } else if (value.isHittingTile(CollisionDirection.Left)) {

        } else if (value.isHittingTile(CollisionDirection.Right)) {
 
        }
    }
})
```

## 撞牆反彈 pt. 2

最後,我們要加上程式碼讓敵人在原本往左走時改成往右,
原本往右走時改成往左。
<hr/>

🔲 把原本 **if/then** 子句裡的 ``||sprites:set [value] [vy (velocity y)] to [-150]||`` 積木複製兩份,
分別扣進兩個空的 **else if** 子句裡。

🔲 在第一個 **else if** 子句(**else if <is value hitting wall left> then**)
的 **set value** 積木裡,把 **vy (velocity y)** 改成 **vx (velocity x)**,把 **-150** 改成 **30**。

🔲 在第二個 **else if** 子句(**else if <is value hitting wall right> then**)
的 **set value** 積木裡,把 **vy (velocity y)** 改成 **vx (velocity x)**,把 **-150** 改成 **-30**。


```blocks
game.onUpdate(function () {
    for (let value of sprites.allOfKind(SpriteKind.Enemy)) {
        if (value.isHittingTile(CollisionDirection.Bottom)) {
            if (value.vx < 0 && value.tileKindAt(TileDirection.Left, myTiles.tile1)) {
                value.vy = -150
            } else if (value.vx > 0 && value.tileKindAt(TileDirection.Right, myTiles.tile1)) {
                value.vy = -150
            }
        } else if (value.isHittingTile(CollisionDirection.Left)) {
            value.vx = 30
        } else if (value.isHittingTile(CollisionDirection.Right)) {
            value.vx = -30
        }
    }
})
```


## Finish

🎊 恭喜你 🎊

你已經做出一款有多個關卡、互動圖塊地圖,還有聰明敵人的 Arcade 遊戲了!記得自己玩一遍,然後分享給朋友。

Arcade 還有許多功能我們在這裡沒有介紹到。如果你還有時間,
可以點到 Arcade 主頁,用完整的編輯器自由玩玩看,
做出一款完全屬於你自己的遊戲!
