# アプリ概要
LifeColor
-> 日頃どのような行動をして1日を過ごしているかを習慣ごとに色付けして記録することで、直感的に自分の生活パターンを把握できる生活管理アプリです。

日頃の行動を　仕事(学校) / 自己研鑽 / 遊び&趣味 / 浪費　の4つに分け、時間を入力することで1日の中での行動の割合を色合いでグラフィカルに表示・管理します。
1週間や一ヶ月の記録を振り返った時に、色合いの変化で自分の行動パターンの変化を瞬時に把握することができます。

# URL
※ 未実装

# GitHub
https://github.com/Fukuda57/LifeColor

# 制作背景
自分の生活を習慣ごとに管理している中で、長いスパンで考えた時に数値だけの記録では習慣の把握がし辛いと感じたため、それらを色合いでグラフィカルに表現してくれるアプリケーションがあれば直感で自分の生活を捉えやすいと考えて実装を決めました。

# 使用技術
- HTML(HAML) / SCSS
- Javascript
- jQuery
- Ruby 2.6.5
- Rails 6.0.3.4


# usersテーブル


|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string|null: false|
|password|string|null: false|

Association

- has_many: relationships
- has_many: records

# relationshipテーブル

|Column|Type|Options|
|------|---|--------|
|user_id|references|null: false, foreign_key: true|
|follow_id|references|null: false, foreign_key: {to_table: :users }|

Association

- belongs_to: user

# recordsテーブル

|Column|Type|Options|
|-----|----|--------|
|work_time|?|null: false|
|self_time|?|null: false|
|play_time|?|null: false|
|waste_time|?|null: false|
|date|?|null: false|
|user_id|references|null: false, foreign_key: true|

Association

- belongs_to: user