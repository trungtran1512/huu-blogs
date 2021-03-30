# /1/device/visits/walkin
## Visit/アポイント

#### 前提条件 : ログイン済（トークンが取得済）であること
> Deviceのトークン
- 例：{"name": "authentication", "value": "1ec2c40395ae4c04b7331ba813dc202e"}


#### 1. Create : [device/visits/walkin/create.yml](../1/admin_apis/device/visits/walkin/create.yml)

- リクエストを設定（登録項目）
```
  {
    "auto_gate": false,
    "label": "カスタム通話",
    "free_text": "フリーテキストフリーテキストフリーテキスト",
    "slack_type": "direct",
    "chatwork_type": "direct",
    "workplace_type": "direct",
    "hangouts_type": "direct",
    "line_works_type": "direct",
    "teams_type": "direct",
    "user_id": 1,
    "department_id": 1,
    "add_guest_count": 1,
    "users": [
      {
        "id": 19509,
        "email": "example@yopmail.com",
        "tel": "",
        "family_name": "family_name",
        "given_name": "Kengiven_nameta",
        "permission": "tenant_admin",
        "token": "266537bf8b847dff90247b4782b9725d",
        "crypted_password": "$2a$10$LTi7VxcIoO5ci2Y7RjkqiejuR87rZCSIxAG7rb2pZjHp1RzcUJKaC",
        "salt": "q3EYtWWJ51qbLWFsKi98",
        "family_ruby": "nil",
        "given_ruby": "nil",
        "display_name": "nil",
        "reset_password_token": "nil",
        "reset_password_token_expires_at": "nil",
        "reset_password_email_sent_at": "nil",
        "resigned": false,
        "company_id": 483,
        "password_changed_at": "Tue",
        "16 Mar 2021 15:33:07 JST +09:00": null,
        "temporary_code": "nil",
        "web_token": "nil",
        "via_oauth": false,
        "name_keys": [
          {
            "key": "abc",
            "abc": true
          },
          {
            "key": "xxxx",
            "default": true
          }
        ],
        "tel_to_call": "",
        "external_id": "nil",
        "extension_phone": "nil",
        "code": "nil",
        "remark": "nil",
        "user_agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/89.0.4389.90 Safari/537.36",
        "push_token": "ftK1t5PZgUXtv7Pf5YRGtz:APA91bHh2f1nygSkpKyESh-fakIAnp5awKsrHjQ9YxcN4v-hPgCv-W2C60yeLIgh6TKoTClvIi56uOzdqTgD_DrOeXXHoSAB6ZuK42BHN4600GTAPC8Ew8DM7YOYF_8Z8EPhIRYQCQwO",
        "hashed_idm": "nil",
        "apple_id": "nil",
        "call_type": "video",
        "mobile_token": "e61d2c788a8cc1789bea8a3c885792f1d6262f685e5eb1fcbdd74441e35bccea",
        "code_token": "PnzNjd9C8UOsheGq",
        "code_token_expires_at": "Tue",
        "23 Feb 2021 12:29:02 JST +09:00": null,
        "additional_information": "nil",
        "user_uuid": "f1601172-f34a-4907-992b-4ce4be45ab5b"
      }
    ],
    "no_notify": true,
    "departments": [
      {
        "id": 2016,
        "name": "Sit et ipsum culpa",
        "company_id": 440,
        "translations": {
          "en": "",
          "ja": "Sit et ipsum culpa"
        },
        "sequence": 5,
        "department_id": 2014,
        "apple_id": "",
        "call_type": "video",
        "for_device": false,
        "slack_channel_name": "",
        "tel_to_call": "234234",
        "group_number": 10,
        "slack_mention": "channel",
        "for_call": false,
        "chatwork_rid": "nil",
        "chatwork_label": "nil",
        "email": "nil",
        "tel_type": "sms",
        "extension_phone": "nil",
        "department_uuid": "d7394c8e-7eb4-464b-b06d-bc1ca75d1095"
      }
    ],
    "guests": [
      {
        "family_name": "guest family_name",
        "given_name": "guest given_name",
        "family_ruby": "guest family_ruby",
        "given_ruby": "guest given_ruby",
        "company_name": "guest company_name",
        "email": "guest@example.com"
      }
    ]
  }
```
- POST device/visits/walkin を実行

- status200が返却されること

- walkin予約なしで訪問を作成する

