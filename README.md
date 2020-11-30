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