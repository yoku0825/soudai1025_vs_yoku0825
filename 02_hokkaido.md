- 第2回は [Database Night Hokkaido 2016 Summer](http://connpass.com/event/37402/)

----

# MySQLで知りたいこと
- MySQLとMySQLクローン（MariaとかPerconaとか）の住み分けについて
  - MariaDB 10で入ったと噂のWindow関数については質問します
  - PerconaとかMariaDBを敢えて選ぶシーンのついて質問します
- MySQLで分析とかしたい時のコツ
  - サブクエリは中間テーブルに分割したほうがいいよとかそういう感じ
- Xプロトコルの可能性（ORMの代用品になるの？）
- 今、CloudでのRDB（RDSとか）全盛感あるけどMySQLのDBAとして生き残るには？
  - 単純な運用はRDSがサポートするからAWSエンジニアとの住み分けが必要だよね
　  - オンプレを使うメリットのある会社に行くべきなのか？
    - オンプレのメリットってなんだろう？
    - 最近はRDSにない機能はNOSQLのAWSサービスに委譲しようみたいな空気がアプリケーションサイドはある
  - DBAのポジションって田舎にはない
- MySQLのローリングアップグレード

- RRがなぜデフォルトなのか
  - ネクストキーロックがくそ


# PostgreSQLで知りたいこと

- MySQLでは [PMP](https://www.percona.com/software/mysql-tools/percona-monitoring-plugins) が流行ってそうだし、他にもいくつかリソースの可視化ツールありますけど、PostgreSQLで有名なものってありますか？
- InnoDBのダブルライト的なものってあるの？
- XAトランザクションって対応してるの？
- 暗黙の型変換ってあるの？
- いつフィーチャーフリーズされるの？
- pgpool?
- DR:BDってお好きですか
  - ストリーミングレプリケーションよりまだ主流？
  - MySQLはいい加減廃れたんだろうか（RDS for MySQLを除く）
- MySQLといえばFacebook, Twitter, Google, Booking.comとかパワーユーザーとして(俺の中で)有名ですけど、PostgreSQLのパワーユーザーってみかか以外にどこかあります？
- セマンティックバージョニングだと思いますが、パッチバージョンってどれくらい上がるものですか？
  - MySQLで一番増えたのは 5.0.96
