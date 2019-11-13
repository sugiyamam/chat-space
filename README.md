# ChatSpace DB設計

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|
### Association
- has_many :messages
- has_many :group, thruogh:  :has_many :user_group


## groupテーブル
|Column|Type|Options|
|------|----|-------|
|group|string|null: false|
|addition|string|||
|username|string|null: false|
### Association
- has_many :user, through:  :has_many :user_group

## messageテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|text|||
### Association
- belongs_to :username

## users_groupテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- has_many :users
- has_many :groups