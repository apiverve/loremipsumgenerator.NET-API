Lorem Ipsum Generator API
============

Lorem Ipsum Generator is a simple tool for generating lorem ipsum text. It returns the generated text.

![Build Status](https://img.shields.io/badge/build-passing-green)
![Code Climate](https://img.shields.io/badge/maintainability-B-purple)
![Prod Ready](https://img.shields.io/badge/production-ready-blue)

This is a .NET Wrapper for the [Lorem Ipsum Generator API](https://apiverve.com/marketplace/api/loremipsumgenerator)

---

## Installation

Using the .NET CLI:
```
dotnet add package APIVerve.API.LoremIpsumGenerator
```

Using the Package Manager:
```
nuget install APIVerve.API.LoremIpsumGenerator
```

Using the Package Manager Console:
```
Install-Package APIVerve.API.LoremIpsumGenerator
```

From within Visual Studio:

1. Open the Solution Explorer.
2. Right-click on a project within your solution.
3. Click on Manage NuGet Packages...
4. Click on the Browse tab and search for "APIVerve.API.LoremIpsumGenerator".
5. Click on the APIVerve.API.LoremIpsumGenerator package, select the appropriate version in the right-tab and click Install.


---

## Configuration

Before using the loremipsumgenerator API client, you have to setup your account and obtain your API Key.  
You can get it by signing up at [https://apiverve.com](https://apiverve.com)

---

## Usage

The Lorem Ipsum Generator API documentation is found here: [https://docs.apiverve.com/api/loremipsumgenerator](https://docs.apiverve.com/api/loremipsumgenerator).  
You can find parameters, example responses, and status codes documented here.

### Setup

###### Authentication
Lorem Ipsum Generator API uses API Key-based authentication. When you create an instance of the API client, you can pass your API Key as a parameter.

```
// Create an instance of the API client
var apiClient = new LoremIpsumGeneratorAPIClient("[YOUR_API_KEY]", true);
```

---


### Perform Request
Using the API client, you can perform requests to the API.

###### Define Query

```
var queryOptions = new loremipsumgeneratorQueryOptions {
  sentences = 3,
  words = 150
};
```

###### Simple Request

```
var response = apiClient.Execute(queryOptions);
if(response.error != null) {
	Console.WriteLine(response.error);
} else {
    var jsonResponse = JsonConvert.SerializeObject(response, Newtonsoft.Json.Formatting.Indented);
    Console.WriteLine(jsonResponse);
}
```

###### Example Response

```
{
  "status": "ok",
  "error": null,
  "data": {
    "words": 150,
    "sentences": 0,
    "text": "qui qui laborum in nisi qui ad dolor in culpa exercitation esse anim sint cupidatat do tempor enim eu consectetur adipisicing anim adipisicing laborum aliqua cupidatat elit cupidatat aliqua proident elit nisi sint irure velit duis laborum dolor eiusmod culpa labore id aliqua officia consequat sunt eu esse magna pariatur commodo occaecat nostrud pariatur magna reprehenderit do adipisicing ea incididunt quis fugiat magna minim incididunt ad aliqua do sit est irure non tempor deserunt sit quis veniam culpa labore exercitation irure mollit excepteur veniam aliqua exercitation ad amet in ullamco ex consequat anim occaecat Lorem aliqua tempor consequat dolore fugiat magna est occaecat excepteur ex fugiat ea eu aliqua cillum nulla velit non nisi ad irure sunt sit do occaecat ad do sit irure excepteur exercitation qui ullamco sit qui deserunt voluptate eiusmod nostrud elit dolor velit exercitation laboris esse est deserunt consectetur est id quis non commodo consectetur eu"
  }
}
```

---

## Customer Support

Need any assistance? [Get in touch with Customer Support](https://apiverve.com/contact).

---

## Updates
Stay up to date by following [@apiverveHQ](https://twitter.com/apiverveHQ) on Twitter.

---

## Legal

All usage of the APIVerve website, API, and services is subject to the [APIVerve Terms of Service](https://apiverve.com/terms) and all legal documents and agreements.

---

## License
Licensed under the The MIT License (MIT)

Copyright (&copy;) 2024 APIVerve, and Evlar LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.