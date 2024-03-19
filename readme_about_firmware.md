# ファームウェアについての覚書

m.ki設計の自作キーボードについて、MCUボードへファームウェアをインストールする手順について説明します。
<br>
ここでは、主にQMK_Firmwareについて説明します。
<br>

## pro microの場合

### 最初に
m.ki設計のpro micro使用の自作キーボードは、初期の作品になります。この頃の作品は、Remapによって、比較的に容易にキーマップ編集ができるので、Remapに登録されているものが多いです。
<br>
ここでいうRemapとは、旧Remapになります。一部、新Remapに対応させたものもあります。しかし、新Remapに対応させると同時に、vialにも対応させていることが多くあります。
<br>
m.kの日常使う環境で、Remapが不安定な挙動をすることがあり、現在、Remapからの脱却を図っています。
<br>

### インストールの手順

QMK Toolboxを入手し、PCにインストールしてください。
<br>
次にm.ki設計の自作キーボードhexファイルを、関係するgithubのfirmwareの中から見つけて下さい。見つけたら、自分のPC上にダウンロードしておいて下さい。
<br>
PCとpro microをUSBケーブルで繋いで下さい。
<br>
QMK Toolboxを立ち上げて下さい。
<br>




## RP2040系MCUボードの場合

2021年秋頃より、m.kiはRaspberry pi picoやRP2040-ZeroのRP2040系MCUボードを使用したcool836pico、cool836rp 、cool640を設計した。当初は、QMK_firmwareに対応していなかった為、PRK_firmwareでファームウェアを作成した。その後、対応してから設計した自作キーボードはQMK_firmwareでファームウェアを作成している


