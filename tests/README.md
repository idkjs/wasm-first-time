# [emscripten](https://emscripten.org/index.html)

# setup emscripten for fishshell

see https://github.com/emscripten-core/emsdk/commit/9538381d56272818cba77a808ba46fdac6c961c8

add the file in link to your emcc then this script to your `fish.config`

```fish
alias emsdk_setup ". /Users/mando/Github/emsdk/emsdk_env.fish"
```

Then run `emsdk_setup` to setup you env in whatever directory you are working in. You will have to do this everytime.
Then run the example:
Compile the `.c` file with `emcc tests/hello_world.c`.

Run `a.out.js` with `node a.out.js`
```sh
emcc-tests> emcc tests/hello_world.c
emcc-tests> node a.out.js
hello, world!
```
