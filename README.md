# @krolis/opentype

A high-performance, ultra-lightweight OpenType metadata parser focusing on font metrics.

高性能、轻量级的OpenType字体元数据解析其器，专注提取字体度量信息。

[![NPM version](https://img.shields.io/npm/v/@krolis/opentype.svg)](https://npmjs.org/package/@krolis/opentype)

## Install

```shell
npm i @krolis/opentype
```

## Usage

```ts
import { parse } from '@krolis/opentype';

const fm = parse(buffer);
console.log(fm); // { name: 'fontFamily', emSquare: 1000, ascent: 600, descent: 400, lineGap: 20 }
```

## Intro

这是一个从 opentype.js 深度精简而来的高性能解析工具。它剥离了复杂的字形（Glyph）渲染和路径解析逻辑，仅保留字体元数据的读取核心。

This is a high-performance font parser derived from opentype.js. By stripping away complex glyph rendering and path parsing, it focuses solely on extracting essential font metadata with minimal overhead.

本库专门提取以下关键字段：

This library specifically extracts the following key metrics:

```ts
type FontMetrics = {
  name: string,
  emSquare: number,
  ascent: number,
  descent: number,
  lineGap: number,
}
```

# License

[MIT License]
