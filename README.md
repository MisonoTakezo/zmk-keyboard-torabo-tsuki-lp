[torabo-tsuki LP](https://github.com/sekigon-gonnoc/torabo-tsuki-lp)用のZMKファームウェア

- `_central`がついているuf2をトラックボールがついている方に、`_peripheral`を反対側に書き込んでください
- キーマップは[keymap-editor](https://nickcoutsos.github.io/keymap-editor/)で編集できます

## キーマップ

![keymap](keymap.svg)

> SVGは [keymap-drawer](https://github.com/caksoylar/keymap-drawer) で生成:
> `keymap parse -z config/keymap.keymap -c 10 -o keymap.yaml && keymap draw -j config/info.json keymap.yaml -o keymap.svg`

---

## フォーク元からの変更点

このリポジトリは[オリジナルのtorabo-tsuki LPファームウェア](https://github.com/sekigon-gonnoc/torabo-tsuki-lp)をフォークし、以下の変更を行っています。

### 機能面の変更

#### トラックボール機能

| 機能                   | 説明                                                          |
| ---------------------- | ------------------------------------------------------------- |
| **スクロールモード**   | レイヤー5有効時にトラックボールがスクロールモードに切り替わる |
| **スクロール速度調整** | X軸、Y軸1:8スケーリングで滑らかなスクロール操作を実現         |

#### キーマップ

[zmk-config-roBa](https://github.com/MisonoTakezo/zmk-config-roBa)のキーマップを移植（8レイヤー構成）

### レイアウト面の変更

| 項目       | オリジナル | 変更後            |
| ---------- | ---------- | ----------------- |
| **キー数** | 61キー     | 42キー（Sサイズ） |
| **行数**   | 5行        | 4行               |

keymap-editor用のレイアウト定義（`config/info.json`）も42キーのコンパクトレイアウトに対応するよう更新しました。
