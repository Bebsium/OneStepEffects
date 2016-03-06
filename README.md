OneStepEffects
=============

１クリックで綺麗なエフェクトやライティングを設定してくれるUnityエディタ拡張です。

=============

__準備__

1. このプロジェクトを適当なところに展開して、Unityで開く
1. [KinoObscurance](https://github.com/keijiro/KinoObscurance/) をzipでダウンロードして、「KinoObscurance.unitypackage」を Assets にドラッグアンドドロップして Import する。
1. [KinoBloom](https://github.com/keijiro/KinoBloom/) をzipでダウンロードして、「KinoBloom.unitypackage」を Assets にドラッグアンドドロップして Import する。
1. Asset Store で [Shader Calibration Scene](http://u3d.as/aiF) をダウンロードして Import する。(この際、「Bloom.cs」と「BloomEditor.cs」は除外しておく。上記 KinoBloom と名前が衝突してしまうため)


__実行__

1. 好きな3Dオブジェクトをシーンに配置する。（[3D Warehouse SketchUp](https://3dwarehouse.sketchup.com) がおすすめ）
1. Window -> One Step Effects を選択すると、One Step Effects設定ウィンドウが表示される。
1. 何も設定に変更なければ「Apply」を押す。
1. ライトマップの焼き付けが終われば出来上がり。

__詳細__

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
- Precomputed Realtime GI の設定で Build する
