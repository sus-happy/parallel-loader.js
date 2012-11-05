# parallel-loader.js

JavaScript非同期ローダー（のテスト）

## 概要

バラバラのJavaScriptいっぱい読み込むときに、最近のモダンブラウザは「async」属性を使えばバックグラウンドで読んでくれるそうなのですが、そうでない環境では非同期通信を使って読むと早くなる、とかいう記事を見かけたことがあったので作ってみました。

## 使い方

parallel-loader.jsを読み込むscriptタグ内に、配列で読み込みたいJSファイルのパスを記述します。
読み込みは一斉に行いますが、実行は読み込んだ順番に行います。

下記の様に記述すると、example01.js -> example02.jsの順番で実行します。

    <script type="text/javascript" src="path/to/parallel-loader.js">['path/to/example01.js', 'path/to/example02.js']</script>

## デモ

* [デモ（何もなしなHTML記述）](http://demo.sus-happy.net/javascript/prloader/normal.html)
* [デモ（deferなHTML記述）](http://demo.sus-happy.net/javascript/prloader/defer.html)
* [デモ（asyncなHTML記述）](http://demo.sus-happy.net/javascript/prloader/async.html)
* [デモ（非同期ローダーを利用）](http://demo.sus-happy.net/javascript/prloader/)

## 注意

JavaScriptの非同期ローダーを作って実験をしたかっただけなので、ほとんどテストをおこなっていないません。
そのため、実務で使うことはオススメしません。