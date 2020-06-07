## rushmini-server

### 前提

- (PersistentVolume にデータを保存する場合) StorageClass が `pv.storageClassName` に定義されている

### 設定項目

| 変数名                | 説明                                  | デフォルト値 | 必須                 |
| --------------------- | ------------------------------------- | ------------ | -------------------- |
| `hostname`            | RushHour アプリケーションのホスト名   | `localhost`  | ○                    |
| `pv.enabled`          | アプリのログ、DB Pod を PV に格納する | `false`      |                      |
| `pv.capacity`         | PV のサイズ                           | `10Gi`       | `pv.enabled`=`true`  |
| `pv.storageClassName` | PVC のストレージクラス名              |              | `pv.enabled`=`true`  |
| `tls.enabled`         | SSL 終端を Ingress で実現する         | `false`      |                      |
| `tls.cert`            | SSL 証明書                            |              | `tls.enabled`=`true` |
| `tls.key`             | SSL 証明書の秘密鍵                    |              | `tls.enabled`=`true` |
