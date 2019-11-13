<<<<<<< HEAD
# ChatSpace DB設計

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|username|string|null: false|
### Association
- has_many :messages
- has_many :group, thruogh:  :has_many :user_group


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|groupname|string|null: false|
### Association
- has_many :users, through:  :has_many :users_group

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|text|||
### Association
- belongs_to :users
- belongs_to :groups

## users_groupテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :users
- belongs_to :groups
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
>>>>>>> parent of 56d38f7... generated files by scaffold
