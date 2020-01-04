# DB設計
## users テーブル
|column   |type    |options  |
|-------  |--------|---------|
|name     |string  |null: false  |
|email    |string  |null: false  |
association
has_many groups , has_many message , has_many group_users 


## groups テーブル
|column   |type    |options  |
|-------  |--------|---------|
|name     |string  |null: false  |
association
has_many users , has_many group_users , has_many message

## message テーブル
|column   |type    |options  |
|body     |text    |         |
|image    |string  |         |
|group_id |integer |null: false, foreign_key: true |
|user_id  |integer |null: false, foreign_key: true |
association
belongs_to group_id , belongs_to user_id

## group_users テーブル
|group_id |integer |null: false, foreign_key: true |
|user_id  |integer |null: false, foreign_key: true |
association
belongs_to group_id , belongs_to user_id