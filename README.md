# Bullet Resume
## 简介
- 主要技术栈：Vue3 + Vite4 + TS + Unocss
- 以 bullet dot 为内容主体的简历
- [view demo](http://resume.corgi.plus/)

## 开始
安装依赖
```bash
$ pnpm install
```
开始构建

```bash
$ pnpm dev
```
使用

修改 `src/config/data.json`

## 说明
除了个人信息（header）部分，内容都是由`Item`组件渲染


``` typescript
type Props = {
title: string,
itemInfoList: ItemInfoType[]
}

type ItemInfoType = {
name?: string,
brief?: string[],
desc?: string[],
}
```
如上所示，每个`Item` 由四个部分组成：标题，名称，简介，描述。

简介部分可以是 “词汇” 也可以是“句子”。建议词汇数量不超过四个。

描述部分是一个无序列表。

除标题是必须外，其他三个都是可选值。

本仓库的`data.json`由`chatgpt`生成，不具备真实性。

## TODO
- [ ] 在线编辑
- [ ] 中英切换
- [ ] 性能优化
