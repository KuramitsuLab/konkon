# 業務フロー図(Workflow Diagram)
![Workflow Diagram](/figs/0108_workflow_diagram.png)

## PlantUML
```
@startuml
!define RECTANGLE class

RECTANGLE QRコード読み取り画面 as QRScan
RECTANGLE ホーム画面 as Home
RECTANGLE ランドマークリスト画面 as LandmarkList
RECTANGLE ランドマーク詳細画面 as LandmarkDetail
RECTANGLE 写真撮影画面 as PhotoCapture
RECTANGLE 写真アップロード画面 as PhotoUpload
RECTANGLE 解析結果画面 as AnalysisResult
RECTANGLE スコア表示画面 as ScoreDisplay
RECTANGLE 活動履歴画面 as ActivityLog
RECTANGLE 特典画面 as Rewards

QRScan --> Home : QRコードを読み取る
Home --> LandmarkList : ランドマークリストを表示
LandmarkList --> LandmarkDetail : ランドマーク詳細を表示
LandmarkDetail --> PhotoCapture : 写真を撮影
PhotoCapture --> PhotoUpload : 写真をアップロード
PhotoUpload --> AnalysisResult : 解析結果を表示
AnalysisResult --> ScoreDisplay : スコアを表示
ScoreDisplay --> ActivityLog : 活動履歴を表示
ActivityLog --> Rewards : 特典を表示
@enduml
```

## 業務フロー図の説明
1. イベントガイドとマップの配布
    - 運営スタッフ: イベントの開始時に参加者にイベントガイドとマップを配布し、QRコードの使い方を説明します。
2. QRコード読み取り
    - 参加者: イベントガイドに記載されたQRコードを読み取ります。
3. ランドマーク探索
    - 参加者: キャンパス内のランドマークを探索し、指定されたランドマークを訪れます。
4. 写真撮影とアップロード
    - 参加者: ランドマークの写真を撮影し、アプリを通じてアップロードします。
5. 写真解析とスコアリング
    - システム: アップロードされた写真を解析し、解説テキストとスコアを生成します。
6. 活動履歴の確認
    - 参加者: アプリで自身の活動履歴を確認します。
7. 特典付与
    - 運営スタッフ: 参加者の活動履歴とスコアを確認し、特典を付与します。
    
これにより、こんこんプロジェクトの全体的な業務フローと各ステークホルダーの役割を視覚的に把握することができます。