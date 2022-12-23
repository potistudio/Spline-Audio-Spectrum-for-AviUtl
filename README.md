# AE_Audio-Spectrum
A Script for AviUtl that Draw an Audio Spectrum Like After Effects.

# AE_AudioSpectrum
AviUtlで音声波形を描画するスクリプトです。<br>
FFTを使用しているので、[After Effects](https://www.adobe.com/jp/products/aftereffects.html)の音声波形と同じ形状、動きの波形ができます。

## 要件
[Rikky Module](https://hazumurhythm.com/wev/amazon/?script=NRMv2q9Q&keyword=rikky_module&search_price=&sort=viewh&filter=all&page=1)を導入している必要があります。

## ファイル内容
  - **Screenshots**<br>
    このスクリプトで描画された音声波形の画像です。
    ご参考に

  - **AE_AudioSpectrum.obj**<br>
	スクリプト本体です。

  - **README.md**<br>
	Markdown形式のREADMEです。

  - **LICENSE**<br>
	このスクリプトのライセンスについて書かれています。

## 導入方法
  - 自分のAviUtlにrikky_moduleが導入されているかを確認します。
  - 同梱のREADMEを読んで、使い方、注意事項を確認します。
  - AE_AudioSpectrum.objをAviUtlのscriptフォルダにコピーします。
  - AviUtlを開いて、動作確認をします。

## 設定項目
  - **トラックバー**<br>
	- 開始位置<br>
	  波形の開始位置 (左端) の位置 (X) を指定します。

	- 終了位置<br>
	  波形の終了位置 (右端) の位置 (X) を指定します。

	- 周波数帯<br>
	  波形の線の量を指定します。

	- 高さ<br>
	  波形の高さを指定します。

  - **ダイアログ**<br>
	- 色<br>
	  波形の色を設定します。

	- 開始周波数 (0 ~ )<br>
	  計算をする周波数帯の開始周波数を設定します。

	- 終了周波数 (0 ~ )<br>
	  終了周波数を設定します。

	- サンプルレベル (0, 1, 2, 3)<br>
	  スペクトラムを計算する際のサンプルレベルを設定します。<br>
	  低い値を設定すると、時間軸は細かくなりますが、分割数は荒くなります。<br>
	  高い値を設定すると、分割数は細かくなりますが、時間軸は荒くなります。<br>
    
 - AUDIOデゥレーション<br>
    複数フレームの波形を取得し、それらを平均化します。
    要するに、動きがより滑らかになります
    代わりに、負荷が高くなります。

	- AUDIOオフセット<br>
	  取得するスペクトラムのフレームオフセットを設定します。<br>
	  -1を設定すると、1フレーム前の波形を取得します。<br>
	  1を設定すると、1フレーム後の波形を取得します。<br>
	  同様に、-2だと2フレーム前、2だと2フレーム後を取得します。<br>

	- 太さ (0 ~ )<br>
	  波形の太さを設定します。

	- ディスプレイオプション (0, 1, 2)<br>
	  描画する波形の種類を設定します。<br>
	  - 0 = 先端が丸い波形
	  - 1 = 先端が平らな波形
	  - 2 = 点のみの波形

	- サイドオプション (0, 1, 2)<br>
	  波形を描画する方向を設定します。
	  - 0 = 上下両方向
	  - 1 = 上方向のみ
	  - 2 = 下方向のみ

 - 丸くする
   波形を極座標変換のように、丸くして描画します。
   外側に行くほど線が太くなり、内側に行くほど細く描画されます。
   
 - 半径
    丸くした場合の半径を設定します

## ライセンス
GNU General Public License v2.0<br>
詳しくは同梱のLICENSEをご覧ください。
