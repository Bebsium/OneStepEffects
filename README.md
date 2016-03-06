OneStepEffects

=============

１クリックで綺麗なエフェクトやライティングを設定してくれるUnityエディタ拡張です。

=============

*準備*

1. [KinoObscurance](https://github.com/keijiro/KinoObscurance/) をzipでダウンロードして、「KinoObscurance.unitypackage」を Assets にドラッグアンドドロップして Import する。
1. [KinoBloom](https://github.com/keijiro/KinoBloom/) をzipでダウンロードして、「KinoBloom.unitypackage」を Assets にドラッグアンドドロップして Import する。
1. Asset Store で [Shader Calibration Scene](http://u3d.as/aiF) をダウンロードして Import する。

*実行*

1. Window -> One Step Effects を選択すると、One Step Effects設定ウィンドウが表示される。
1. 何も設定に変更なければ「Apply」を押す。
1. ライトマップの焼き付けが終われば出来上がり。

*詳細*

やっていることは以下の通り

- シーン内の全マテリアル（Root Objectが設定されている場合はそれ以下の全マテリアル）を調べてStandard Shader でNormal mapが張っていない場合、自動的にコピーして(_Nmlとファイル名の最後に付く)、Normal map として設定する。
- シーン内の全てのオブジェクトを Static にする。（Root Objectが設定されている場合はそれ以下の全オブジェクト）
- カメラをHDRオン、Deferred Shadingにする
- プロジェクトの中に Skybox があれば、設定する
- カメラに AntiAliasing エフェクトをつける
- カメラに Kino Bloom エフェクトをつける
- カメラに Screen Space Reflection エフェクトをつける
- カメラに Kino Obscurance エフェクトをつける
- ライトマップ設定をちょうどいい感じにする
- ライトマップを焼く
