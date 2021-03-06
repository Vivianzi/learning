# 集合

集合就是一组文档。如果说MongoDB中的文档类似于关系型数据库中的行，那么集合就如同表。

## 无模式

- 集合是无模式的。这意味着一个集合里面的文档可以是各式各样的。
- 为什么还要使用多集合？
    - 把各种各样的文档都混在一个集合里面，无论对于开发者还是管理员来说都是噩梦
    - 在一个集合里面查询特定类型的文档在速度上也很不划算，分开做多个集合要快得多
    - 把同种类型的文档放在一个集合里，这样数据会更加集中
    - 当创建索引的时候，文档会有附加的结构（尤其是有唯一索引的时候）

## 命名

集合名可以是满足下列条件的任意UTF-8字符串
- 不能是空字符串""
- 不能含有\0字符（空字符）
- 不能以“system.”开头
- 不能含有保留字符$

## 子集合

组织集合的一种惯例是使用“.”字符分开的按命名空间划分的子集合。