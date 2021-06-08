# [emscripten](https://emscripten.org/index.html)

# setup emscripten for fishshell

see https://github.com/emscripten-core/emsdk/commit/9538381d56272818cba77a808ba46fdac6c961c8

add the file in link to your emcc then this script to your `fish.config`

```fish
alias emsdk_setup ". /Users/mando/Github/emsdk/emsdk_env.fish"
```

Then run `emsdk_setup` to setup you env in whatever directory you are working in. You will have to do this everytime.

# WASM in HTML

https://marcoselvatici.github.io/WASM_tutorial/

```sh
emcc html/hello.c -o html/hello.js -s WASM=1 -s EXPORTED_FUNCTIONS='["_fib"]' -s EXTRA_EXPORTED_RUNTIME_METHODS='["cwrap"]'
```

```sh
serve html
```

# WASM in JS
Then run the example:
Compile the `.c` file with:
```sh
emcc hello/hello_world.c -o hello/a.out.js
```

Run `hello/a.out.js` with `node hello/a.out.js`
