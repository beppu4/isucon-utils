02_setup_server
---

# 概要

サーバーのパッケージやミドルウェアの設定ファイルのセットアップをおこないます。

# 使い方

## inventoryファイルの準備

まずは、inventoryに(既に記載済みの内容を参照し)、サーバー情報を記載してください。

## 通常実行

以下のコマンドを実行することで、各ロールのmain.ymlを実行します。

```
$ ansible-playbook -i inventory site.yml
```

## プレイブックを選択して実行

--tagsオプションと任意のタグを指定することで、実行するプレイブックを選択できます。
実行内容は、roles/<ロール名>/tasks/main.ymlを参照してください。

```
$ ansible-playbook -i inventory site.yml [--tags [common], [nginx], [mysql]]
```

