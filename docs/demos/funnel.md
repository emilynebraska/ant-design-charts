---
title: 漏斗图
---

# 漏斗图

## 基本用法

<a href="https://g2plot.antv.vision/zh/examples/funnel/basic/API" target="_blank">配置</a>

```tsx
import React from 'react';
import { Funnel } from '@ant-design/charts';

const App: React.FC = () => {
  const data = [
    { action: '浏览网站', pv: 50000 },
    { action: '放入购物车', pv: 35000 },
    { action: '生成订单', pv: 25000 },
    { action: '支付', pv: 15000 },
    { action: '成交', pv: 8500 },
  ];

  const config = {
    data,
    title: {
      visible: true,
      text: '漏斗图',
    },
    width: 650,
    height: 450,
    xField: 'action',
    yField: 'pv',
  };
  return <Funnel {...config} />;
};
export default App;
```

## 动态高度

<a href="https://g2plot.antv.vision/zh/examples/funnel/basic/API" target="_blank">配置</a>

```tsx
import React from 'react';
import { Funnel } from '@ant-design/charts';
const App: React.FC = () => {
  const data = [
    { action: '浏览网站', pv: 50000 },
    { action: '放入购物车', pv: 35000 },
    { action: '生成订单', pv: 25000 },
    { action: '支付', pv: 15000 },
    { action: '成交', pv: 8500 },
  ];

  const config = {
    data,
    title: {
      visible: true,
      text: '漏斗图',
    },
    description: {
      visible: true,
      text: '漏斗图 - 动态高度',
    },
    width: 650,
    height: 500,
    xField: 'action',
    yField: 'pv',
    dynamicHeight: true,
  };
  return <Funnel {...config} />;
};

export default App;
```

## 横向展示

<a href="https://g2plot.antv.vision/zh/examples/funnel/basic/API" target="_blank">配置</a>

```tsx
import React from 'react';
import { Funnel } from '@ant-design/charts';
const App: React.FC = () => {
  const data = [
    { action: '浏览网站', pv: 50000 },
    { action: '放入购物车', pv: 35000 },
    { action: '生成订单', pv: 25000 },
    { action: '支付', pv: 15000 },
    { action: '成交', pv: 8500 },
  ];

  const config = {
    data: data,
    xField: 'action',
    yField: 'pv',
    transpose: true,
  };
  return <Funnel {...config} />;
};

export default App;
```