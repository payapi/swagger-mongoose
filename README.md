![Travis Status](https://travis-ci.org/simonguest/swagger-mongoose.svg?branch=master)
# swagger-mongoose

Generate Mongoose Schemas and Models from your Swagger Documents

## Installation

```js
npm install swagger-mongoose
```

## Usage

Simply pass your swagger document to the compile method, and then dynamically access the underlying mongoose models.

```js
var swaggerMongoose = require('swagger-mongoose');

var swagger = fs.readFileSync('./petstore.json');
var Pet = swaggerMongoose.compile(swagger).models.Pet;
```

## Limitations

swagger-mongoose only supports flat schemas, with the following attributes:

  integer, long, float, double, string, password, boolean, date, dateTime, array

swagger-mongoose does not yet support nested schemas or perform/create any validation from the swagger definitions (see issues if you'd like to help)

## License

Copyright 2015 Simon Guest

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
