# json-typescript
TypeScript interfaces for the JSON objects :rooster::koala::dragon:

This type is not provided in the default library

## Advocacy

[@Elephant-Vessel](https://github.com/Microsoft/TypeScript/issues/1897#issuecomment-271146964) this has deeper utility that just representing some arbitrary format like JSON. It enables us to more clearly distinguish data from operations on data. That's a quite fundamental piece of our domain as software developers, I don't think that would be a totally useless concept to have available and tangible in code, even if OOP still might be the norm.


* issue in typescript repo https://github.com/Microsoft/TypeScript/issues/1897 along with suggestions
* An proposed solution http://www.typescriptlang.org/play/#src=interface%20Json%20%7B%0D%0A%09%5Bx%3A%20string%5D%3A%20string%20%7C%20number%20%7C%20boolean%20%7C%20Date%20%7C%20Json%20%7C%20JsonArray%3B%0D%0A%7D%0D%0A%0D%0Ainterface%20JsonArray%20extends%20Array%3Cstring%20%7C%20number%20%7C%20boolean%20%7C%20Date%20%7C%20Json%20%7C%20JsonArray%3E%20%7B%20%7D%0D%0A%0D%0Ainterface%20Id%20extends%20Json%20%7B%0D%0A%09id%3A%20number%3B%0D%0A%7D%0D%0A%0D%0Avar%20z%20%3D%20()%3A%20Id%20%3D%3E%20(%7B%20id%3A%2034%20%7D)%3B%0D%0A%0D%0Aclass%20Bass%20%7B%0D%0A%09f()%3A%20Id%20%7B%20return%20undefined%3B%20%7D%0D%0A%7D%0D%0A%0D%0Aclass%20Foos%20extends%20Bass%20%7B%0D%0A%09f()%20%7B%20return%20%7B%20id%3A%2010%20%7D%7D%0D%0A%7D%0D%0A%0D%0Ainterface%20Foo%20extends%20Json%20%7B%0D%0A%09foo%3A%20%7B%20val%3A%20string%20%7D%3B%0D%0A%7D%0D%0A%0D%0Avar%20result%3A%20Id%5B%5D%20%3D%20%27a%7Cb%27.split(%27%7C%27).map(item%20%3D%3E%20%7B%0D%0A%09return%20%7B%20id%3A%200%20%7D%3B%0D%0A%7D)%3B
* another reflexion http://blog.ninja-squad.com/2016/03/15/ninja-tips-2-type-your-json-with-typescript/
* The spec http://www.json.org/


## Contributing
See CONTRIBUTING.md
