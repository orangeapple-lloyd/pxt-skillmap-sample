# 認識 MakeCode Arcade


```ghost
let mySprite: Sprite = null;
mySprite.startEffect(effects.spray)
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    game.showLongText("The little unicorn walked into the meadow.", DialogLayout.Top)
    scene.cameraShake(4, 500)
})
scene.setBackgroundColor(9)
scene.setBackgroundImage()
mySprite.x += 0
effects.confetti.startScreenEffect()
effects.confetti.endScreenEffect()
mySprite.setPosition(70, 80)
for (let index = 0; index < 4; index++) {
    controller.moveSprite(mySprite)
    music.setVolume(20)
    music.playMelody("- - - - - - - - ", 120)
}
game.onUpdateInterval(5000, function () {
    if (game.askForString("Continue?") == "Y" || game.askForString("Continue?") == "y") {
        mySprite.say(":)")
    }
    game.splash("")
})

```

### @explicitHints true

## 簡介 @unplugged

![興奮的猴子](/static/skillmap/interface/monkey.png "興奮的猴子準備好了!" )

**準備好開始寫自己的遊戲了嗎?**

完成這份教學,你會學到:
- 跟著教學的步驟操作
- 在積木工具箱中找到積木
- 在工作區中組合程式
- 在內建模擬器上執行你的遊戲

不知不覺中,你就會擁有一款屬於自己的 Arcade 遊戲!

## 步驟 1 

**⭐歡迎⭐**

你剛剛發現了跟著教學操作最重要的一件事 —— 讀說明!

如果你看不到完整的說明,點擊下方的 **[v 更多...]** 展開內容。

---

當你準備好進入下一步時,點擊 **[ >  下一步]** 繼續。  


## 步驟 2

這個方框會顯示每一步的說明資訊。

如果你需要更多資訊,點擊右側的燈泡,可以得到額外的提示。


#### ~ tutorialhint 
```
**你發現提示了!**
```


## 使用工作區

現在我們來談談你的 [__*工作區*__](#workIt "組合程式的區域")。

工作區是說明下方的區域,你會在這裡把積木接在一起,組合成你的程式。並不是所有積木都能互相連接,我們稍後會再說明。

---

🔲 點擊 ``||game:splash "___"||`` 積木裡的文字區域,把目前的句子改成更有趣的內容。

---

**小提示:** 你有注意到剛剛第一次出現「__工作區__」這個詞時,長得不太一樣嗎?我們會不時為重要的詞彙加上特殊樣式。把滑鼠移到上面就可以看到定義。

#### ~ tutorialhint 
```blocks
game.splash("I like bananas!")
```

```template
game.splash("These blocks are in your workspace!")

```

## 認識積木  @unplugged

積木可以從 [__*工具箱*__](#tools "工作區左側列出積木分類的長條區域") 拖出來,進行連接、複製與刪除。

繼續往下,了解更多積木的用法。

![積木動畫](/static/skillmap/interface/use_blocks.gif "積木的出現、複製與刪除。" )



## 你的工具箱

**你需要用到的積木,並不一定一開始就在工作區裡。**

說明中,你需要找的積木描述通常會用和工具箱分類相同的顏色標記。

**舉例來說:** 當我們希望你找出下面這個積木時,會寫成 ``||game:splash "___"||``:

```block
game.splash(" ")
```

這個積木會在你的專案中加上一個 [__*啟動畫面*__](#splasht "程式或關卡載入時顯示的全螢幕訊息")。

## 你的工具箱 2



**來看看實際怎麼操作**

🔲 找到 ``||scene:set background color to [ ]||`` 積木,把它接在工作區中已經有的 **on start** 容器的最上面。

#### ~ tutorialhint 
```blocks
scene.setBackgroundColor(0)
game.splash("My monkey is better than yours")
```



## 例外狀況

每條規則都會有例外,我們來看看其中一個顏色和所在分類不同的積木。

``||variables:set [mySprite] to sprite [ ] of kind [Player]||`` 這個積木是紅色的,但它住在 ``||sprites:Sprites||`` 分類裡面。

---

<!-- **小提示:** 找不到想要的積木時,可以試試 -->


🔲 把 ``||variables:set [my sprite] to sprite [ ] of kind [Player]||`` 接到 **on start** 容器的最後面,玩一玩,讓畫面上出現一個 [__*角色*__](#sprote "在螢幕上移動的 2D 圖像")。

*(把滑鼠移到上面的「__角色__」可以看到定義。)*

---

**小提示:** 把 ``||game:splash "___"||`` 從 ``||loops:on start||`` 容器中拖出來,丟回工具箱即可刪除它,你的角色就會出現!

#### ~ tutorialhint

![開啟圖像編輯器](/static/skillmap/misc/open-image-editor-small.gif "如何開啟圖像編輯器。" )

---



```blocks
scene.setBackgroundColor(5)
let mySprite = sprites.create(img`
    e e e . . . . e e e . . . . 
    c d d c . . c d d c . . . . 
    c b d d f f d d b c . . . . 
    c 3 b d d b d b 3 c . . . . 
    f b 3 d d d d 3 b f . . . . 
    e d d d d d d d d e . . . . 
    e d f d d d d f d e . b f b 
    f d d f d d f d d f . f d f 
    f b d d b b d d 2 f . f d f 
    . f 2 2 2 2 2 2 b b f f d f 
    . f b d d d d d d b b d b f 
    . f d d d d d b d d f f f . 
    . f d f f f d f f d f . . . 
    . f f . . f f . . f f . . . 
    `, SpriteKind.Player)
```


## 容器積木

**接下來看看不同類型的積木,以及它們怎麼使用。** 

首先是 [__*容器積木*__](#blockIt "可以裝其他積木的積木")。容器積木的上下兩端各有一條邊,中間留有空白,讓其他積木可以扣進去。容器積木控制裡面的程式碼*什麼時候*執行。範例如下:

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
	
})
```
---

🔲  找到 ``||controller:on [A] button pressed ||`` 容器積木,把它拖到工作區。下個步驟會繼續加東西進去。

#### ~ tutorialhint

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    let mySprite: Sprite = null
})
```

## 一般積木

接下來是 [__*一般積木*__](#sBlockIt "佔大多數程式的單行積木")。一般積木是上下都有凸起或凹陷的單行積木,可以扣在其他積木之間。這類積木會依照它們在容器中由上到下的順序執行。

下面是一般積木的範例:

```block
let mySprite: Sprite = null;
mySprite.startEffect(effects.spray)
```

---

🔲  找到 ``||sprites:[mySprite] start [spray] effect ||`` 積木,把它接到 **on A button pressed** 容器裡⋯⋯然後選一個你自己喜歡的特效!

#### ~ tutorialhint
```blocks
let mySprite: Sprite = null;

controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.startEffect(effects.confetti)
})
```



## 數值積木

最後是 [__*數值積木*__](#aBlockIt "為其他積木提供數值的特別積木")。數值積木是會把資訊填入其他積木的特別積木。它們有時是尖角、有時是圓角,但一定要嵌在其他積木裡才能用。數值積木看起來像這樣:

![數值積木](/static/skillmap/interface/parameter-blocks.png "這是數值積木的形狀。" )

---

🔲  把 ``||sprites:[mySprite] say [":)"] ||`` 積木接到 **on A button pressed** 容器的最後面。

🔲  找到 ``||game: ask for number [" "] ||`` 數值積木,塞進去取代 **":)"**。

---

**小提示:** 數值積木會依照它提供的資訊類型,呈現不同形狀。每種數值只能嵌進特定形狀的空格裡。

#### ~ tutorialhint
```blocks
let mySprite: Sprite = null;

controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    mySprite.say(game.askForNumber(""))
})
```

## 組合起來

🎨 現在發揮你的創意 🎨

可以看看我們在工具箱裡加進來的其他積木。

不知道它們是做什麼用的也沒關係。試著用看看,觀察它們對遊戲有什麼影響!

---

**小提示:** 你隨時都可以用左側的模擬器測試遊戲!按重新整理按鈕(🔄)重新載入,然後用你設定的按鈕操作遊戲!  



## 結語 

🎈 恭喜你 🎈 

你已經學會所有進入下一份教學所需要的基礎了。

繼續學習,你會掌握更多在 MakeCode Arcade 中製作遊戲的技巧!  
