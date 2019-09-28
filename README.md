# QitzADIAPSystemの使い方！

##依存プラグインのGoogleAdmobのプラグインパッケージを入れます！

https://github.com/googleads/googleads-mobile-unity/releases/tag/v4.0.0

##依存プラグインのUnityIAPを有効にします！

![図](https://i.gyazo.com/75271fdfb403ba3a4cc39e5905026b47.png "図")<br>
![図](https://i.gyazo.com/5bc3ec5c161d4c95b7d0ac0dc7f6d694.png "図")<br>

インポートボタン押下でインポートします。

##次にパッケージをインスコします！

https://github.com/QitzPub/QitzADIAPSystem/raw/master/QitzADIAPSystem.unitypackage

![図](https://i.gyazo.com/e6b8f5253f9af1b45e23253e93fce165.png "図")<br>

こんな感じでプロジェクトにQitzAdIAPSystemとQitzAdModuleが追加されます。

##GoogleAdmobの設定を行います。

![図](https://i.gyazo.com/822853ad77933f4394dce84441d2ef3e.png "図")<br>
QitzAdModule/Resources/QitzAdModule.prefab<br>
![図](https://i.gyazo.com/b4350d350a8f0cf9cbd865115c29d2a3.png "図")<br>

インスペクターに広告の各種ADIDを入れます。
※初期ではテスト用のIDが入っています。
※広告を使わない場合はここはスキップしてOKです

##課金モジュールの使い方

![図](https://i.gyazo.com/9d7d4a7d98355559b02dc16493680ac5.png "図")<br>

QitzAdIAPSystem/Prefab/IAPDisplay.prefab
が対象のプリファブになります。
シーンに配置すると以下のような形になります↓
![図](https://i.gyazo.com/223cd7ec88628a0500910ffd6e7170b9.png "図")<br>
このような形で課金購入のボタンなどを配置できます。

また、以下のような形でインスペクターを設定していきます。
![図](https://i.gyazo.com/362717776cacacab1ffafd91fda825c9.png "図")<br>

### productElements

ItunesConnectやGooglePlayConsoleで設定した課金アイテムのIDを入れるためのフィールドになります。<br>
![図](https://i.gyazo.com/2c3bf7ef1858bfed495ec045142b9cd5.png "図")<br>
![図](https://i.gyazo.com/6e04f8df0cc5ea33b3c2235b07763ec9.png "図")<br>
↓<br>
![図](https://i.gyazo.com/679211d141e279aa0a2caec2590e030c.png "図")<br>


















