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

### loadingScreen

課金アイテム読み込み中や購入処理中にユーザーが他の画面ボタンをタップしないようにするためのスクリーンです。
![図](https://i.gyazo.com/94b0bd7b8afb6e1d7b349cbe4657c561.png "図")<br>
<br>
![図](https://i.gyazo.com/172aebdb7f63a0e38136a5d4a0eef5ab.png "図")<br>
<br>
QitzAdIAPSystem/Prefab/LoadingScreen.prefab<br>
が対象のプリファブになります。<br>
こちらをシーンに配置後に先ほどのインスペクターに設定します。<br>
<br>
![図](https://i.gyazo.com/140de1db7388b2c19e00a9cc5abf07ad.png "図")<br>


### AdIAPConfirmDialog

![図](https://i.gyazo.com/07a98ae4e6c9b085e07347fe2662de1e.png "図")<br>
<br>
QitzAdIAPSystem/Prefab/AdIAPConfirmDialog.prefab<br>
<br>
　こちらのプリファブをIAPDisplayのインスペクターに設定します。<br>
 <br>
![図](https://i.gyazo.com/4535a6a711cd5f8660cafa8efbfff0c1.png "図")<br>

### DialogParent

AdIAPConfirmDialogをインスタンス化させたあとの親になるTransformを指定します。

##ざっくり設定したところで使い方

###ゲーム内通貨の取得

```C#

      var iapDataStore = AdIAPSaveDataFactory.Create();
      var money = iapDataStore.Money;

```
こんな感じで通貨を取得できます。

##他にも色々APIがあるのですが、また次回詳しく記載！














