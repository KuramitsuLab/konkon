# 画面遷移図(Screen Transition Diagram)

Error

## テキスト
1. QRコード読み取り画面
    ↓
2. ホーム画面
    ↓
3. ランドマークリスト画面
    ↓
4. ランドマーク詳細画面
    ↓
5. 写真撮影画面
    ↓
6. 写真アップロード画面
    ↓
7. 解析結果画面
    ↓
8. スコア表示画面
    ↓
9. 活動履歴画面
    ↓
10. 特典画面

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

## 画面遷移図の説明
1. QRコード読み取り画面
    - ユーザーが最初にアクセスする画面。ここでイベントガイドのQRコードを読み取ります。
    - QRコード読み取り後、ホーム画面に遷移します。
2. ホーム画面
    - アプリのメイン画面で、ランドマークリストへのアクセスが可能。
    - 「ランドマークリスト」ボタンをタップしてランドマークリスト画面に遷移します。
3. ランドマークリスト画面
    - キャンパス内のランドマークのリストを表示します。
    - 特定のランドマークを選択してランドマーク詳細画面に遷移します。
4. ランドマーク詳細画面
    - 選択されたランドマークの詳細情報を表示します。
    - 「写真撮影」ボタンをタップして写真撮影画面に遷移します。
5. 写真撮影画面
    - ランドマークの写真を撮影します。
    - 撮影後、写真アップロード画面に遷移します。
6. 写真アップロード画面
    - 撮影した写真をアップロードします。
    - アップロード完了後、解析結果画面に遷移します。
7. 解析結果画面
    - アップロードされた写真の解析結果を表示します。
    - 解析結果に基づいて解説テキストとスコアを表示します。
    - 「スコア表示」ボタンをタップしてスコア表示画面に遷移します。
8. スコア表示画面
    - 解析結果に基づいたスコアを表示します。
    - 「活動履歴」ボタンをタップして活動履歴画面に遷移します。
9. 活動履歴画面
    - 参加者の活動履歴を表示します。
    - 「特典表示」ボタンをタップして特典画面に遷移します。
10. 特典画面
    - 参加者が獲得した特典を表示します。

これにより、こんこんプロジェクトのアプリ内での画面遷移を視覚的に把握することができます。