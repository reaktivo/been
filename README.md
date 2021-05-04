### Been

`Been` allows you to convert a statically exported web app into a single executable. It's a simple convenience wrapper around justine.lol's amazing [`redbean`](https://justine.lol/redbean/) project.

### What is redbean

Redbean makes it possible to distribute a web application as a single-file executable that is portable, meaning that it will run on Linux, macOS or Windows.

### How to use

`Been` takes a single argument, a directory of files to be served. Once run, it will create a sibling file to the directory appending `.com` to it's name.

```sh
been ./dist

# ./dist.com server created
./dist.com -p 8080
```

### Usage with static site builders

#### Next.js

```json
"scripts": {
  "build": "next build && next export && been ./out"
}
```

#### Vite.js

```json
"scripts": {
  "build": "vue-tsc --noEmit && vite build && been ./dist",
}
```

#### Create React App

```json
"scripts": {
  "build": "react-scripts build && been ./build"
}
```

### More

You can checkout more of how `redbean` works at [justine.lol's site](https://justine.lol/redbean/)
