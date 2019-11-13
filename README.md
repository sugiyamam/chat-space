<<<<<<< HEAD
<<<<<<< HEAD
=======
>>>>>>> f44954dc918ba6788a3c51db92e07b2a960b613f
# ChatSpace DB設計

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|username|string|null: false|

### Association
- has_many :messages
- has_many :groups, thruogh: :users_groups


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|groupname|string|null: false|
### Association
- has_many :users, through: :users_groups

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|text|||
### Association
- belongs_to :user
- belongs_to :group

## users_groupテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- belongs_to :group




=======
# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
