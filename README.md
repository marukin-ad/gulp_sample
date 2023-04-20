# gulpサンプル

gulpとは<br>
https://ics.media/entry/3290/{:target="_blank"}

## 導入方法

1.Node.jsをダウンロード、インストール。推奨版で大丈夫です。<br>
https://nodejs.org/ja{:target="_blank"}

2.Vscodeをダウンロード、インストール。<br>
Dreamweaverでも使えますが、その場合はターミナルを使うことになります。<br>
https://code.visualstudio.com/download{:target="_blank"}

3.Vscodeの日本語化
Vscodeのプラグインを使用し日本語化できます。<br>
https://wp-load.in/html-css/vscode-plugin{:target="_blank"}<br>
プラグインの導入方法はここにわかりやすく載っているので参考にして見てください。<br>
日本語以外にも便利なプラグインが載っているのでインストールしてもいいと思いますが、Live Serverというものはgulpに似たような機能が含まれているため不要です。<br>
これ以外にも色々便利なプラグインがあるので探してみて自分なりにカスタマイズしてみてください。

4.このページからgulpファイルをダウンロード
ページ上部に行き、Codeを書かれた緑のボタンをクリックし、Download Zipでダウンロード。
![9030a1f31639895ba70fe3de22f435d2](https://user-images.githubusercontent.com/117270549/233002360-539e1d3a-66c9-441d-8696-d59a36a1e35f.png)

5.ファイルを解凍し、解凍したフォルダをVscodeで開く

6.Vscodeの上部にあるターミナル→新規ターミナルをクリックするとターミナルが開くので、"npm install"と入力し、エンター（コピペで大丈夫です）
*Sublime textでターミナルを開く方法<br>
![https://nelog.jp/sublime-text-terminal-package](https://nelog.jp/sublime-text-terminal-package)
https://nelog.jp/sublime-text-terminal-package{:target="_blank"}

7.インストールが終わったら、同じように"npm run dev"と入力し、エンター

8.ブラウザでテストサイトが開けば完了です。


## gulpの使い方
* "npm run dev"コマンドを使うことで、ローカル環境でHTMLやCSSを変更した場合に即座に反映されるURLが生成されます。
* 生成されたURLをブラウザで開くことで、デザインビューのような確認が可能で、また同じネットワーク上であればスマートフォンでも確認できます。
* SSIインクルードも確認可能です。
* コーディングに関しては通常と同じ方法を使用できます。

### 画像の格納方法
画像を格納する場合は、一旦slice_imgフォルダ内に格納して下さい。<br>
例：index > img > kv.jpgとしたい場合は、slice_img > index > img > kv.jpgに格納してください。

### 他のサイトに流用する場合
他のサイトでもgulpを使いたい場合は、最初から新しく作る場合なら今回DLしたZIPファイルをもとに進めてもらえばいいですが、既存サイトにgulpを入れたいという場合は、"gulpfile.js"と"package.json"と".csscomb.json"だけをコピーすれば大丈夫です。<br>
導入したいサイトのルート直下に先程の3ファイルを配置し、ターミナルから"npm install"を実行すれば大丈夫です。（ディレクトリ構造によってはエラーが出る可能性もあるので、その場合は報告してもらえれば修正します。）