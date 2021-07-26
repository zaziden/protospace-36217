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

# テーブル設計

## users テーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| name               | string | null: false |
| email              | string | null: false |
| password           | string | null: false |
| profile            | text   | null: false |
| occupation         | text   | null: false |
| position           | text   | null: false |

## comments テーブル

| Column             | Type       | Options     |
| ------------------ | ---------- | ----------- |
| user               | references |             |
| prototype          | references |             |
| text               | text       | null: false |

## prototypes テーブル

| Column             | Type          | Options     |
| ------------------ | ------------- | ----------- |
| title              | string        | null: false |
| user               | references    |             |
| catch_copy         | text          | null: false |
| concept            | text          | null: false |
| image              | ActiveStorage |             |