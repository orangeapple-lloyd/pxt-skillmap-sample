# 太空探險家


## 簡介 @unplugged

** 一起來探索浩瀚的宇宙吧! **

在這份教學中,你會為這趟旅程設計一艘太空船。

![穿越太空](/static/skillmap/space/space1.gif "穿越星空" )

## 設定場景
**給玩家一點好看的東西** 🔭

---


🔲 從 ``||scene:Scene||`` 分類把 ``||scene:start screen [confetti] effect ⊕||`` 拖出來,放進工作區裡已經有的 ``||loops:on start||`` 積木中。

🔲 接著從下拉選單中選擇 ``||scene:star field||``(取代 ``||scene:confetti||``),看著你的太空船衝進宇宙吧!🚀 


---


```blocks
// @highlight
effects.starField.startScreenEffect()
```



## 畫出你的太空船
**🧑🏿‍🚀 來挑選我們的太空船吧!👩🏾‍🚀**

---

🔲 從 ``||sprites:Sprites||`` 分類拖出 ``||variables:set [mySprite] to sprite [ ] of kind [Player]||`` 
積木,把它放在 ``||loops:on start||`` 容器的最後面。

🔲 點擊
 ``||variables:set [mySprite] to sprite [ ] of kind [Player]||`` 積木中間的灰色方框,
設計一艘屬於你自己的太空船!你想當生鏽的破銅爛鐵,還是流線型的未來感火箭呢?

---

**小提示:** 不想自己畫太空船嗎?進入角色編輯器後,切換到圖庫就可以挑選現成的圖片。

```blocks
effects.starField.startScreenEffect()
// @highlight
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
```

## 操控你的太空船

🌟 來讓你的太空船動起來吧 🌟

---

🔲 找到 ``||controller:move [mySprite] with buttons ⊕||`` 積木,
把它拖到 ``||loops:on start||`` 容器的最下面。

** 現在試試看在模擬器中移動你的太空船! **  
你可以用搖桿、方向鍵,或是 **W A S D** 鍵來操控太空船。  



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
// @highlight
controller.moveSprite(mySprite)
```

## 留在畫面內

**糟糕!如果你移出畫面外,你的太空船就會消失不見!**

---

🔲 為了不讓你的太空船跑出畫面邊界,找到
 ``||sprites:set [mySprite] stay in screen <on>||`` 積木,
把它接在程式的最後面。
 


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
// @highlight
mySprite.setStayInScreen(true)

```


## 大結局 @unplugged

**做得好!**

---

點擊教學上的完成按鈕之前,
記得先在模擬器上實際玩玩看你的遊戲。  

![你在太空中](/static/skillmap/space/space1end.gif "在自己的遊戲中翱翔" )

一切都符合你想要的樣子了嗎?如果發現有想調整的地方,
你隨時可以回到前面的步驟編輯。



## 掰掰

** 🚀 就是這樣!🚀**

你已經準備好遨遊整個宇宙了!

點擊 **「Finish」** 就能發佈你的遊戲,跟家人朋友一起分享。
