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
- [ ] ギミック
  - [x] 絵画ギミック (最優先！)
  - [x] Dissolve 基礎
  - [x] Stencil 基礎
  - [ ] 着替えギミック
  - [ ] 4次元ポケット
  - [ ] 目に髪がかかっても目が浮いて見える
  - [ ] 箱の中だけ別世界
  - [ ] 
- [ ] GIF
  - [x] Dissolve 基礎
  - [x] Stencil 基礎
  - [ ] 絵画ギミック
  - [ ] 着替えギミック
  - [ ] 4次元ポケット
  - [ ] 目に髪がかかっても目が浮いて見える
  - [ ] 箱の中だけ別世界
  - [ ] 絵画ギミックの作り方 (Unity)
==================================================
-->

<!-- _class: titlecall -->
# 出入りできる絵画ギミックを作ろう<br>(Dissolve / Stencil)

---

<!-- _class: bg -->

![bg right](images/Nekobox_Picture_01.png)

## 講師紹介
名前: ねこぼっくす
好きなもの: 紅茶と焼き菓子
最近ハマってること: Resonite

---

<!-- _class: changed -->

![bg width:100% right:30%](images/QRCode_Github_UniMagic-6_Slide.png)

## 講義にあたってのお願い

- 講師をShow Avatar (シフォンちゃんが見えたらOK)
- イヤーマフの解除 (テキストボックスの視認性向上)
- 講義資料を開く (QRコード/URL: <br>https://nekobox-dev.github.io/UniMagic-6_Slide/ )

講義進行のためご協力をお願いします！

(できた人は手を挙げるボタンで教えてください)

---

## この講義を受けるとうれしいこと

1. 衣装や小物の**出現**や**消失**を**リッチにする**方法が分かる
1. **見せたい所**と**見せたくない所**を**制御する術**を知れる
1. **遊び心**や**インパクト**がある**表現の仕組み**を学べる

---

## 本日の流れ

1. Dissolve ってなに？
2. Dissolveでの消失エフェクトについて
3. Stencil ってなに？
4. Stencilでのマスク表現について
5. 組み合わせるとどうなる？
6. 絵画ギミックを実際に作ってみよう

---

<!-- _class: titlecall -->
<!-- header: '**1. Dissolve ってなに？**' -->

# 1. Dissolve ってなに？
2. Dissolveでの消失エフェクトについて
3. Stencil ってなに？
4. Stencilでのマスク表現について
5. 組み合わせるとどうなる？
6. 絵画ギミックを実際に作ってみよう

---

<!-- _class: bg -->

![bg right vertical](https://placehold.jp/32/444444/ffffff/720x1280.png?text=お着替えギミックの動作.gif)
![bg](https://placehold.jp/32/444444/ffffff/720x1280.png?text=4次元ポケット.gif)

## <span>Dissolve</span> ってこんな感じ

---

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

## <span>Dissolve</span>のエフェクトの種類
- **座標**: ルートボーンや原点からの距離もしくは方向で溶ける部分を指定
- **透明度**: テクスチャの透明度で溶ける部分を指定
- **UV**: テクスチャの中心からの距離もしくは方向で溶ける部分を指定

---

<!-- _class: bg -->

![bg right](images/2_1_1_Dissolve_透明度.gif)

### <span>Dissolve(透明度)</span>の動作
テクスチャの透明度で溶ける部分を指定

---

<!-- _class: bg -->

![bg right](images/2_2_1_Dissolve_UV_点.gif)

### <span>Dissolve(UV:点)</span>の動作
テクスチャの中心からの距離もしくは方向で溶ける部分を指定

---

<!-- _class: bg -->

![bg right](images/2_2_2_Dissolve_UV_線.gif)

### <span>Dissolve(UV:線)</span>の動作
テクスチャの中心からの距離もしくは方向で溶ける部分を指定

---

<!-- _class: bg -->

![bg right](images/2_3_1_Dissolve_座標_点.gif)

### <span>Dissolve(座標:点)</span>の動作
ルートボーンや原点からの距離もしくは方向で溶ける部分を指定

---

<!-- _class: bg -->

![bg right](images/2_3_2_Dissolve_座標_線.gif)

### <span>Dissolve(座標:線)</span>の動作
ルートボーンや原点からの距離もしくは方向で溶ける部分を指定

---

<!-- _class: bg -->

![bg right](images/2_4_1_Dissolve_座標_線上下.gif)

### <span>Dissolve(座標:線の上下)</span>のマテリアルを2つ同時に入れた時の動作
何かが消えると同時に何かが現れるような表現ができる

---

<!-- _class: titlecall -->
<!-- header: '**3. Stencil ってなに？**' -->

1. Dissolve ってなに？
2. Dissolveでの消失エフェクトについて
# 3. Stencil ってなに？
4. Stencilでのマスク表現について
5. 組み合わせるとどうなる？
6. 絵画ギミックを実際に作ってみよう

---

<!-- _class: bg -->

![bg right vertical](https://placehold.jp/32/444444/ffffff/720x1280.png?text=目に髪がかかっても目が浮いて見える様子.gif)
![bg](https://placehold.jp/32/444444/ffffff/720x1280.png?text=箱の中だけ別世界の動作.gif)

## <span>Stencil</span>ってこんな感じ

---

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

## liltoonにおける<span>Stencil</span>のプリセット
- **Writer**: オブジェクトにRefの値を設定する
- **Reader**: Writer越しに見たときにRefの値が同じなら非表示 (NotEqual)
- **Reader(反転)**: Writer越しに見たときにRefの値が同じなら表示 (Equal)

---

## <span>Stencil</span>の主な条件式
- **Always**: Refの値を参照せず常に表示、liltoonのデフォルトはこれ
- **Equal**: 指定したRefと等しいオブジェクト越しに見たときだけ表示
- **NotEqual**: 指定したRefと等しいオブジェクト越しに見た時だけ非表示

---

<!-- _class: bg -->

![bg right](images/4_1_Stencil_Reader.gif)

### Readerの動作

Writer越しに見たときにRefの値が同じなら非表示 (NotEqual)

---

<!-- _class: bg -->

![bg right](images/4_2_Stencil_Reader反転.gif)

### Reader(反転)の動作

Writer越しに見たときにRefの値が同じなら表示 (Equal)

---

<!-- _class: bg -->

![bg right](images/4_3_Stencil_Reader+Reader反転.gif)

### ReaderとReader(反転)のマテリアルを2つ同時に入れた時の動作

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

<!-- _class: bg -->

![bg right](images/5_1_Dissolve+Stencil.gif)

## <span>Dissolve</span> と <span>Stencil</span> を<br>組み合わせたら

額縁をルートボーンとStencil(Writer)に設定すると...
**額縁の外と内で別々のモノが見える**ようになる！

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
### →長い！難しい！

---

## 絵画ギミックに挑戦したい人は

**ごめんなさい！** 授業内では時間が足りないので扱いません...
挑戦してみたい方は**授業後に公開される資料を参照**しながら作ってみてください！

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
- Dissolve は「条件を満たした部分を(溶かしたように)見えなくするモノ」
- Stencil は「条件を満たした部分を(型紙のように)切り抜くモノ」

---

## 参考資料
- liltoon Dissolve <br> (https://lilxyzw.github.io/lilToon/ja_JP/advanced/dissolve.html)
- liltoon ステンシル設定 <br> (https://lilxyzw.github.io/lilToon/ja_JP/advanced/stencil.html)

---

<!-- _class: titlecall -->
## ご清聴ありがとうございました
