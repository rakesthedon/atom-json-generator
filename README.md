# json-generator package

Generates random dummy JSON data atom package.

![overview](https://raw.githubusercontent.com/KunihikoKido/atom-json-generator/master/screenshots/overview.gif)

## Installation

Atom Package: https://atom.io/packages/json-generator

```
apm install json-generator
```

Or Settings/Preferences ➔ Install ➔ Search for `json-generator`


## Commands
* Json Generator: New Template
* Json Generator: Generate (ctrl-alt-g)

## Basic available helpers
This package is used based on the [dummy-json](https://github.com/webroo/dummy-json).

You can see the  details of available helpers on the dummy-json.

I am grateful to the dummy-json!


## Additional helpers

### Language

`{{language}}`

Generates a random language.

### Currency

`{{currency}}`

Generates a random currency.

### Gender

`{{gender}}`

Generates a random gender.

### Genre

`{{genre}}`

Generates a random genre.

### Movie title

`{{movie}}`

Generates a random movie.

### Occupation

`{{occupation}}`

Generates a random occupation.

### Japanese lorem ipsum

`{{loremja [sentenceCount]}}`

* `sentenceCount` Number of sentences to generate (optional, default is 1)

Generates random sentences of japanese lorem ipsum text.

### Random
`{{random [csv] }}`

* `csv` comma separated values

`{{random 'apple,orange,banana'}}`

## Overriding built-in mock data.
You can override the built-in data using the package settings.

(Settings/Preferences ➔ Packages ➔ Search for `json-generator`)


## Output Format
You can change the output format.
(Settings/Preferences ➔ Packages ➔ Search for `json-generator`)

### Pretty JSON format
When you have selected the `json`

**Example**

``` json
[
  {
    "_index": "item",
    "_type": "items",
    "_id": "966b0d44-6e1f-4fe6-b971-cf9522d8ec09",
    "firstname": "Francis",
    "lastname": "Backer",
    "age": 3
  },
  {
    "_index": "item",
    "_type": "items",
    "_id": "cb26c226-6a59-4696-8cd0-267bea89fb14",
    "firstname": "Michelle",
    "lastname": "Kilmer",
    "age": 42
  },
  {
    "_index": "item",
    "_type": "items",
    "_id": "9d34885c-9b21-4329-be08-e89e73935d08",
    "firstname": "Jenna",
    "lastname": "Karst",
    "age": 57
  }
]
```
### JSON Lines format
newline-delimited JSON format.

When you have selected the `jsonlines`

**Example**

``` json
{"_index":"item","_type":"items","_id":"15e82060-9b25-408d-be74-9f7aa4a9de8b","firstname":"Isabelle","lastname":"Keesee","age":26}
{"_index":"item","_type":"items","_id":"9ba26f1d-d9b9-4513-834e-01ce22edacad","firstname":"Kathy","lastname":"Oldman","age":79}
{"_index":"item","_type":"items","_id":"ed72b4c7-3d68-4221-a469-e166ab644135","firstname":"Maisha","lastname":"Flinn","age":43}
```

See more details ➔ [JSON Lines](http://jsonlines.org/)

### Elasticsearch Bulk API format
When you have selected the `elasticsearch`

**Example**

``` json
{"index":{"_index":"item","_type":"items","_id":"95e2351f-f61b-4252-a716-1ddd02850638"}}
{"firstname":"Madeleine","lastname":"Rohloff","age":69}
{"index":{"_index":"item","_type":"items","_id":"9ee29322-68ac-4886-83c1-ea7b93c7fa45"}}
{"firstname":"Alejandro","lastname":"Raymond","age":100}
{"index":{"_index":"item","_type":"items","_id":"8e5bd58b-7b30-44c2-9ddb-fc95961676e3"}}
{"firstname":"Travis","lastname":"Pickering","age":39}

```

See more details ➔ [Bulk API | Elasticsearch Reference](https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-bulk.html)
