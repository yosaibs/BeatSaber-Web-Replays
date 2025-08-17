# Beat Saber Web Replays

 - こちらは [Beat Saver Web Replays](https://github.com/BeatLeader/BeatSaber-Web-Replays) の改造版です。自動スピード変更機能（ミスの周辺とそれ以外で再生スピードを変える）が追加されています。
 - デフォルトでは自動スピード変更機能はオンになっており、設定の Playback からオン/オフ切り替えと各種設定ができます。
 - ご利用は自己責任でお願いします。お問い合わせには返答できない場合があります。

## 動作環境(確認できたもの)
 - OS: Windows
 - ブラウザ: Chrome/Firefox

## 事前準備

 - [nodejs](https://nodejs.org/en/) をインストールする
 - 本リポジトリの master をローカルに落とす
 - コマンドプロンプト上でローカルに落としてきたフォルダの最上階層に移動し、以下のコマンドを打つ
```
npm install
```
 - コマンドプロンプトで任意の場所で以下のコマンドを打つ
```
npm install netlify-cli -g
```

## 使い方

 - コマンドプロンプト上でローカルに落としてきたフォルダの最上階層に移動し、以下のコマンドを打つ
```
netlify dev
```
 - ブラウザで[localhost:9999](http://localhost:9999)にアクセスすると改造版 Beat Saver Web Replays が利用できます。（上記コマンドを打つと既定のブラウザでlocalhost:9999が開きます。）
   - 本家と同様に以下の手段でリプレイを表示できます。
     - url 末尾に scoreId をつけて開く
     - 画面をクリックした後開かれるファイル選択画面で、bsor 形式のファイルを選択する。（bsorファイルは {Beat Saberが置いてある場所}\UserData\BeatLeader\Replays 以下に置いてあります。 ）
     - bsor 形式のファイルをドラッグアンドドロップする
 - ちなみに netlify コマンドを打ったコマンドプロンプト上でCtrl-Cを押すとローカルサーバーが終了します

## 設定
 
 - Playback の設定の末尾に改造版の設定項目があります。変更した設定は本家同様にブラウザに保存されます。
 - <img width="847" height="744" alt="image" src="https://github.com/user-attachments/assets/d369b659-e01a-46ca-887d-65f02eb3b95b" />

   - Auto Speed Controls: 自動スピード変更機能のオンオフ。デフォルトオン
   - Speed normal: ミスが近くにない時の再生速度。デフォルト1。範囲は(0,2]。
   - Speed slow: ミスが近くにある時の再生速度。デフォルト0.2。範囲は(0,1]。
   - Offset seconds for slow-mode-beginning: ミスしたノーツのどのくらい前から再生スピードがスローに変化するかの値。デフォルト-0.3。単位は秒。マイナス方向に行けば行くほどスローになるのが早くなる。範囲は[-1,1]。
   - Offset sedonds for slow-mode-ending: ミスしたノーツのどのくらいあとから再生スピードがノーマルに戻るかの値。デフォルト0。単位は秒。プラス方向に行けば行くほどノーマルに戻るのが遅くなる。範囲は[-1,1]。
   
