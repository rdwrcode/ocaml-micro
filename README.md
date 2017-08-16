# ocaml microservices with bucklescript
[original article](https://medium.com/dailyjs/how-to-build-disruptive-ocaml-microservices-with-bucklescript-8c2f774f67cd)

## setup
```
yarn add micro
yarn add --dev bs-platform
```

create a new directory and add add.ml into it.
```
mkdir src && cd src
echo "let add a b = a + b" > add.ml
```

run build and check the newly created lib subdirectory.
```
npm run build
```

now to use node to test the auto-generated code
```
$ node
> require("./lib/js/src/add.js").add(5, 6)
11
```

to use our code with existing JS functions, the foreign function interfaces, FFI, are required.

add index.ml in src, and run build again.
```
npm run build
npm start
```
now check http://localhost:1337/ in your browser. You should be able to get Hello world!

use now to deploy it.
