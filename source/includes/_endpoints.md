# Endpoints

## /get/word

```shell
GET "https://api.jsonipsum.com/get/word/"
```

> JSON response

```json
[
    "consectetur"
]
```

Generate a random single word.

Parameter | Value | Description
--------- | ------- | -----------
[_count](#count) | 1-100 | Set the number of words to be returned. <br>_Default: 1_



## /get/sentence

```shell
GET "https://api.jsonipsum.com/get/sentence/"
```

> JSON response

```json
[
    "Aliqua elit cillum ullamco dolor culpa quis qui sint Lorem eu dolor dolore magna quis aliquip in est consequat officia."
]
```

Generate a random sentence or sentences.

Parameter | Value | Description
--------- | ------- | -----------
[_length](#length) | short<br>medium<br>long | Determine the length of the sentence returned.<br>_Default: medium_
[_count](#count) | 1-100 | Set the number of sentences to be returned. <br>_Default: 1_



## /get/paragraph

```shell
GET "https://api.jsonipsum.com/get/paragraph/"
```

> JSON response

```json
[
    "Cillum sunt exercitation reprehenderit aliqua laborum sit cupidatat amet minim ipsum quis amet Lorem. Adipisicing qui cillum incididunt reprehenderit in aute id culpa ipsum esse minim. Enim sit nostrud eiusmod ipsum amet labore commodo nisi sint aliqua aliquip dolor esse mollit. Velit et proident pariatur labore consectetur non exercitation magna deserunt excepteur dolor. Lorem consectetur quis id consectetur in reprehenderit incididunt culpa incididunt pariatur duis in et ullamco nulla id deserunt anim sunt. Et adipisicing ad ad quis dolore anim est culpa est fugiat voluptate deserunt cillum occaecat Lorem nostrud."
]
```

Generate a random paragraph. With this endpoint multiple sentences will be returned instead of just a single sentence like with the [Sentence](#sentence) endpoint.

Parameter | Value | Description
--------- | ------- | -----------
[_length](#length) | short<br>medium<br>long | Determine the length of the sentence as well as the number of sentences in the paragraph. <br>_Default: medium_
[_count](#count) | 1-100 | Set the number of paragraphs to be returned. <br>_Default: 1_



## /get/data   

```shell
GET "https://api.jsonipsum.com/get/data?_template=post"
```

> JSON response

```json
[
    {
        "id": 1,
        "title": "Aliquip id aliqua nostrud sunt in duis dolore amet in aliquip cillum deserunt excepteur consectetur ullamco.",
        "body": "Sit pariatur minim dolor magna elit fugiat. Cillum qui exercitation tempor occaecat culpa amet consectetur enim ad Lorem. Laboris elit consectetur ea dolor officia adipisicing laborum magna aliquip. Laboris dolor ad nulla ad et et occaecat sint officia proident. Minim occaecat irure cillum excepteur. Pariatur eu do dolore ipsum proident irure ullamco ad consequat deserunt. Culpa exercitation incididunt.",
        "username": "doyle1987",
        "date": {
            "string": "2018-10-10",
            "timestamp": 1539129600000
        },
        "likes": 89,
        "_template": "post"
    }
]
```

This endpoint returns a block of text and/or data. Can create a JSON object of repeatable text blocks where various types of data/text can be requested.

Parameter | Value | Description
--------- | ------- | -----------
[_count](#count) | 1-100 | Set the number of items to be returned.<br>_Default: 1_
[_json](#json) | Stringified Object | Use this parameter to pass a json object in a GET request. JSON must be stringified.
[_template](#template) | user<br>post<br>blog<br>comment<br>todo<br>photo | Return template based JSON object with all its properties.



## /post/data   

```shell
POST "https://api.jsonipsum.com/post/data"

body = {
    "title": "__sentence",
    "body": "__paragraph",
    "date": "__date(past)"
}
```

> JSON response

```json
{
    "success": true,
    "status": 200,
    "body": [
        {
            "id": 101,
            "title": "Lorem sunt aliqua cupidatat aliqua anim anim deserunt minim sunt nostrud eiusmod Lorem ut esse cupidatat.",
            "body": "Sit est id aute incididunt reprehenderit labore aliqua incididunt ullamco amet irure consequat qui quis proident dolore. Do quis voluptate elit nisi amet dolor irure dolor quis Lorem ex occaecat. Dolore enim commodo dolore. Ea aliquip aliqua labore nulla nisi mollit ipsum amet elit commodo id ex nisi nisi reprehenderit. Occaecat incididunt deserunt proident in mollit tempor esse consequat cillum exercitation officia laborum non laboris. Anim eu nulla nulla. Commodo elit esse labore sunt ea duis sint consectetur tempor aliqua velit commodo est laborum deserunt. Elit laborum non voluptate cupidatat commodo pariatur minim excepteur laboris qui ut. Ad ex velit commodo eiusmod anim culpa quis. Elit tempor ullamco consectetur minim dolore cillum aute cupidatat mollit labore qui anim id.",
            "date": {
                "string": "2020-2-21",
                "timestamp": 1582264800000
            }
        }
    ]
}
```

Making a POST request to this endpoint will allow you to send any valid JSON object as the requst body. Allowing you to easily create custom complex objects as a response. API [constructors](#constructors) as values can be used to easily generate random text/data.

Parameter | Value | Description
--------- | ------- | -----------
[_count](#count) | 1-100 | Set the number of items to be returned.<br>_Default: 1_
[_template](#template) | user<br>post<br>blog<br>comment<br>todo<br>photo | Return template based JSON object with all its properties.
