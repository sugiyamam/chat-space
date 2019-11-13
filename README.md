# ChatSpace DB設計

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|
### Association
- has_many :masseges
- has many :groups


## gruopテーブル
|Column|Type|Options|
|------|----|-------|
|group|string|null: false|
|addition|string|null: false|
|username|string|null: false|
### Association
- has_many :groups
- has_many :addition

## messageテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|text||
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