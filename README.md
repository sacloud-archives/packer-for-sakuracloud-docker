:warning: **[sacloud/packer-plugin-sakuracloud](https://github.com/sacloud/packer-plugin-sakuracloud)へ移行されました**

# Packer for さくらのクラウド

[Packer for さくらのクラウド](https://github.com/sacloud/packer-builder-sakuracloud)用Dockerイメージ

## 使い方

### 起動コマンド書式

```bash
docker run -it --rm sacloud/packer [packerサブコマンド] [packerオプション]
```

`WORKDIR`は`/work`になっています。
テンプレートjsonファイルを指定する場合、以下のように実行します。

### 実行例(カレントディレクトリのexample.jsonを指定してビルド)
```bash
docker run -it --rm \
       -e SAKURACLOUD_ACCESS_TOKEN \
       -e SAKURACLOUD_ACCESS_TOKEN_SECRET \
       -v $PWD:/work \
       sacloud/packer build example.json
```
