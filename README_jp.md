__本日本語訳は Google 翻訳を利用した暫定版であり、内容の正確性を保証しません。確実な情報は英語版の [README.md](https://github.com/Biacco42/Ergo42/blob/master/README.md) を参照してください！__

# Ergo42

**生命、宇宙、そして少なくともキーボードの究極の質問への答え**

7x4 ortholinear スプリットキーボード。

![Ergo42](https://raw.githubusercontent.com/Biacco42/Ergo42/readme/readme_image/ergo42_image.jpg)

_注意！バージョン 3.0.0 Towel 以降の Ergo42 は、バージョン 1 と 2 の両方のシリーズデザインと互換性がありません。バージョン 3 Towel シリーズではない Ergo42 を構築する場合は、1.x または 2.x ブランチを参照してください。_

# パーツ

 -  **2** PCB
 -  **2** 5V / 16MHz Pro Micro互換ボード
 -  **56** 1N4148（THD）または1N4148w（SMD）ダイオード
 -  **2** [MJ-4PP-9 TRRSジャック](http://akizukidenshi.com/catalog/g/gC-06070/)
 -  **2**ケースプレートセット（この Repo で利用可能なデザイン）
 -  **10** 5 mm（Cherry MX）/ 3 mm（Kailhロープロファイル）M2スタンドオフ
 -  **8** 15 mm高さM2スタンドオフ
 -  **36** 4〜6 mm M2ネジ（板厚に対応した高さ）
 -  **2** 2ピンタクトスイッチ
 -  **56** [選択したスイッチ](https://mechanicalkeyboards.com/shop/index.php?l=product_list&c=107)
 -  **1** TRRS / TRSケーブル

ネジはキーキャップに若干のクリアランスの問題があります。プロファイルの低い頭のネジを使用してください。

## ダイオードをマウントする

お互いに最も近い内部にTRRSジャックとしてPCBを配置します。

 -  **左のPCB** には TRRS ジャックが **右側にあります**
 -  **右のPCB** には TRRS ジャックが **左側にあります**

ダイオードをはんだ付けする側は、スイッチプレートの厚さとキースイッチタイプ（Cherry MX互換またはKailhロープロファイル）によって異なります。チェリーMX対応のアクリル板の厚さが3mm未満の場合は、キースイッチと同じ側にダイオードを配置する必要があります。 Kailhロープロファイルスイッチ付きのアクリルプレートには、キースイッチの反対側にダイオードが付いていなければなりません。

**あなたの作業を再確認してください。** 黒い線（THD）/白い線（SMD）は、正方形のパッドに面している必要があります。

![diodes_01](https://raw.githubusercontent.com/Biacco42/Ergo42/readme/readme_image/ergo42_rev2_diode_from_top.jpg)

## [オプション]抵抗とブリッジジャンパを取り付けます

UARTではなくI2Cを使用して他の側のPCBと通信する場合は、左側のPCBのR1およびR2プリントシルクに2.2 kオームの抵抗を追加する必要があります。また、各側のPCB上のはんだジャンパーによって短いW1パッドにブリッジします。通常、この手順を実行する必要はありません。

## TRRSジャックとタクトスイッチを取り付けます

TRRSジャックとタクトスイッチをスイッチと同じ側に取り付けてください。それは上面にあるべきです。

## Pro Microをマウントする

Ergo42のPCBは対称ですが、Pro Microマウントは左右のPCBで異なります。 _この仕様はバージョン2から変更されました。_

### プロマイクロピンヘッダー

Pro Microのコンポーネント側にピンヘッダーをハンダします。 __左側のものと右側のものは同じものです__

![はんだピンヘッダー](https://raw.githubusercontent.com/Biacco42/Ergo42/readme/readme_image/pro_micro_connector_through.jpg)

##### コンスルーを利用する場合

[コンスルー](http://www.mac8sdk.co.jp/mac8/parts/XXX/xb.html) を使用する場合は、PCB上ではなく、Pro Microボード上に半田付けする必要があります。

コンスルーには裏表と方向があります。推奨されるマウント方向があります。

![Through hole connector directions and sides](https://raw.githubusercontent.com/Biacco42/Ergo42/readme/readme_image/pro_micro_THC_sides.jpg)

上記の画像の方向を参照して、Pro Micro にコンスルーを取り付けてください。コンスルーを同じ方向に向けるように注意してください。両方の _コンスルーの穴_ を同時に見ることができます。下記の画像で同時にコンスルーの穴が見えていることを確認してください。

![Soldered pin header](https://raw.githubusercontent.com/Biacco42/Ergo42/readme/readme_image/pro_micro_connector_through.jpg)

### Pro Microを半田付け（または設定）

PCB上のPro Microを取り付ける面の白線に合わせて Pro Micro をハンダします(コンスルーを利用する場合は差し込むだけです)。

![はんだピンヘッダー](https://raw.githubusercontent.com/Biacco42/Ergo42/readme/readme_image/ergo42_rev3_pro_micro_mount_line1.jpg)

![はんだピンヘッダー](https://raw.githubusercontent.com/Biacco42/Ergo42/readme/readme_image/ergo42_rev3_pro_micro_mount_line2.jpg)

__Pro Micro側（はんだ付け側ではありません）の白い線を注意深く参照してください.__
以下の画像の青線で囲った場所が正しい位置となります。左右で取り付けるべき場所が違うので注意してください。 __以下の画像はスイッチを取り付ける面(上面)から見たもの__です。

![ProMicro取り付け位置](https://user-images.githubusercontent.com/732828/51353965-7d1ef000-1af5-11e9-808b-43a172dfa545.jpg)

## スイッチをマウントする

アクリル板にスイッチを取り付け、PCBをはめ込み、スイッチをハンダします。
**チェリーMX互換機をアクリルプレートの厚さ<3 mm、高さ5 mmのスタンドオフで使用する場合は、スイッチの電気端子の先端を切断してください。スイッチの電気端子が底板と干渉します。**

## ケースを組み立てる

スタンドオフ付きのネジを締めます。
一部の [ビニールパッド](https://www.amazon.co.jp/gp/product/B00V5MQWGS/ref=oh_aui_detailpage_o00_s00?ie=UTF8&psc=1) は、キーボードの安定性に役立ちます。
キーキャップを取り付けます。

バージョン 3 Towel からは、いくつかのテント/チルトレッグオプションがあります。安定性のために足をセットし、[シリコンテープ](https://amzn.to/2PkJYzK) を置くことができます。

## Flash QMKファームウェア

### Remapがホストするビルド済みファームウェアをフラッシュする場合

現在、RemapでVIA / Remapキーマップ編集に対応したビルド済みファームウェアをフラッシュすることができます。

https://remap-keys.app/catalog/unf8swoIgYlDVLGyN9H6

### ファームウェアを自作する場合

Ergo42用のQMKファームウェアは、[QMKファームウェア](https://github.com/qmk/qmk_firmware) で利用できるようになりました。
このドキュメントでは、QMKを構築する方法については説明しません。 [QMKドキュメント](https://docs.qmk.fm/) を参照してください。

USBケーブルでキーボードをPCに接続して実行する

```
$ make ergo42:default:avrdude
```

左右のキーボードで個別に操作します。

ファームウェアをビルドしてフラッシュしようとします。 Pro Microをリセットするために必要な指示に従ってください。

このプロセスには特権が必要な場合があります。 `Permission denied` エラーがある場合は、試してみてください。

```
$ sudo make ergo42:default:avrdude
```

## すべて完了！
