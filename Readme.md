# `esmo` bug with `pnpm` install semantics

To reproduce the error

- clone this repo
- cd into it
- run `npm install -g pnpm`
- run `pnpm install`
- run `./node_modules/.bin/esmo test.ts`

Observe the last command failed with node complaining about it being unable
to find `esbuild-node-loader` which is a defined dependency of `esno` package.

This works fine with `npm@7`. 
