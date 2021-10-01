# Constructors

Constructors are custom string values that will be parsed into generated data. Each constructor can support specific arguments that can be passed along using parentheses: `__constructor(args)`. Constructors always start with double underscores.

## __word

```JS
__word
```
```json
"incididunt"
```

Return lorem ipsum word.

`__word(count)`

Argument | Value | Description
--------- | --------- | -----------
count | integer | Number of words to return in a single string <br>_Default: 1_



## __phrase

```JS
__phrase
```
```json
"Pariatur commodo id irure"
```

Return a short group of 3 - 6 words.

`__phrase`



## __sentence

```JS
__sentence
```
```json
"Pariatur consequat ut tempor dolor veniam tempor irure sunt."
```

Return a single properly formatted sentence with punctuation.

`__sentence(length)`

Length | Description
--------- | -----------
short | Returns shorter length text <br>_3-6 word sentences_
medium | Returns medium length text. <br>_6-12 word sentences_
long | Returns longer length text. <br>_12-18 word sentences_
rand | Returns random length text. <br>_Default. 3-18 word sentences_



## __paragraph

```JS
__paragraph
```
```json
"Pariatur adipisicing eiusmod esse aliquip reprehenderit labore culpa officia elit voluptate sint irure amet. Et nisi qui do incididunt dolore enim sit. Dolore sit nostrud id enim aliquip sunt dolor irure est culpa aliqua tempor consequat velit labore quis do. Ex deserunt cupidatat est enim adipisicing elit sint ad tempor consectetur adipisicing consequat fugiat excepteur. Consectetur sit in laborum occaecat cupidatat do duis nostrud occaecat proident adipisicing fugiat enim ipsum eiusmod enim elit. Mollit adipisicing in. Proident adipisicing duis mollit commodo deserunt dolore voluptate aute eiusmod sunt aute labore. Fugiat aliqua non pariatur Lorem ut fugiat tempor dolor voluptate officia Lorem velit do duis cillum cupidatat."
```

Return a single string containing multiple sentences.

`__paragraph(length)`

Length | Description
--------- | -----------
short | Returns shorter length text <br>_3-6 sentences in a paragraph_
medium | Returns medium length text. <br>_5-8 sentences in a paragraph_
long | Returns longer length text. <br>_7-12 sentences in a paragraph_
rand | Returns random length text. <br>_Default. 3-12 sentences in a paragraph_



## __alphanum

```JS
__alphanum(18)
```
```json
"mkLEw1sHMDDmKG6hiL"
```

Return a random alphanumeric string.

`__alphanum(count)`

Argument | Type | Description
--------- | --------- | -----------
count | integer | Number of characters to return in a single string <br>_Default: 16_



## __number

```JS
__number(100,200)
```
```json
164
```

Return a single integer from a defined range.

`__number(start,end)`

Argument | Type | Description
--------- | --------- | -----------
start | integer | Range start <br>_Default: 1_
end | integer | Range end <br>_Default: 100_



## __boolean
```JS
__boolean
```
```json
true
```

Return _true_ or _false_ randomly.

`__boolean`



## __date
```JS
__date
```
```json
{
    "string": "2021-1-27",
    "timestamp": 1611727200000
}
```

Return date object with timestamp and string representation.

`__date(range)`

Range | Description
--------- | -----------
past | Random date between today and 3 years ago
today | Todays date <br>_Default_
future | Random date between today and 3 years from now



## __array

```JS
__array(4,my array item)
```
```json
[
    "my array item",
    "my array item",
    "my array item",
    "my array item"
]
```

```JS
__array(4,__sentence)
```
```json
[
    "Labore aliquip veniam aliqua sit.",
    "Id eiusmod anim eiusmod laboris nulla proident ipsum sint nostrud esse sunt eu commodo.",
    "Esse reprehenderit mollit anim ex eu cupidatat irure minim pariatur pariatur mollit est fugiat.",
    "Ullamco in incididunt cillum ex tempor aliquip cupidatat nostrud irure pariatur ipsum voluptate est anim cupidatat et."
]
```

Return array with specified number of items and values.

`__array(count,value)`

Argument | Type | Description
--------- | --------- | -----------
count | integer | Number of items in array
value | string<br>__constructor | Data value for each item in array



## __object

```JS
__object(key1:value1,key2:value2,key3:value3)
```
```json
{
    "key1": "value1",
    "key2": "value2",
    "key3": "value3"
}
```

```JS
__object(word:__word,sentence:__sentence,paragraph:__paragraph)
```
```json
{
    "word": "cillum",
    "sentence": "Non enim irure aute cillum in aute excepteur labore culpa ea consectetur deserunt adipisicing et.",
    "paragraph": "Do dolor est proident aute proident ad sunt et enim aliqua. Esse pariatur eu ipsum cillum ullamco irure amet dolore anim elit et elit incididunt ipsum occaecat ex. Mollit commodo nulla. Eu ex ipsum elit veniam exercitation irure aute elit nulla."
}
```

Return object with nested _key:value_ pairs.

`__object(key:value)`

Argument | Type | Description
--------- | --------- | -----------
key | string | Object key
value | string<br>__constructor | Object key value

<aside class="notice">
The <em>Key:Value</em> argument can be repeated by seperating multiple with commas.
</aside>



## __image

```JS
__image(small)
```
```json
{
    "landscape": "https://via.placeholder.com/480x320",
    "portrait": "https://via.placeholder.com/320x480",
    "square": "https://via.placeholder.com/480x480"
}
```

Return object with urls to landscape, portrait, and square versions of a placeholder image.

`__image(size)`

Size | Description
--------- | -----------
small | Small image size (~480px)
medium | Medium size image (~640px) <br>_Default_
large | Large size image (~960px)



## __file

```JS
__file
```
```json
{
    "name": "Placeholder.pdf",
    "link": "https://upload.wikimedia.org/wikipedia/commons/a/a4/Placeholder.pdf",
    "mime_type": "application/pdf",
    "size": 2749
}
```

Return object with file name, file link, mime type, and random file size data for a sample file.

`__file`



## __video

```JS
__video
```
```json
{
    "id": "87110435",
    "url": "https://vimeo.com/87110435",
    "embed": "https://player.vimeo.com/video/87110435",
    "duration": 106194
}
```

Return video object with id, url, embed url, and random duration data.

`__video`



## __coordinates

```JS
__coordinates
```
```json
{
    "latitude": "40.5343",
    "longitude": "-64.0280"
}
```

Return object with random latitude and longitude values.

`__coordinates`



## __address

```JS
__address
```
```json
{
    "street": "474 Linnie Cape",
    "city": "Johnstonborough",
    "postal": "90062-1473",
    "province": "Nebraska",
    "country": "Kenya",
    "countrycode": "LC"
}
```

```JS
__address(postal)
```
```json
"08087-0895"
```

Return address object with street, city, province, postal, country, and country code.

`__address(option)`

Option | Description
--------- | -----------
street | Only return street value as string
city | Only return city value as string
postal | Only return postal code value as string
province | Only return province value as string
country | Only return country value as string
countrycode | Only return abbreviated country code value as string



## __user

```JS
__user
```
```json
{
    "name": {
        "fullname": "Beaulah Macejkovic",
        "firstname": "Beaulah",
        "lastname": "Macejkovic"
    },
    "email": "beaulah1996@jsonipsum.com",
    "username": "beaulah1996"
}
```

```JS
__user(email)
```
```json
"jocelyn2009@jsonipsum.com"
```

Return user object with name, email, username, and address.

`__user(option)`

Option | Description
--------- | -----------
name | Only return name object
email | Only return city value as string
username | Only return username as string

## __template

```JS
__template(post)
```
```json
{
    "title": "Sint sunt id aliquip ut do anim occaecat Lorem.",
    "body": "Pariatur non deserunt sunt commodo non Lorem sint quis sunt aliquip ad. Dolore do occaecat adipisicing consequat elit id. Aliqua qui sit aliquip duis est ad sunt duis amet id aute dolore esse velit nostrud ut quis.",
    "username": "mona1987",
    "date": {
        "string": "2020-11-3",
        "timestamp": 1604383200000
    },
    "likes": 92
}
```

Quickly return a pre-formatted JSON objects.

`__template(option)`

Option | Description
--------- | -----------
user | Returns a User object with name, email, username, and address.
post | Returns a Post object with title, body, username, date, and likes count.
blog | Return a Blog object with title, excerpt, thumbnail, author, date, and comments count.
comment | Return a Comment object with body, username, reply count, likes count, and date.
todo | Return a Todo object with title, date, and complete boolean.
photo | Return a Photo object with image, title, caption, username, date, comment count, and likes count.
