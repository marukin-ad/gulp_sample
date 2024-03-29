# gulp サンプル

gulp とは<br>
https://ics.media/entry/3290/

## 導入方法

1.Node.js をダウンロード、インストール。推奨版で大丈夫です。<br>
https://nodejs.org/

2.Vscode をダウンロード、インストール。<br>
Dreamweaver でも使えますが、その場合はターミナルを使うことになります。<br>
https://code.visualstudio.com/download

3.Vscode の日本語化
Vscode のプラグインを使用し日本語化できます。<br>
https://wp-load.in/html-css/vscode-plugin<br>
プラグインの導入方法はここにわかりやすく載っているので参考にして見てください。<br>
日本語以外にも便利なプラグインが載っているのでインストールしてもいいと思いますが、Live Server というものは gulp に似たような機能が含まれているため不要です。<br>
これ以外にも色々便利なプラグインがあるので探してみて自分なりにカスタマイズしてみてください。

4.このページから gulp ファイルをダウンロード
ページ上部に行き、Code を書かれた緑のボタンをクリックし、Download Zip でダウンロード。
![9030a1f31639895ba70fe3de22f435d2](https://user-images.githubusercontent.com/117270549/233002360-539e1d3a-66c9-441d-8696-d59a36a1e35f.png)

5.ファイルを解凍し、解凍したフォルダを Vscode で開く

6.Vscode の上部にあるターミナル → 新規ターミナルをクリックするとターミナルが開くので、`npm install`と入力し、エンター（コピペで大丈夫です）<br>
\*Sublime text でターミナルを開く方法<br>
https://nelog.jp/sublime-text-terminal-package

7.インストールが終わったら、同じように`npm run dev`と入力し、エンター

8.ブラウザでテストサイトが開けば完了です。

## gulp の使い方

- `npm run dev`コマンドを使うことで、ローカル環境で HTML や CSS を変更した場合に即座に反映される URL が生成されます。
- 生成された URL をブラウザで開くことで、デザインビューのような確認が可能で、また同じネットワーク上であればスマートフォンでも確認できます。
- SSI インクルードも確認可能です。
- コーディングに関しては通常と同じ方法を使用できます。
- gulp を止める時はターミナル上で Control + C です。

### 画像の格納方法

画像を格納する場合は、一旦 slice_img フォルダ内に格納して下さい。<br>
例：index > img > kv.jpg としたい場合は、slice_img > index > img > kv.jpg に格納してください。<br>
slice_img に格納すると、slice_img 以下のフォルダ構造と同じ状態で圧縮された画像が自動で生成されます。

### 他のサイトに流用する場合

他のサイトでも gulp を使いたい場合は、最初から新しく作る場合なら今回 DL した ZIP ファイルをもとに進めてもらえばいいですが、既存サイトに gulp を入れたいという場合は、"gulpfile.js"と"package.json"と".csscomb.json"だけをコピーすれば大丈夫です。<br>
導入したいサイトのルート直下に先程の 3 ファイルを配置し、ターミナルから`npm install`を実行すれば大丈夫です。（ディレクトリ構造によってはエラーが出る可能性もあるので、その場合は報告してもらえれば修正します。）

## 注意点

開発のみに必要なファイルが多いため、以下のファイルは納品時には除外してください<br>

- node_modules フォルダ（容量が重く時間もかかるので、テストサイトなどにもアップしないほうがいいです）
- slice_img フォルダ
- gulpfile.js
- package.json
- package-lock.json
- README.md
- .csscomb.json
- .gitignore
- common > css > base フォルダ
- その他各.scss ファイル、及び.map ファイル

.gitignore と README.md に関しては作業にも必要ないので、解凍した段階で削除してしまっても問題ありません。

### 今回のテンプレで使用している common 内の CSS について

こちらも新しくテンプレートを作って効率化を図ろうとしている段階なので、こちらについても何か意見があればお願いします。（カスタムプロパティという聞き慣れないものが使われているのでわかりにくいかも知れません…）
