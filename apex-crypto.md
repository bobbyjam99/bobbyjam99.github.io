# Apex Crypto クラス

* A markdown unordered list which will be replaced with the ToC, excluding the "Contents header" from above
{:toc}

### 署名検証
Apexで検証を行うためのメソッド。

* `verify(String algorithmName, Blob data, Blob signature, Blob publicKey)` : 指定した公開鍵と検証
* `verify(String algorithmName, Blob data, Blob signature, String certDevName)` : [証明書と鍵の管理] に登録した証明書と検証
* `verifyHMac(String algorithmName, Blob input, Blob privateKey, Blob macToVerify)` : HMAC署名の検証

#### JWTの署名検証
JWTのトークンは `[ヘッダー].[ペイロード].[署名]` の形式になっている。

`[ヘッダー].[ペイロード]` をHS256アルゴリズムとシークレットキーのよって署名化された値が `[署名]` と比較して一致しているかで署名の検証を行う。

## Resources
* [Apex開発者ガイド : Cryptoクラス](https://developer.salesforce.com/docs/atlas.ja-jp.apexcode.meta/apexcode/apex_classes_restful_crypto.htm)
* [Apex開発者ガイド : データのセキュリティ保護](https://developer.salesforce.com/docs/atlas.ja-jp.apexcode.meta/apexcode/apex_crypto.htm)
* [JSON Web Tokenによる認証](https://tech-lab.sios.jp/archives/7576)
* [Using the Crypto.verify() method to verify a JWT signature](https://salesforce.stackexchange.com/questions/273742/using-the-crypto-verify-method-to-verify-a-jwt-signature)
