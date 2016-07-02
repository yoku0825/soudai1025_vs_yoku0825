# MySQLで知りたいこと
- MySQLとMySQLクローン（MariaとかPerconaとか）の住み分けについて
  - MariaDB 10で入ったと噂のWindow関数については質問します
  - PerconaとかMariaDBを敢えて選ぶシーンのついて質問します
- 実際クローン製品全般どうなの？
  - 今後積極的にクローン製品を選ぶべきなのかMySQLとともに歩む方が正解か？
- マテビューマジ欲しいんだけど代替案ってトリガーとかCREATE TABLE bar (m INT) SELECT n FROM foo;？
- MySQLで分析とかしたい時のコツ
  - サブクエリは中間テーブルに分割したほうがいいよとかそういう感じ
  - EXCEPTが無いの地味にきつい（テストとかSQLチューニング後のデータの確認の時とか）けど欲しい関数ってありますか？
```
SELECT FORM target_table EXCEPT SELECT FROM test_table
-- とかは
SELECT target_table.id
  FROM target_table
  LEFT JOIN test_table
         ON test_table.id = target_table.id
         AND target_table.id IS NULL
 -- で代用するよ的なやつ
```
- 最近MySQLはXプロトコルとかJSONプラグインとかよりNOSQLっぽい方向性に向いてる気がするけど？
- Xプロトコルの可能性（ORMの代用品になるの？）
- マルチマスターレプリケーション(Percona XtraDB Clusterしか知らないんですけど、しかも使ったことはないんですけど)ってどうなの？
  - MySQLでも実現可能なの？
  - 要はRAC相当の冗長性が担保できる上にHA_Proxyとか使うと負荷分散出来て最強っぽいけど？
- 今、CloudでのRDB（RDSとか）全盛感あるけどMySQLのDBAとして生き残るには？
  - 単純な運用はRDSがサポートするからAWSエンジニアとの住み分けが必要だよね
　  - オンプレを使うメリットのある会社に行くべきなのか？
    - オンプレのメリットってなんだろう？
    - 最近はRDSにない機能はNOSQLのAWSサービスに委譲しようみたいな空気がアプリケーションサイドはある
  - DBAのポジションって田舎にはない

とりあえずここまで。


# PostgreSQLで知りたいこと

- **NLJ以外のJOIN** ってよく聞きますけど、具体的にどんなのがあってNLJと比べてどんなメリットとデメリット(NLJより上手くいくケース、NLJの方が良いケース)があるのです？
- Btree以外のインデックスってどんなものがあるですか？ それぞれBtreeと比べたメリットとデメリットが知りたいです。
  - ginインデックスってどういう仕組み？
- MySQLでは [PMP](https://www.percona.com/software/mysql-tools/percona-monitoring-plugins) が流行ってそうだし、他にもいくつかリソースの可視化ツールありますけど、PostgreSQLで有名なものってありますか？
- そーだいさんがよくdisってる pgAdmin(でしたっけ？) のデモをしてください :)
- PostgreSQLのバグってどこに報告するの？
- InnoDBのダブルライト的なものってあるの？
- XAトランザクションって対応してるの？
- 関数インデックスが昔からありますが、みんなサクサクとカジュアルに貼りまくるもの？
- みかかが死んだら死ぬの？
- 暗黙の型変換ってあるの？
