---
marp: true
theme: unimagic
paginate: true
header: ''
footer: '**出入りできる絵画ギミックを作ろう / ねこぼっくす**'
size: 16:9
---

<!--
==================================================
# TODO list
- [x] 自己紹介とアジェンダの間にこの授業で得られる事、嬉しい事についてアイスブレイクを兼用したスライドを入れる
- [x] クイズセクションの削除
- [x] タイトルコールの印象を変える
- [x] タイトルを6章構成にする
- [x] Stencilは難しいのでなじみ深い例を出す(壁裏の敵ハイライト等)
- [x] アジェンダを目次/コンテンツ/本日の流れ等に変える
- [x] 「可視性に条件を設定するモノ」という表現はわかりづらいので変えたい=>今回は削除する方向に
- [x] 「Dissolveの条件一覧」を「Dissolveのエフェクトの種類」と書き換える
- [x] ステンシルの条件の前にliltoonのStencilプリセットの説明を持ってくる
- [x] 「絵画ギミックを実際に作ってみよう」は授業では完成系の紹介にとどめて後日見てもらうように
- [x] 振り返りを現状の内容に合わせて書き換える
- [x] 参考資料の欄にliltoonのドキュメントを追加する
==================================================
-->

<!-- _class: titlecall -->
# 出入りできる絵画ギミックを作ろう<br>(Dissolve / Stencil)
- **(ここで盛大に絵画ギミックで登場！！)**

---

<!-- _class: bg -->

![bg right](../images/Nekobox_Picture_01.png)

## 講師紹介
名前: ねこぼっくす
好きなもの: 紅茶と焼き菓子
最近ハマってること: Resonite

---

<!-- _class: added -->

## この講義を受けるとうれしいこと

1. 市販の **ギミックの中身がわかる** ようになる
2. **ギミック高い！買えない→自分で作ろう！** の様に **できない** が **できる** に **変わる**
3. アイテムの**見た目の遷移をよりリッチに**表現できる

---

## <span class="changed">本日の流れ</span>

1. Dissolve ってなに？
2. Dissolveでの消失エフェクトについて
3. Stencil ってなに？
4. Stencilでのマスク表現について
5. 組み合わせるとどうなる？
6. 絵画ギミックを実際に作ってみよう

---

<!-- _class: titlecall -->
<!-- header: '**1. Dissolve ってなに？**' -->

# 1. <span class="changed">Dissolve ってなに？</span>
2. Dissolveでの消失エフェクトについて
3. Stencil ってなに？
4. Stencilでのマスク表現について
5. 組み合わせるとどうなる？
6. 絵画ギミックを実際に作ってみよう

---

<!-- _class: removed -->

## Q. Dissolve / Stencil ってなに？
## A.「可視性に条件を設定するモノ」

---

<!-- _class: bg moved -->

![bg right vertical](https://placehold.jp/32/444444/bfffbf/720x1280.png?text=お着替えギミックの動作.gif)
![bg](https://placehold.jp/32/444444/bfffbf/720x1280.png?text=分身ギミックの動作.gif)

## <span>Dissolve</span> ってこんな感じ

---

<!-- _class: moved -->

## <span>Dissolve(溶解)</span> とは
- **条件を満たした部分を(溶かしたように)見えなくするモノ**
- 小物や衣装の「フェードイン/フェードアウト」によく使われる

---

<!-- _class: titlecall -->
<!-- header: '**2. Dissolveでの消失エフェクトについて**' -->

1. Dissolve ってなに？
# 2. Dissolveでの消失エフェクトについて
3. Stencil ってなに？
4. Stencilでのマスク表現について
5. 組み合わせるとどうなる？
6. 絵画ギミックを実際に作ってみよう

---

## <span class="changed"><span>Dissolve</span>のエフェクトの種類</span>
- **座標**: ルートボーンや原点からの距離もしくは方向で溶ける部分を指定
- **透明度**: テクスチャの透明度で溶ける部分を指定
- **UV**: テクスチャの中心からの距離もしくは方向で溶ける部分を指定

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=Dissolve(座標)の動作.gif)

### <span>Dissolve(座標)</span>の動作
ルートボーンや原点からの距離もしくは方向で溶ける部分を指定

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=Dissolve(透明度)の動作.gif)

### <span>Dissolve(透明度)</span>の動作
テクスチャの透明度で溶ける部分を指定

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=Dissolve(UV)の動作.gif)

### <span>Dissolve(UV)</span>の動作
テクスチャの中心からの距離もしくは方向で溶ける部分を指定

---

<!-- _class: removed -->

## クイズ: Dissolve(座標)のルートボーンを動かすとどうなる？
みんなで考えてみよう！

---

<!-- _class: removed -->

## Q. Dissolve(座標)のルートボーンを動かすとどうなる？
## A. 溶け始める位置や方向を変えられる

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=Dissolve(座標)のルートボーンを動かした時の動作.gif)

### <span>Dissolve(座標)</span>のルートボーンを動かした時の動作
溶け始める位置や方向を変えられる

---

<!-- _class: titlecall -->
<!-- header: '**3. Stencil ってなに？**' -->

1. Dissolve ってなに？
2. Dissolveでの消失エフェクトについて
# 3. <span class="added">Stencil ってなに？</span>
4. Stencilでのマスク表現について
5. 組み合わせるとどうなる？
6. 絵画ギミックを実際に作ってみよう

---

<!-- _class: bg moved -->

![bg right vertical](https://placehold.jp/32/444444/bfffbf/720x1280.png?text=目に髪がかかっても目が浮いて見える様子.gif)
![bg](https://placehold.jp/32/444444/bfffbf/720x1280.png?text=箱の中だけ別世界の動作.gif)

## <span>Stencil</span>ってこんな感じ

---

<!-- _class: moved -->

## <span>Stencil(型紙)</span> とは
- **条件を満たした部分を(型紙のように)切り抜くモノ**
- いわゆる「マスク」を動的に行える

---

<!-- _class: titlecall -->
<!-- header: '**4. Stencilでのマスク表現について**' -->

1. Dissolve ってなに？
2. Dissolveでの消失エフェクトについて
3. Stencil ってなに？
# 4. Stencilでのマスク表現について
5. 組み合わせるとどうなる？
6. 絵画ギミックを実際に作ってみよう

---

<!-- _class: moved -->

## liltoonにおける<span>Stencil</span>のプリセット
- **Writer**: オブジェクトに<span class="changed">Refの値</span>を設定する
- **Reader**: Writer越しに見たときにRefの値が同じなら非表示 (NotEqual)
- **Reader(反転)**: Writer越しに見たときにRefの値が同じなら表示 (Equal)

---

<!-- _class: moved -->

## <span>Stencil</span>の主な条件式
- **Always**: <span class="changed">Refの値</span>を参照せず常に表示、liltoonのデフォルトはこれ
- **Equal**: 指定したRefと等しいオブジェクト越しに見たときだけ表示
- **NotEqual**: 指定したRefと等しいオブジェクト越しに見た時だけ非表示

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=Stencil(Reader)の動作.gif)

### Readerの動作

Writer越しに見たときにRefの値が同じなら非表示 (NotEqual)

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=Stencil(Reader反転)の動作.gif)

### Reader(反転)の動作

Writer越しに見たときにRefの値が同じなら表示 (Equal)

---

<!-- _class: removed -->

## クイズ: ReaderとReader(反転)のマテリアルを同時に入れたらどうなる？
みんなで考えてみよう！

---

<!-- _class: removed -->

## Q. ReaderとReader(反転)のマテリアルを同時に入れたらどうなる？
## A. 共存して両方が個別の条件で表示される

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=Stencil(ReaderとReader反転)のマテリアルを同時に入れた時の動作.gif)

### ReaderとReader(反転)のマテリアルを同時に入れた時の動作

共存して両方が個別の条件で表示される

---

<!-- _class: titlecall -->
<!-- header: '**5. 組み合わせるとどうなる？**' -->

1. Dissolve ってなに？
2. Dissolveでの消失エフェクトについて
3. Stencil ってなに？
4. Stencilでのマスク表現について
# 5. 組み合わせるとどうなる？
6. 絵画ギミックを実際に作ってみよう

---

## TODO: 作例紹介(実演も交える)、頑張ってギミック作る...！！！

---

<!-- _class: titlecall -->
<!-- header: '**6. 絵画ギミックを実際に作ってみよう**' -->

1. Dissolve ってなに？
2. Dissolveでの消失エフェクトについて
3. Stencil ってなに？
4. Stencilでのマスク表現について
5. 組み合わせるとどうなる？
# 6. 絵画ギミックを実際に作ってみよう

---

## 絵画ギミックの作り方
- 額縁をStencil(Writer)兼Dissolve(座標)のルートボーンにする
- アバターのマテリアルをコピーしてRefの違うReaderとReader(反転)を作りアバターに付ける
- ReaderにDissolve(座標:線)で額縁の前側の時だけ表示するように(+Z)する
- Reader(反転)にDissolve(座標:線)で額縁の後ろ側の時だけ表示するように(-Z)する
- 額縁のON/OFFとワールド固定のメニューを作る
### <span class="added">→長い！難しい！</span>

---

<!-- _class: bg added -->

![bg right](https://placehold.jp/32/444444/bfffbf/720x1280.png?text=スライドのQRコード.png)

### 授業内じゃ時間が足りないので...<br>授業外で見れるようにスライド公開します！

みんなスクショしてー！

[スライドのURL](https://example.com)

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=額縁をStencil(Writer)兼Dissolve(座標)のルートボーンにする時の動作.gif)

### 額縁をStencil(Writer)兼Dissolve(座標)のルートボーンにする
- Stencil(Writer)は額縁越しに見たときにRefの値を変えるモノ
- Dissolve(座標)のルートボーン設定は額縁の位置を基準に溶けるようにするためのモノ

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=アバターのマテリアルをコピーしてRefの違うReaderとReader(反転)を作りアバターに付ける.gif)

### アバターのマテリアルをコピーしてRefの違うReaderとReader(反転)を作りアバターに付ける
- Reader(反転)は額縁の内側でだけ見えるマテリアル、絵画ギミックの根幹
- Readerは本来Alwaysでも絵画ギミックは成立するのだが、機能は変わらずに応用で大活躍してくれるのでReaderで作る

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=ReaderにDissolve(座標:線)で額縁の前側の時だけ表示するように(+Z)する.gif)

### ReaderにDissolve(座標:線)で額縁の前側の時だけ表示するように(+Z)する

- Readerが額縁の外側でだけ見えるように額の内側をDissolveで消す
- Dissolveは描画モードがカットアウトか半透明でしか使えないので描画モードを変える

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=Reader(反転)にDissolve(座標:線)で額縁の後ろ側の時だけ表示するように(-Z)する.gif)

### Reader(反転)にDissolve(座標:線)で額縁の後ろ側の時だけ表示するように(-Z)する
- Reader(反転)が額縁の内側でだけ見えるように額の外側をDissolveで消す
- Dissolveは描画モードがカットアウトか半透明でしか使えないので描画モードを変える

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=額縁のON/OFFとワールド固定のメニューを作る.gif)

### 額縁のON/OFFとワールド固定のメニューを作る
- MA Object Toggleで額縁のON/OFF
- 額縁事態にMA World FixedをつけてMA Object ToggleとParent Constraintでワールド固定

---

<!-- _class: bg -->

![bg right](https://placehold.jp/32/444444/ffffff/720x1280.png?text=動作確認(GestureManager).gif)

### 動作確認(GestureManager)
アバターや額縁を動かしたり、メニューからON/OFFやワールド固定を試してみよう

**全部が正常に動いたら...**

---

<!-- _class: titlecall -->
## 絵画ギミック完成！おめでとう！！！

---

<!-- header: '' -->

## 振り返り
- <span class="removed">Dissolve / Stencil は「可視性に条件を設定するモノ」</span>
- Dissolve は「条件を満たした部分を(溶かしたように)見えなくするモノ」
- Stencil は「条件を満たした部分を(型紙のように)切り抜くモノ」

---

## 参考資料
- <span class="removed">[Example](https://example.com)</span>
- <span class="added">liltoon ステンシル設定 <br> (https://lilxyzw.github.io/lilToon/ja_JP/advanced/stencil.html)</span>
- <span class="added">liltoon Dissolve <br> (https://lilxyzw.github.io/lilToon/ja_JP/advanced/dissolve.html)</span>

---

<!-- _class: titlecall -->
## ご清聴ありがとうございました
