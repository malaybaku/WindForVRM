# WindForVRM

* 獏星(ばくすたー)
* 2019/11/09

Sample repository to introduce wind effect for VRM.

VRMの揺れモノに風っぽいエフェクトを入れるための作例です。

![example](./gif/example.gif)

## 手元の検証環境

以下の組み合わせで動作確認しています。

* Unity 2018.3.7f1
* UniVRM v0.53.0
* ニコニ立体ちゃん(Alicia)

## 導入手順

* 手元のプロジェクトに、[UniVRM](https://github.com/vrm-c/UniVRM)のReleasesからパッケージを導入します。
* このレポジトリのReleasesからUnityPackageをダウンロードしてインポートします。
    - UnityPackageの内容は、このレポジトリの`WindForVrm/Assets/WindForVrm/`以下と同じです。
* あらかじめシーン上にロードしたVRMや、`prefab`化されたVRMに風エフェクトを適用する場合、`VRMWind`コンポーネントをVRMに割り当てます。
* 動的にVRMをロードする場合、シーンの他の場所に`VRMWind`コンポーネントがアタッチされたオブジェクトを配置しておいて、VRMのロード時点で`LoadVrm(Transform vrmRoot)`を呼び出します。
