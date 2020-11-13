# 管理アプリ

# 概要
- アカウト管理で、皿、資材、食材の管理ができる。
# URL

# テストアカウント

# 利用方法
- 使用者はアカウントを作成。
- 購入した皿、資材、食材を登録
- 使用もしくは破損した数を登録

# 課題解決
- コラボカフェでの営業では、皿、資材、食材が常に変わる。その為管理がかなり難しいと考えられる。
- 皿は約1月で大きく変わる為、会社でどんな皿を所持できているか把握が困難担っていく。その為、特徴での検索をできる必要がある。
- 資材は店舗管理になっている為、ロスが出やすい、その為ロスの計算をしないでいいように退勤時に各自が記述できるようにすれば作業の削減を可能にできる。
- 食材は各コラボで変わることが多いので、まだ使える食材の管理をする必要がある。
- 食材の消費期限が近づくと通知がいくことが必要である。

# 要件定義
- 誰が登録したかを明確にする必要がある。
- 皿、資材、食材の3つの管理が必要である

# 実装した機能についてのGIFと説明

# 実装予定の機能
- 皿、資材、食材の登録/一覧/詳細/削除機能
- ユーザー登録機能
- 検索機能
- 1部ユーザーにしか使えないようにする。

# データベース設計
-/Users/daikiyamada/newapp/understand/ER.dio
# ローカルでの動作方法


# userテーブル
| Column           | Type    | Option     |
|------------------|---------|------------|
| name             | string  | null:false |

# itemテーブル
| Column           | Type      | Option                         |
|----------------- | ---------- |------------------------------ |
| user             | references | null:false, foreign_key: true |
| name             | string     | null:false                    |
| feature          | string     | null:false                    |
| Remarks          | string     |                               |
