---
title: Extend
order: 3
---

`<Graphin/>` 组件 `props.extend` 配置。用于配置 Graphin 布局/NodeShape/Marker 的扩展。

|   属性    | 类型                                                           | 是否必选 | 说明       |
| --------- | -------------------------------------------------------------- | -------- | ---------- |
| layout    | (graphin: [Graphin](), prevProps: [GraphinProps](/zh/docs/api/graphin#props)) => [ExendLayout](#extendlayout)[ ]  | 否       | 自定义布局 |
| nodeShape | (node: [Node](/zh/docs/api/graphin#node)) => [ExtendNodeShape](#extendnodeshape)[ ] | 否       | 自定义节点 |
| marker    | ( ) => [ExtendMarker](#extendmarker)[ ]         | 否       | 自定义图标 |
| icon   | ( ) => [ExtendIcon](#extendicon)[ ]         | 否       | 自定义图标（iconfont 形式） |

### ExendLayout

自定义布局配置

|   属性   | 类型                  | 是否必选 | 说明          |
| -------- | --------------------- | -------- | ------------- |
| name    | string       | **是** | 布局名称，唯一标识符      |
| desc  | string     | **是**       | 布局展示名称      |
| icon  | string   | **是**     | antd icon 类型     |
| layout      | (data: [Data](/zh/docs/api/graphin#data), options: [LayoutOption](/zh/docs/api/layout#layoutoptions)) => { data: [Data](/zh/docs/api/graphin#data); forceSimulation?: [ForceSimulation]();} | **是**       | 布局函数，用于计算布局。接受节点，返回带有位置的节点      |

### ExendNodeShape

自定义 NodeShape 配置

|   属性   | 类型                  | 是否必选 | 说明          |
| -------- | --------------------- | -------- | ------------- |
| shape    | string       | **是** | 自定义的 NodeShape 名称，唯一标识符      |
| shapeComponents  | [ShapeComponent](#shapecomponent)[ ]     | **是**       | 构成 Shape 的组件数组      |

#### ShapeComponent

|   属性   | 类型                  | 是否必选 | 说明          |
| -------- | --------------------- | -------- | ------------- |
| shape    | string       | **是** | G6 内置的 NodeShape 名称      |
| attrs  | [Attrs](https://www.yuque.com/antv/g6/ffzwfp)     | **是**       | G6 Shape 属性      |


### ExendMarker

自定义 Marker 配置

|   属性   | 类型                  | 是否必选 | 说明          |
| -------- | --------------------- | -------- | ------------- |
| name    | string       | **是** | icon 类型      |
| path | string     | **是**       | svg 路径数据      |


### ExtendIcon

自定义 Icon 配置

|   属性   | 类型                  | 是否必选 | 说明          |
| -------- | --------------------- | -------- | ------------- |
| fontFamily    | string       | **是** | 字体名称      |
| map | { font\_class: string; unicode\_decimal: number; }[ ]     | **是**       | iconfont 的 class name 和 unicode decimal 的映射集合      |

