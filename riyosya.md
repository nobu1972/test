FORMAT: 1A
HOST: http://polls.apiblueprint.org/

# nobu1972

Polls is a simple API allowing consumers to view polls and vote in them.

## 利用者リスト [/riyosyalist/{id}]

+ Parameters
    + id ( number, `1`) ... メンバーのID、型は数値

### 利用者リストを返す [GET]

+ Response 200 (application/json)

        [
            {
            "id": 1,
            "name": "カイゴ太郎"
            }
        ]

### 利用者を新規登録 [POST]

You may create your own question using this action. It takes a JSON
object containing a question and a collection of answers in the
form of choices.

+ Request (application/json)

        {
          [
            {
            "id": 1,
            "name": "カイゴ太郎"
            },
            {
            "id": 2,
            "name": "カイゴ次郎"
            }
          ]
        }

+ Response 201 (application/json)

    + Headers

            Location: /questions/2

    + Body
```json
            {
                "question": "Favourite programming language?",
                "published_at": "2015-08-05T08:40:51.620Z",
                "choices": [
                    {
                        "choice": "Swift",
                        "votes": 0
                    }, {
                        "choice": "Python",
                        "votes": 0
                    }, {
                        "choice": "Objective-C",
                        "votes": 0
                    }, {
                        "choice": "Ruby",
                        "votes": 0
                    }
                ]
            }
```


### Response


<!--
type: tab
title: Schema
-->

```json
{
  data: [
            {
            "id": 1,
            "name": "カイゴ太郎"
            },
            {
            "id": 2,
            "name": "カイゴ次郎"
            }
        ]
}
```
<!-- type: tab-end -->
