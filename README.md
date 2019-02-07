# Terminal Block Fonts

Big fonts which each character is formed by many blocks for terminal display.

The font is [Arcade](https://www.dafont.com/arcade-ya.font), all fonEt rights belongs to the original author.

## Install

```
npm install --save terminal-block-fonts
```

## Usage

### Generate block string directly

```
const { toBlockString } = require("terminal-block-fonts");

console.log(toBlockString("05:30:12 AM"));
```

### Generate blocks and manipulate them

```
const { toBlock, mapBlock, concatBlocks, toString } = require("terminal-block-fonts");
const { red, yellow, blue } = require("chalk");

const hourBlock = mapBlock(toBlock("05"), red);
const minuteBlock = mapBlock(toBlock("30"), yellow);
const secondBlock = mapBlock(toBlock("12"), blue);
const sepBlock = toBlock(":");

console.log(toString(concatBlocks(
  hourBlock,
  sepBlock,
  minuteBlock,
  sepBlock,
  secondBlock
)));
```
