---
layout: default
title: EC-CUBE3のバージョン違いによる動作
---

# {{ page.title }}

EC-CUBE3.0.8までとEC-CUBE3.0.9以上からプラグイン機構(プラグインの実装)が変わっており、古いバージョンもサポートされていますがサポートするEC-CUBEのバージョンにより対応するイベントが異なります。また本体側でサポートされた機能も存在します。

イベントについては[イベント](event)で詳しく解説しますが、EC-CUBEのバージョンによって動作方法で以下の違いがあります。

#### EC-CUBE3.0.8まで
リクエストやレスポンスに対してのみイベントがあり、プラグインからはそのイベントに対してのみ処理を差し込み可能です。


#### EC-CUBE3.0.9から
新たなイベントを新規追加、フックポイントの新規追加、コントローラーやtwigファイル単位でのイベントを追加等々機能が大幅に改善され、  
プラグインから本体に対して処理を介在する箇所が増えています。


#### EC-CUBE3.0.11から
トランザクション管理が本体側でサポートされ、それに伴いプラグイン側も考慮する必要があります。  
詳しくは、 [EC-CUBE 3.0.11 変更内容に伴うプラグインへの影響](/guideline/plugin-update-for3.0.11){:target="_blank"} を参照してください。

#### EC-CUBE3.0.12から
本体側にログ機能が用意され、プラグインからログを簡単に出力する事ができるようになりました。
詳しくは、 [EC-CUBE3でのログ設定](/log){:target="_blank"} を参照してください。


### プラグインをどの本体のどのバージョンまでサポートするか
この記事を執筆時点でEC-CUBE3.0.9がリリースされてから半年以上経過しており今後新しくプラグインを作成する場合、EC-CUBE3.0.9以上のみを対象に先ずは作成しましょう。  
その後、3.0.8以下でもプラグインを対応して欲しいという要望が出た時点で対応すればいいでしょう。