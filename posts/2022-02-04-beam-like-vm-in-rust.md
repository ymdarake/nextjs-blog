---
title: "Rustで作るBEAMライクなLanguage VM - 2"
date: "2022-02-04"
---

引き続き、BEAM-like VM in Rustをしていく。

今日は [Part 02](https://blog.subnetzero.io/post/building-language-vm-part-02/)。


VMにプログラムとプログラムカウンタを持たせて、ループして処理していく。

この辺は後でどんどん最適化？していくらしい。


プログラムの中身用に別途オペコードをenumで定義する。

ちなみにレジスターが32bit、そのうちオペコードが8bitの設計。（これは [Part01](https://blog.subnetzero.io/post/building-language-vm-part-01/) で話があった）

VMが入力のプログラム(いまはただの`Vec<u8>`)をループしてOpcodeを一つずつ処理するように書いて、

テストを書いて今日のところはお開き。


Part02にしてプログラム(とテスト)の骨格が出来てきていい感じ。


**おまけ**

ブログの筆者がテストを逐一書いていくスタイルなので、
それならばということでGitHub Actionsを追加して、
[Codecov](https://about.codecov.io/)でRustのテストカバレッジを測定できるようにした。


[CodecovのBotがPRにレポートしてくる設定](https://github.com/apps/codecov)も追加。


今回のコードはこちら。
[https://github.com/ymdarake/iridium/pull/2](https://github.com/ymdarake/iridium/pull/2)


次回に続く。
