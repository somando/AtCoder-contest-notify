# AtCoder-Contest-Notify

AtCoderコンテスト通知LINE Notify

## How to use

- Google Sheet

  ワークブック名は何でも構いませんが、シート名が「contest_data」というシートを予め用意します。

- Google App Script

  {データベース用Google Sheet ID} に作成したGoogle Sheet ID、<br>{通知先LINE Notifyトークン} に取得したLINE Notifyトークンを挿入します。

  そして、トリガーに以下の2つを設定します。

  - get_contest関数

    | 設定項目                   | 選択項目             | 
    | -------------------------- | -------------------- | 
    | イベントのソース           | 時間主導型           | 
    | 時間ベースのトリガータイプ | 日付ベースのタイマー | 
    | 時刻を選択                 | 午前4時～5時         | 

  - set_trigger関数
 
    | 設定項目                   | 選択項目             | 
    | -------------------------- | -------------------- | 
    | イベントのソース           | 時間主導型           | 
    | 時間ベースのトリガータイプ | 日付ベースのタイマー | 
    | 時刻を選択                 | 午前5時～6時         | 
