# ユースケース図(Use Case Diagram)

![Use Case Diagram](/figs/0106_use_case_diagram.png)
## テキスト
アクター: オープンキャンパス参加者
  - イベントガイドの読み取り
  - ランドマーク探索
  - 写真撮影とアップロード
  - 解説テキスト表示
  - スコアリング

アクター: 運営スタッフ
  - 活動履歴の表示
  - スコア確認と特典付与

アクター: オペレータ端末
  - 写真解析
  - アクティビティログ

## PlantUML
```
@startuml
actor "オープンキャンパス参加者" as Participant
actor "運営スタッフ" as Staff
actor "オペレータ端末" as Operator

usecase "イベントガイドの読み取り" as UC1
usecase "ランドマーク探索" as UC2
usecase "写真撮影とアップロード" as UC3
usecase "写真解析" as UC4
usecase "解説テキスト表示" as UC5
usecase "スコアリング" as UC6
usecase "アクティビティログ" as UC7
usecase "活動履歴の表示" as UC8
usecase "スコア確認と特典付与" as UC9

Participant --> UC1
Participant --> UC2
Participant --> UC3
Participant --> UC5
Participant --> UC6

Operator --> UC4
Operator --> UC7

Staff --> UC8
Staff --> UC9

UC3 --> UC4 : includes
UC4 --> UC5 : includes
UC5 --> UC6 : includes
@enduml
```

## ユースケース図の説明
1. オープンキャンパス参加者
  - イベントガイドの読み取り: QRコードを読み取り、アプリを起動する。
  - ランドマーク探索: キャンパス内のランドマークを探索する。
  - 写真撮影とアップロード: ランドマークの写真を撮影し、アプリにアップロードする。
  - 解説テキスト表示: アップロードした写真の解析結果として表示される解説テキストを読む。
  - スコアリング: 写真の解析結果に基づいてスコアを取得する。

2. 運営スタッフ
  - 活動履歴の表示: 参加者の活動履歴を表示する。
  - スコア確認と特典付与: 参加者のスコアを確認し、特典を付与する。

3. オペレータ端末
  - 写真解析: アップロードされた写真を解析する。
  - アクティビティログ: 参加者の活動履歴をログとして保存する。

これにより、こんこんプロジェクトのシステムとユーザーの関係を視覚的に把握することができます