# TL Split Keyboard 16mm Rev0ビルドガイド

TL Split Keyboard 16mmは、TRONキーボード風のキーボードです。オリジナルのTRONキーボードの良さが分かりやすい、Mサイズ（16mmピッチ）で設計しています。

## 説明
TL Split Keyboard 16mmは、PCBが左右違います。4.7kΩ抵抗（R1,R2）がある方が左です。
基本的に、左側にUSBケーブルを接続するようにしています。

PCBには、表面と裏面があります。"TL Split Keyboard"と記載がある方が、表面です。

## 組み立て
### PCBへパーツ半田付け

- ダイオードを、左右PCB裏面に36カ所実装します。

ダイオードを、左右PCB裏面に実装します。ダイオードは極性があるので、カソード（黒い方）をシルク印刷で線が入っている方（かつKと書かれて、穴が四角の方）になるよう、左右それぞれ36カ所半田付けしていきます。

- 4.7kΩ抵抗を左側PCB表面に2カ所実装します。

4.7kΩ抵抗を、左側PCB表面のみに実装します。極性は無いので、どちらでもかまいません。

- リセットスイッチを、左右PCB裏面に実装します。

リセットスイッチを、左右PCB裏面に実装します。左右PCBそれぞれに1カ所ずつリセットスイッチ位置があるので、半田付けしてください。

※裏面にシルク印刷されています。

- TRRSジャックを、左右PCB裏面に実装します。

TRRSジャックを、左右PCB裏面に実装します。左右PCBに、それぞれ半田付けしてください。

※裏面にシルク印刷されています。

### Pro Microへコンスルー半田付け

遊舎工房で購入すれば、コンスルー付きが買えます。

PCBから外した状態で、部品（USBコネクタなど）が実装されている面にコンスルーを載せて、半田付けします。

できたら、左右PCBの裏面にはめ込みます。基板の外側（左側は左、右側は右）にUSBコネクタが来るようにはめます。

### CherryMX キースイッチ半田付け

アクリルのトッププレートとPCBの間にスペーサー(3mm)をはさみ、左右それぞれ4カ所ネジ止めします。ねじ頭が上側に来るようにして、PCBの下にはスペーサー(10mm)で止めてください。
キースイッチをアクリルトッププレートの上からアクリル・PCBにはめ込み、固定します。ここでキーが浮かないよう、しっかりトッププレートにはめ込んで、半田付けしてください。

CherryMXキースイッチは、親指扇形部分以外の64カ所半田付けします。

### Kailh Mid-Height キースイッチ半田付け

親指扇形部分は、間隔が狭いためKailh Mid-Height キースイッチを使用しています。CherryMXと高さが違うため、アクリルにははめ込まず、直接PCBに固定するようになります。

Kailh Mid-Height キースイッチは、親指扇形部分の8カ所半田付けします。

## ファームウェア書き込み
QMK Toolboxでhexファイルを書き込んでください。
[tlsplit18_default.hex](https://github.com/satromi/tlsplit18_rev0/blob/master/hex/tlsplit18_default.hex) をダウンロードして、QMK Toolboxで書き込みます。
左右それぞれ書き込みが必要です。

## 動作確認

左右のキーボードをTRRSケーブルで繋いだら、USBケーブルでPCと接続し、動作確認してください。
