## [GitHub] Markdownでスライド資料作成

---


### 会社の先輩がmarkdownからスライド作成していたので・・・
---

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

