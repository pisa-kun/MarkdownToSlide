## [GitHub] Markdownでスライド資料作成


### 会社の先輩がmarkdownからスライド作成していたので・・・

練習も兼ねてMarkdown(.md)でスライド資料を作成する方法を調査してみる。

- 利点
     - ソースコードを簡単に記述できる
     ```c#
     <!-- SampleCode -->
        public class Hoge()
        {
            private static readonly int _hogeCounter = 0; // Field Number
            public Hoge() => Console.WriteLine("Constructor!"); //Constuctor
            public void HugeWrite(string str) => Console.WriteLine($"{str} : is printed"); // public Method
        }

     ```
     - Markdown記述なのでGitで差分を見やすい
     - 表も簡単に書ける(はず)


### Remark × Markdown

[@natsumoさんの記事](https://qiita.com/natsumo/items/717e40de2c43824624b6)参考

| | |
|--|--|
|Remark|Githubを使用してMarkdownでスライドを作成するツール|
|Markdown|文書記述言語。最近流行している|

Githubにcommitすることで、スライドとして公開することが可能。

ローカルだと上手く表示できなかったので別の方法がいいのかも。

### スライド作成法
---
1. 「index.html」と「sample.md」ファイルを作成する

- #### index.html は名前固定だそうです
```javascript
//index.html
  <script type="text/javascript">
    // sample.md
    var slideshow = remark.create({sourceUrl: "sample.md"});
  </script>
```
一応ソースコード解説
- remark.create メソッドのsourceUrlのkeyにファイル名を渡す。今回はsample.md

「sample.md」は下記リンク先を一応参考に

[https://raw.githubusercontent.com/natsumo/SampleSlide/master/sample.md](https://raw.githubusercontent.com/natsumo/SampleSlide/master/sample.md)

2. GitHubにプロジェクトを作成してコミット & プッシュ

任意のプロジェクト名でGithubにプロジェクトを作成後、先ほど作成したhtmlとmdファイルをコミット & プッシュ。

3. masterブランチと別個で「gh-pages」ブランチを作成

- #### ここ、つまりポイント
- gh-pagesブランチにマークダウンファイルが公開されると、[environment]が表示される

![pic1](https://github.com/pisa-kun/MarkdownToSlide/blob/gh-pages/img/pic1.png)

メモ : readme.mdに添付する画像はgitの適当なブランチに画像投げて参照するのがいいみたい。

- [environment] から [view deployment]をクリックでMarkdownのスライドが閲覧できる

![pic2](https://github.com/pisa-kun/MarkdownToSlide/blob/gh-pages/img/pic2.png)

- タイトル

![pic3](https://github.com/pisa-kun/MarkdownToSlide/blob/gh-pages/img/pic3.png)

- 目次

![pic4](https://github.com/pisa-kun/MarkdownToSlide/blob/gh-pages/img/pic4.png)

あとはsample.mdのコードを見ながらスライド作成するだけですね。

---
### 参考
[@harasouさん](https://qiita.com/harasou/items/1fa3cca6ac1ef175c876)

[readmeにのせる画像](http://cakecatz.hatenadiary.com/entry/2015/02/10/214942)