# Examples
Pariatur adipisicing eiusmod esse aliquip reprehenderit labore culpa officia elit voluptate sint irure amet. Et nisi qui do incididunt dolore enim sit. Dolore sit nostrud id enim aliquip sunt dolor irure est culpa aliqua tempor consequat velit labore quis do.

## `GET` Text

```shell
GET "https://api.jsonipsum.com/get/sentence/?_length=short"
```
> JSON Response

```json
[
    "Velit duis ad dolor ullamco velit."
]
```
```shell
GET "https://api.jsonipsum.com/get/sentence/?_count=4"
```
> JSON Response

```json
[
    "Sint culpa et eu ad et laborum elit aliquip est ea sit ipsum tempor nisi incididunt.",
    "Occaecat ut magna ullamco eiusmod minim exercitation in.",
    "Amet duis ad.",
    "Enim excepteur aliquip commodo qui."
]
```

The easiest way to start with the API is just to make a GET request to one of the direct lorem ipsum endpoints: [word](#word), [sentence](#sentence), [paragraph](#paragraph).



## `GET` Basic Object

```shell
GET "https://api.jsonipsum.com/get/data/?key1=__phrase&key2=__sentence&key3=My static value"
```
> JSON Response

```json
[
    {
        "id": 1,
        "key1": "Ex consectetur non sint dolore nulla",
        "key2": "Commodo excepteur do ea elit duis nostrud dolor qui fugiat dolor fugiat minim reprehenderit.",
        "key3": "My static value"
    }
]
```

Using the [data](#data) endpoint, you can simply pass url query parameters with values to generate a JSON response. This example is using the provided [constructors](#constructors) as a way to randomly generate values for a given key, along with a static string for `key3`.



## `GET` Template Object

```shell
GET "https://api.jsonipsum.com/get/data/?_template=user"
```
> JSON Response

```json
[
    {
        "id": 1,
        "name": {
            "fullname": "Oren Lindgren",
            "firstname": "Oren",
            "lastname": "Lindgren"
        },
        "email": "oren1995@jsonipsum.com",
        "username": "oren1995"
    }
]
```

Using the [data](#data) endpoint along with the [_template](#template) parameter, you can request pre-formatted JSON objects. If you pass additional key parameters, you can override any of the default keys/values.


## `GET` Template Object with additional data

```shell
GET "https://api.jsonipsum.com/get/data/?_template=user&address=__address&password=__alphanum(18)"
```
> JSON Response

```json
[
    {
        "id": 1,
        "name": {
            "fullname": "Oren Lindgren",
            "firstname": "Oren",
            "lastname": "Lindgren"
        },
        "email": "oren1995@jsonipsum.com",
        "username": "oren1995",
        "address": {
            "street": "667 Grady Circle",
            "city": "North Araceli",
            "postal": "87768-8549",
            "province": "Louisiana",
            "country": "Saint Vincent and the Grenadines",
            "countrycode": "CI"
        },
        "password": "tw4VghTwiQ2KECvonh"
    }
]
```

You can append additional data to prepared [_template](#template) objects, by passing in additinal parameters with the request. The additional data values can be [__constructors](#constructors) or static values.


## `GET` Array of Template Objects

```shell
GET "https://api.jsonipsum.com/get/data/?_template=user&_count=3"
```
> JSON Response

```json
[
    {
        "id": 1,
        "name": {
            "fullname": "Bonita Grady",
            "firstname": "Bonita",
            "lastname": "Grady"
        },
        "email": "bonita1999@jsonipsum.com",
        "username": "bonita1999"
    },
    {
        "id": 2,
        "name": {
            "fullname": "Deangelo Effertz",
            "firstname": "Deangelo",
            "lastname": "Effertz"
        },
        "email": "deangelo1983@jsonipsum.com",
        "username": "deangelo1983"
    },
    {
        "id": 3,
        "name": {
            "fullname": "Elvera Hickle",
            "firstname": "Elvera",
            "lastname": "Hickle"
        },
        "email": "elvera1991@jsonipsum.com",
        "username": "elvera1991"
    }
]
```

To return more than a single object you can pass in the `_count` paramter with an integer value. Here you can see we requested `3` of the pre-formatted `user` objects.



## `GET` Custom Object

```shell
GET 'https://api.jsonipsum.com/get/data?_json={"title":"__sentence","body":"__paragraph","date":"__date(past)"}'
```
> JSON Response

```json
[
    {
        "id": 1,
        "title": "Culpa adipisicing ea proident labore mollit.",
        "body": "Lorem adipisicing consectetur fugiat Lorem nisi. Esse aliqua duis proident eiusmod voluptate commodo irure esse enim occaecat. Dolore elit dolor consectetur mollit et dolore aliqua culpa quis dolor ea proident sint. Magna veniam aliqua consectetur consequat dolor pariatur eu magna proident ipsum reprehenderit dolor duis Lorem culpa ad. Magna exercitation in commodo sunt in ex voluptate laborum quis dolor sint est exercitation tempor et. Eiusmod proident ea sint fugiat exercitation amet adipisicing nulla fugiat nulla ea enim dolor elit veniam sit qui. Exercitation nisi eiusmod ad nostrud et veniam incididunt dolore dolor et culpa elit aliqua ipsum.",
        "date": {
            "string": "2020-10-11",
            "timestamp": 1602374400000
        }    }
]
```

Using the [data](#data) endpoint along with the [_json](#json) parameter, you can pass in any JSON object, as a string. The API will parse key/value pairs and return the object in the response.

This example is using the provided [constructors](#constructors) as a way to randomly generate values for the given keys.



## `GET` Array of Custom Objects

```shell
GET 'https://api.jsonipsum.com/get/data?_json={"title":"__sentence","body":"__paragraph","date":"__date(past)"}&_count=3'
```
> JSON Response

```json
[
    {
        "id": 1,
        "title": "Dolor ullamco officia esse et aliquip pariatur sint occaecat.",
        "body": "Minim incididunt laborum exercitation labore voluptate fugiat consectetur consectetur Lorem mollit culpa est duis. In Lorem reprehenderit labore ex anim aliquip aliqua fugiat. Consectetur aliquip laboris labore do aliquip. Dolor veniam Lorem voluptate laboris ut labore quis ullamco dolore eiusmod nisi proident.",
        "date": {
            "string": "2018-8-18",
            "timestamp": 1534568400000
        },
    },
    {
        "id": 2,
        "title": "Anim amet eiusmod consectetur fugiat ex.",
        "body": "Elit ullamco nulla labore do dolore sint nostrud dolore ad. Officia culpa mollit non adipisicing officia tempor Lorem dolor nulla voluptate adipisicing ea. Labore aliquip sunt nisi velit. Magna magna eu adipisicing excepteur consectetur id proident velit consequat quis consequat tempor in exercitation. Aliqua aliquip cupidatat magna anim aute. Aute nostrud velit sunt tempor mollit irure labore eu voluptate deserunt officia tempor enim enim do. Cillum labore fugiat. Sit Lorem deserunt proident quis ad consequat voluptate laborum reprehenderit. Consequat eiusmod occaecat sit exercitation cillum magna officia incididunt et deserunt. Culpa consectetur ullamco tempor anim enim laboris do mollit. Ad tempor et fugiat ipsum Lorem eiusmod sunt eiusmod nulla cupidatat non proident duis voluptate pariatur.",
        "date": {
            "string": "2019-12-2",
            "timestamp": 1575266400000
        },
    },
    {
        "id": 3,
        "title": "Sint adipisicing commodo Lorem elit anim tempor in.",
        "body": "Ullamco irure mollit non minim est. Enim aute laborum laboris ullamco sit ad eiusmod officia sunt fugiat eiusmod laborum esse ullamco culpa. Aliquip dolor nulla et commodo dolor ea. Enim cillum incididunt. Dolor cupidatat mollit aliqua non laboris fugiat enim excepteur culpa incididunt qui reprehenderit voluptate deserunt qui ullamco ipsum. Adipisicing ea exercitation occaecat tempor elit proident. Ad incididunt amet id nulla laboris anim eiusmod. Ipsum laborum do irure nostrud anim culpa elit sunt velit laborum nostrud proident mollit adipisicing. Esse pariatur occaecat pariatur enim est commodo dolore. Consectetur adipisicing non dolor non ipsum mollit exercitation velit aute excepteur minim labore qui in. Dolore sint magna deserunt dolor qui veniam tempor commodo deserunt esse excepteur velit. Dolore minim ut nisi consectetur.",
        "date": {
            "string": "2020-3-16",
            "timestamp": 1584334800000
        },
    }
]
```

By passing the `_count` parameter, you can return multiple objects with a single request. This example is using the provided [constructors](#constructors) as a way to randomly generate values for the given keys.



## `POST` Custom Object

```shell
POST 'https://api.jsonipsum.com/post/data'

body = {
    "title": "__sentence",
    "body": "__paragraph",
    "date": "__date(past)"
}
```
> JSON Response

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

Using the [data](#data) endpoint with a POST request, you can pass in any JSON object as the request body. The API will parse key/value pairs and return the object in the response.

This example is using the provided [constructors](#constructors) as a way to randomly generate values for the given keys.



## `POST` Array of Custom Objects

```shell
POST 'https://api.jsonipsum.com/post/data'

body = {
    "title": "__sentence",
    "body": "__paragraph",
    "date": "__date(past)",
    "_count": 3
}
```
> JSON Response

```json
{
    "success": true,
    "status": 200,
    "body": [
        {
            "id": 101,
            "title": "Lorem sit minim quis elit laboris.",
            "body": "Mollit in ex excepteur mollit do irure excepteur ex tempor. Aliquip laboris qui qui. Aliquip minim in ut amet veniam magna non mollit et dolor qui veniam anim do sint culpa do.",
            "date": {
                "string": "2018-8-3",
                "timestamp": 1533272400000
            }
        },
        {
            "id": 102,
            "title": "Mollit aliquip dolore consequat et qui culpa culpa.",
            "body": "Nisi eiusmod duis dolore. Sunt irure qui id reprehenderit deserunt magna deserunt velit elit elit tempor occaecat. Eiusmod ea ipsum Lorem sint ad consectetur. Est sunt anim nulla sit deserunt minim enim esse eiusmod officia veniam et in adipisicing mollit adipisicing magna. Quis dolore enim labore ipsum minim culpa qui reprehenderit laborum tempor sunt labore nostrud aliquip. Qui elit pariatur veniam adipisicing occaecat fugiat Lorem occaecat sint consectetur non et veniam non magna et.",
            "date": {
                "string": "2018-4-22",
                "timestamp": 1524373200000
            }
        },
        {
            "id": 103,
            "title": "Deserunt do veniam sunt consequat enim eiusmod occaecat.",
            "body": "Veniam dolor in ex dolore proident dolor ipsum excepteur adipisicing id. Commodo culpa cillum veniam ex duis elit. Irure ad ut ea ea anim sunt occaecat cillum. Magna do tempor. Amet proident nostrud. Ullamco velit eu exercitation ut deserunt eiusmod exercitation labore. Ea enim sint dolore do deserunt deserunt ex tempor tempor mollit irure ea. Anim ad deserunt eiusmod fugiat. Adipisicing amet proident ullamco esse sit velit anim ea irure deserunt qui reprehenderit veniam veniam. Magna laborum ipsum. Enim est consectetur.",
            "date": {
                "string": "2018-10-18",
                "timestamp": 1539820800000
            }
        }
    ]
}
```

Just like with `GET` requests, you can request multiple objects from a response using the `POST` method and [data](#data) endpoint. Here we include the `_count` parameter within the request body.
