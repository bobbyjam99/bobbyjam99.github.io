# 逆引き sfdx command

## [project コマンド](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference_force_project.htm#cli_reference_create)

### Salesforce DX プロジェクトを作成する

```console
$ sfdx force:project:create -n newproject
```

## [apex コマンド](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference_force_apex.htm)

### Apex クラス作成

```console
$ sfdx force:apex:class:create -n myclass
```
* デフォルトではカレントディレクトリに作成。指定する場合は `-d` を使用。

### Trigger クラス作成

```console
$ sfdx force:apex:trigger:create -n mytrigger -s Account -e 'before insert, after insert' -d <app-dir>/main/default/triggers
```

## source コマンド

### リリース

#### すべての Apex クラスをリリース

```console
$ sfdx force:source:deploy -m ApexClass
```

#### 特定の Apex クラスをリリース

```console
$ sfdx force:source:deploy -m ApexClass:MyApexClass
```

#### ディレクトリ内のソースファイルをリリース

```console
$ sfdx force:source:deploy -p path/to/source
```

#### マニフェストにリストされたすべてのコンポーネントをリリース

```console
$ sfdx force:source:deploy -x path/to/package.xml
```

```console
$ sfdx force:source:push -u me@my.org
```

## data コマンド

```console
$ sfdx force:data:tree:import --sobjecttreefiles <インポートファイル>
```

## [org コマンド](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference_force_org.htm)

### 組織管理

#### 組織の一覧を表示する
```
sfdx force:org:list
```

#### スクラッチ組織を作成する
```
sfdx force:org:create -f config/project-scratch-def.json -a MyScratchOrg -v myhuborg
```

#### 組織を削除する

```
sfdx force:org:delete -u me@my.org
```

## [設定関連(configコマンド)](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference_force_config.htm#cli_reference_force_config)

### 設定を一覧取得する???

```
sfdx force:config -u me@my.org
```

### 設定を取得する

```
sfdx force:config:get defaultusername
```

### 設定を設定する

```console
$ sfdx force:config:set defaultusername=me@my.org defaultdevhubusername=me@myhub.org
```

#### Local Developmentサーバを起動

```console
$ sfdx force:lightning:lwc:start -u xxx
```
http://localshot:3333 にアクセス

デフォルトHUB組織設定
```console
$ sfdx force:config:set defaultdevhubusername=<devhubusername> --global
```

## [CLIの更新](https://developer.salesforce.com/docs/atlas.ja-jp.sfdx_setup.meta/sfdx_setup/sfdx_setup_update_cli.htm)

#### インストーラを使用して Salesforce CLI をインストールした場合

```console
$ sfdx update
```

```console
$ sfdx plugins:update
```

## [CLI バイナリまたはプラグインのアンインストール](https://developer.salesforce.com/docs/atlas.ja-jp.sfdx_setup.meta/sfdx_setup/sfdx_setup_uninstall.htm)

#### CLIバイナリのアンインストール

```console
$ sudo rm -rf /usr/local/sfdx
$ sudo rm -rf /usr/local/lib/sfdx
$ sudo rm -rf /usr/local/bin/sfdx
$ sudo rm -rf ~/.local/share/sfdx ~/.config/sfdx ~/.cache/sfdx
$ sudo rm -rf ~/Library/Caches/sfdx
```

#### プラグインのアンインストール

```console
$ sfdx plugins:uninstall plugin-name
```
