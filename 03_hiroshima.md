- 第3回は [第18回 中国地方DB勉強会 in 広島](http://connpass.com/event/40880/edit//)

----

# MySQLで知りたいこと
- MySQLとMySQLクローン（MariaとかPerconaとか）の住み分けについて
- MySQL 8について
 - 再帰クエリの実用性
 - グラフモデルで実用可能なのか
 - 目玉機能について
- Xプロトコルってまだ息してるの？
- トランザクション分離レベルでRC使わないの？
 - RCを使わない理由
 - PostgreSQLはRCで困ってないし、むしろWebならRCで良いんじゃね？
- ロックみたいなパフォーマンスを監視するツール作りたいけど何見ればいいの？

# PostgreSQLで知りたいこと

- MySQLでは [PMP](https://www.percona.com/software/mysql-tools/percona-monitoring-plugins) が流行ってそうだし、他にもいくつかリソースの可視化ツールありますけど、PostgreSQLで有名なものってありますか？
- InnoDBのダブルライト的なものってあるの？
- XAトランザクションって対応してるの？
- 暗黙の型変換ってあるの？
- いつフィーチャーフリーズされるの？
  - MySQLはRCになったタイミング…と言いたいところだけど！
- pgpool?
- DR:BDってお好きですか
  - ストリーミングレプリケーションよりまだ主流？
  - MySQLはいい加減廃れたんだろうか（RDS for MySQLを除く）
- MySQLといえばFacebook, Twitter, Google, Booking.comとかパワーユーザーとして(俺の中で)有名ですけど、PostgreSQLのパワーユーザーってみかか以外にどこかあります？
- セマンティックバージョニングだと思いますが、パッチバージョンってどれくらい上がるものですか？
  - MySQLで一番増えたのは 5.0.96
- PostgreSQLのドライバーやクライアントライブラリーで有名どころをいくつか教えてください。
- シェアードバッファってInnoDBバッファプールとは全然違う？
- [@sawada_masahito](https://twitter.com/sawada_masahiko) さんがたまにHAモジュールっぽいものを書いていますが、アレって実用されてたりするんでしょうか。
- RDS for PostgreSQLってどうなの？
  - 同Heroku
- 実際、バージョンアップって大変？
  - どんな手順でやるの？
  - レプリケーション環境の時はどんな手順？
- UberのアレってPostgreSQLおじさんとしてはどんな感想？
  - "MySQLはsushiとbeerが一緒だから…" くらいの感覚で合ってる？ :D
- DROP TABLEをロールバックって、その間に他のトランザクションが更新したやつはどうなるの？
  - もしかして: MySQLではそれをRENAME TABLEと呼びます？
  - カラム追加も気になる
- キミは衝撃の `SELECT *, GROUP_CONCAT(..) FROM .. WHERE .. GROUP BY ..` を見たことがあるか！
