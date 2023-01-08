# テーブル設計

## users テーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| name               | string | null: false |
| email              | string | null: false |
| encrypted_password | string | null: false |
| profile            | text   | null: false |
| occupation         | text   | null: false |
| position           | text   | null: false |

## prototype テーブル

| Column             | Type       | Options                  |
| ------------------ | -----------| ------------------------ |
| title              | string     | null: false              |
| catch_copy         | text       | null: false              |
| concept            | text       | null: false              |
| user               | references | null: false, foreign_key |

## comments テーブル

| Column             | Type       | Options                  |
| ------------------ | -----------| ------------------------ |
| content            | text       | null: false              |
| prototype          | reference  | null: false, foreign_key |
| user               | reference  | null: false, foreign_key |