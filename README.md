# lifegameJS
A lifegame which is using JS.

JSで作ったライフゲームです。(3作目)
- [1作目](https://www.mugisus.com/game_of_life)
- [2作目](https://www.mugisus.com/game_of_life_inf)
- [3作目](https://www.mugisus.com/lifegameJS) ←これ

[lifegame.js](https://github.com/MugiSus/lifegameJS/blob/main/lifegame.js)
速度も速いしソースコードも随分と綺麗になったんじゃないですかね。あと趣味で書いたコードなので可読性には帰ってもらいました。

```js
clientWrite(0, 0, 1);
clientWrite(1, 1, 1);
clientWrite(1, 2, 1);
clientWrite(0, 2, 1);
clientWrite(-1, 2, 1);

for (let i = 0; i < 100; i++) ep = evaluate(ep);
```
これはグライダーを100世代動かすコードです

実行結果はオブジェクトmに出てます

```js
>>> m
22: {25: false, 26: false, 27: false}
23: {24: false, 25: false, 26: false, 27: false, 28: false}
24: {24: false, 25: false, 26: false, 27: true, 28: false}
25: {24: false, 25: true, 26: false, 27: true, 28: false}
26: {24: false, 25: false, 26: true, 27: true, 28: false}
27: {25: false, 26: false, 27: false}
```
trueとfalseでわかりにくいですがちゃんと動いてますね

図示するとこんな感じです
```
 ◻️◻️◻️ 
◻️◻️◻️◻️◻️
◻️◻️◻️◼️◻️
◻️◼️◻️◼️◻️
◻️◻️◼️◼️◻️
 ◻️◻️◻️ 
```
白は`true`、黒は`false`、スペースがあるところは`undefined`です

もっとユーザーフレンドリーなUI作ってるので待っててね。待てない人はconsole開いて遊んでてください。
