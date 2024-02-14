# WebAssembly example

This example shows how to import WebAssembly files (`.wasm`) and use them inside of a React component that is server rendered. So the WebAssembly code is executed on the server too. In the case of this example we're showing Rust compiled to WebAssembly.

## Preview

Preview the example live on [StackBlitz](http://stackblitz.com/):

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/vercel/next.js/tree/canary/examples/with-webassembly)

## How to use

Execute [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) with [npm](https://docs.npmjs.com/cli/init), [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/), or [pnpm](https://pnpm.io) to bootstrap the example:

```bash
npx create-next-app --example with-webassembly with-webassembly-app
```

```bash
yarn create next-app --example with-webassembly with-webassembly-app
```

```bash
pnpm create next-app --example with-webassembly with-webassembly-app
```

This example uses Rust compiled to wasm, the wasm file is included in the example, but to compile your own Rust code you'll have to [install](https://www.rust-lang.org/learn/get-started) Rust.

To compile `src/add.rs` to `add.wasm` run:

```bash
npm run build-rust
# or
yarn build-rust
# or
pnpm build-rust
```

## Build with Docker

1. Build the container: `docker build . -t react-rust-wasm`
1. Run the container with: `docker run -p 3000:3000 react-rust-wasm`