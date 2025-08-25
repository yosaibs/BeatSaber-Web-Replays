# Beat Saber Web Replays(I will provide the English explanation later.)

 - こちらは [Beat Saver Web Replays](https://github.com/BeatLeader/BeatSaber-Web-Replays) の改造版です。自動スピード変更機能（ミスの周辺とそれ以外で再生スピードを変える）が追加されています。 **公式に本機能相当の機能が実装(2025/8/18)されたためこちらの開発は中止します。**
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
 - ブラウザで[localhost:9999](http://localhost:9999)にアクセスすると改造版 Beat Saver Web Replays が利用できます。（上記コマンドを打つと、ローカルサーバーが起動し、既定のブラウザでlocalhost:9999が開きます。）
   - 本家と同様に以下の手段でリプレイを表示できます。
     - url 末尾に scoreId をつけて開く
     - 画面をクリックした後開かれるファイル選択画面で、bsor 形式のファイルを選択する。（bsorファイルは {Beat Saberが置いてある場所}\UserData\BeatLeader\Replays 以下に置いてあります。 ）
     - bsor 形式のファイルをドラッグアンドドロップする
 - ちなみに netlify コマンドを打ったコマンドプロンプト上でCtrl-Cを押すか、コマンドプロンプトを閉じるとローカルサーバーが終了します

## 設定
 
 - Playback の設定の末尾に改造版の設定項目があります。変更した設定は本家同様にブラウザに保存されます。
 - <img width="847" height="744" alt="image" src="https://github.com/user-attachments/assets/d369b659-e01a-46ca-887d-65f02eb3b95b" />

   - Auto Speed Controls: 自動スピード変更機能のオンオフ。デフォルトオン
   - Speed normal: ミスが近くにない時の再生速度。デフォルト1。範囲は(0,2]。
   - Speed slow: ミスが近くにある時の再生速度。デフォルト0.2。範囲は(0,1]。
   - Offset seconds for slow-mode-beginning: ミスしたノーツのどのくらい前から再生スピードがスローに変化するかの値。デフォルト-0.3。単位は秒。マイナス方向に行けば行くほどスローになるのが早くなる。範囲は[-1,1]。
   - Offset sedonds for slow-mode-ending: ミスしたノーツのどのくらいあとから再生スピードがノーマルに戻るかの値。デフォルト0。単位は秒。プラス方向に行けば行くほどノーマルに戻るのが遅くなる。範囲は[-1,1]。

--------------------

# Beat Saber Web Replays (translated by copilot)

- This is a modified version of [Beat Saver Web Replays](https://github.com/BeatLeader/BeatSaber-Web-Replays). It features an automatic speed adjustment function (the playback speed changes depending on whether you are near a miss or not).
- **Since an official feature equivalent to this functionality was implemented on August 18, 2025, development of this project will be discontinued.**
- By default, the automatic speed adjustment is turned on. You can toggle it on/off and configure its settings in the Playback settings.
- Use at your own risk. We may not be able to respond to inquiries.

## Confirmed Working Environments
- OS: Windows
- Browsers: Chrome/Firefox

## Prerequisites

- Install [nodejs](https://nodejs.org/en/)
- Clone the master branch of this repository to your local machine
- Move to the top-level folder of the cloned repository in the command prompt, then run the following command:
```
npm install
```
- Install Netlify CLI globally by running the following command anywhere in the command prompt:
```
npm install netlify-cli -g
```

## Usage

- In the command prompt, move to the top-level folder of the cloned repository and run:
```
netlify dev
```
- Access [localhost:9999](http://localhost:9999) in your browser to use the modified Beat Saver Web Replays. (Running the above command will start a local server.)
  - As with the original, you can view replays by the following methods:
    - Open a URL with the scoreId appended to the end
    - After clicking the screen, select a file in the bsor format from the file selection dialog that appears (bsor files are located at {Where Beat Saber is installed}\UserData\BeatLeader\Replays)
    - Drag and drop a bsor file
- Note: The local server will stop if you press Ctrl-C in the command prompt running the netlify command or if you close the command prompt window.

## Settings

- Additional settings for the modified version are available at the end of the Playback settings. Changed settings are saved in your browser, just like the original.
- <img width="847" height="744" alt="image" src="https://github.com/user-attachments/assets/d369b659-e01a-46ca-887d-65f02eb3b95b" />

  - Auto Speed Controls: Toggle automatic speed adjustment. On by default.
  - Speed normal: Playback speed when not near a miss. Default is 1. Range is (0,2].
  - Speed slow: Playback speed when near a miss. Default is 0.2. Range is (0,1].
  - Offset seconds for slow-mode-beginning: How many seconds before a missed note the slow speed should start. Default is -0.3. Unit is seconds. Negative values mean it starts before the miss.
  - Offset seconds for slow-mode-ending: How many seconds after a missed note the speed returns to normal. Default is 0. Unit is seconds. Positive values mean it ends after the miss.
