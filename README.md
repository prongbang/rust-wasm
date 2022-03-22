# rust-wasm

https://rustwasm.github.io/docs/book/introduction.html

## Install [Rust](https://www.rust-lang.org/tools/install)

```shell
$ curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

## Install [wasm-pack](https://rustwasm.github.io/wasm-pack/installer/)

Building, testing, and publishing Rust-generated WebAssembly.

````shell
$ curl https://rustwasm.github.io/wasm-pack/installer/init.sh -sSf | sh
````

## Install [cargo-generate](https://github.com/cargo-generate/cargo-generate)

Make a project.

```shell
$ cargo install cargo-generate
```

## Install [npm](https://docs.npmjs.com/getting-started)

Package manager for JavaScript.

```shell
$ npm install npm@latest -g
```

## Clone project

```shell
$ cargo generate --git https://github.com/rustwasm/wasm-pack-template
```

### Build the Project

```shell
$ cd wasm-game-of-life
$ wasm-pack build 
```

### Output

```shell
pkg
├── README.md
├── package.json
├── wasm_game_of_life.d.ts
├── wasm_game_of_life.js
├── wasm_game_of_life_bg.js
├── wasm_game_of_life_bg.wasm
└── wasm_game_of_life_bg.wasm.d.ts
```

### Putting it into a Web Page

```shell
$ cd wasm-game-of-life
$ npm init wasm-app www
```

### Output

```shell
wasm-game-of-life/www/
├── bootstrap.js
├── index.html
├── index.js
├── LICENSE-APACHE
├── LICENSE-MIT
├── package.json
├── README.md
└── webpack.config.js
```

### Add package in `package.json`

```shell
"dependencies": {                     // Add this three lines block!
  "wasm-game-of-life": "file:../pkg"
},
```

### Install package

```shell
$ npm install
```

### Modify `www/wasm-game-of-life/index.js`

```shell
import * as wasm from "wasm-game-of-life";

wasm.greet("wasm-game-of-life!");
```

### Serving Locally

```shell
$ npm run start
```

### Result

![img.png](wasm-game-of-life/screenshot/img-1.png)

![img.png](wasm-game-of-life/screenshot/img-2.png)