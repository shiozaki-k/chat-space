# DB設計
## users テーブル
|column   |type    |options  |
|-------  |--------|---------|
|name     |string  |null: false  |
|email    |string  |null: false  |



## groups テーブル
|column   |type    |options  |
|-------  |--------|---------|
|name     |string  |null: false  |

## message テーブル
|column   |type    |options  |
|body     |text    |         |
|image    |string  |         |
|group_id |integer |null: false, foreign_key: true |
|user_id  |integer |null: false, foreign_key: true |

## group_users テーブル
|group_id |integer |null: false, foreign_key: true |
|user_id  |integer |null: false, foreign_key: true |