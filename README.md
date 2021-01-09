# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

# テーブル設計

## users テーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| email      | string | null: false |
| password   | string | null: false |
| name       | string | null: false |
| profile    | text   | null: false |
| occupation | text   | null: false |
| position   | text   | null: false |

### Association

- has_many :prototypes
- has_many :comments


## prototypes テーブル

| Column     | Type       | Options     |
| ---------- | ---------- | ----------- |
| prototypes | string     | null: false |
| catch_copy | text       | null: false |
| concept    | text       | null: false |
| image      |
| user       | references |

### Association

- belongs_to :comment
- belongs_to :user


## comments テーブル

| Column    | Type       | Options     |
| --------- | ---------- | ----------- |
| text      | text       | null: false |
| user      | references | null: false |
| prototype | references | null: false |

### Association

- belongs_to :user