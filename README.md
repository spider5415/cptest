# cptest

# 概要
競技プログラミングのコードテストを支援するコマンドラインツールです。
具体的には以下のことが出来ます。
- コンテストサイト上に掲載されている sample テストケースをダウンロード＆テストできる。
  - とりあえず AtCoder と Codeforces を対応予定。
- sample テストケースとして自作のテストケースを追加できる。
  - sample の正当性は自分で確認してください。
  - extreme なケースを sample に追加するのも検討。
- naive なアルゴリズムで確実に正しい出力をするコードを用いて提出用コードをテストできる。
  - 十分小さなケースでテストを行うが、入力の生成方法が課題。
    - 入力のテンプレートファイルを与える方法が現実的。
    - 入力形式を解析しても結局制約は手打ちのため自動生成は予定していない。
  - 最小ケースや準最小ケースあたりの生成もする予定。
- 普通のランダムケース(answer 不明)でテストして、時間を測定する。
  - answer が不明なので、基本的に時間の測定のみを行う。
  - random case と extreme なケースを生成して行う。
  - runtime error もある程度検出できるようにしたい。
    - こちらは C++ に限定すれば何とか実装できなくもなさそうです。
- interactive な問題に対するテストも行えるようにしたい。
  - 隠された配列などのリソースを入力として与えてクエリに返答するようなプログラムが必要。
  - C/C++ なら Go から呼べるけど他の言語は stand alone な返答コードを書いてもらう必要がある。
  - それでも多分 interactive をテストできるというだけでそこそこの利点があると思う。
