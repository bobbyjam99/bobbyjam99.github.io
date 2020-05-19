# VS CodeでApexを匿名実行する
実装する前に組織に接続している必要あり。

![組織に接続している]({{ site.url }}/assets/images/connect-org.png)

**ファイル全体を実行**
* `scripts/apex/filename.apex` を作成
* `Ctrl + Shift + P` を押して `sfdx: Execute Anonymous Apex with editor content` を選択
* OUTPUTタブに実行結果が出力
  * コンパイルしたApexは `.sfdx/tools/tempApex.input` に出力

**ファイルの一部分のみ実行**
* `scripts/apex/filename.apex` を作成
  * 作成しなくてもOK
* `Ctrl + Shift + P` を押して `sfdx: Execute Anonymous Apex with Currently selected text` を選択
* OUTPUTタブに実行結果が出力
  * コンパイルしたApexは `.sfdx/tools/tempApex.input` に出力

