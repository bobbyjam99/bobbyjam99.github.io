# Lightningアクション

Lightning

Lightningアクションに関するインターフェース。
* `lightning:actionOverride`: 標準アクションの上書き
* `lightning:availableForFlowActions`: フローアクション
* `force:lightningQuickAction`: クイックアクション(キャンセルボタンなどあり)
* `force:lightningQuickActionWithoutHeader`: クイックアクション(キャンセルボタンなどなし)

標準アクションでも「承認」「コピー」は上書きできない。
「コピー」はカスタムボタンで実現可能。

## Lightning Web Components (LWC) の利用
LWCではインターフェースを実装できない。そのためLWCを利用したい場合には、Aura Componentでラップする必要がある。

```
<aura:component implements="lightning:actionOverride, lightning:hasrecordId">
</aura:component>
```

## Resources

- [Standard Actions and Overrides Basics](https://developer.salesforce.com/docs/atlas.en-us.lightning.meta/lightning/components_using_lex_s1_action_overrides_basics.htm)
- [Build an Aura Component to Override a Standard Action](https://trailhead.salesforce.com/ja/content/learn/projects/workshop-override-standard-action)
- [Create Lightning Custom button to clone and edit the newly created record](https://help.salesforce.com/articleView?siteLang=ja&id=000322260&language=ja&type=1&mode=1)
