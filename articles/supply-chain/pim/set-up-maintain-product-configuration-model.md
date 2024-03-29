---
title: 设置产品配置模型
description: 本文介绍设置和创建产品模型配置的步骤。
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dc9f46d91dc298a5c8babee2b370fea09f61741
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578216"
---
# <a name="set-up-a-product-configuration-model"></a>设置产品配置模型

[!include [banner](../includes/banner.md)]

本文介绍设置和创建产品模型配置的步骤。

| 任务                                                        | 说明                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 创建基础产品。                                    | 从列表 **基础产品** 创建基础产品。 下达基础产品到所有相关公司。 对于用作产品配置模型版本为或作为子组件的基础产品，必须选择 **基于约束的配置** 作为配置技术，且配置维度必须只为产品维度组选择。 |
| 创建组件。                                          | 在 **组件** 页上创建组件。 组件是产品配置模型的构建基块，可在多个产品配置模型中重复使用。                                                                                                                                                                                                                      |
| 创建属性类型。                                     | 在 **属性类型** 页上创建属性类型。 属性类型为用于产品配置模型的所有属性指定一组数据类型。 **布尔值** 属性、具有固定列表的 **文本** 和具有范围类型的 **整数** 列出您基于产品配置模型配置产品变型时可用的一组值。       |
| 创建产品配置模型。                       | 在 **新产品配置模型** 页创建产品配置模型。                                                                                                                                                                                                                                                                                                              |
| 添加属性到产品配置模型。            | 在 **基于约束的产品配置模型详细信息** 页上，在 **属性** 快速选项卡上创建属性。 属性描述产品配置模型的功能。                                                                                                                                                                                                       |
| 添加约束到产品配置模型。           | 在 **基于约束的产品配置模型详细信息** 页上，在 **约束** 快速选项卡上创建约束。 约束是产品配置必须指定的限制。 约束是表达式约束或表约束。                                                                                                                                 |
| 将子组件添加到产品配置模型。         | 在 **基于约束的产品配置模型详细信息** 页上，在 **子组件** 快速选项卡上创建子组件。 子组件与组件相关，并与表示子组件的物料相关联。                                                                                                                                                                       |
| 将用户要求添加到产品配置模型。     | 用户要求类似于子组件，不过，它们不引用物料。 您可以将用户要求视为虚拟物料清单。 所有直接置于用户要求下的物料清单行或工艺路线工序将折叠到父组件。                                                                                                                       |
| 添加物料清单行到产品配置模型。             | 在 **基于约束的产品配置模型详细信息** 页上，在 **物料清单行** 快速选项卡上创建物料清单行。 物料清单行表示构建产品变型所需的部分。                                                                                                                                                                                                 |
| 将工艺路线工序添加到产品配置模型。      | 在 **基于约束的产品配置模型详细信息** 页上，在 **工艺路线工序** 快速选项卡上创建工艺路线工序。 工艺路线工序表示为生成产品变型而执行的一系列步骤中的步骤。                                                                                                                                                    |
| 创建产品配置模型的有效版本。 | 在 **版本** 页中创建产品配置模型的有效版本。 版本是产品配置模型与基础产品之间的关系。 具有有效版本的产品配置模型可以基于销售订单、销售报价单、采购订单或生产订单配置。                                                               |
| 测试产品配置模型。                         | 从 **基于约束的产品配置模型详细信息** 页或 **产品配置模型列表** 页测试产品配置模型。 测试产品配置模型模拟在订单处理期间发生的产品模型配置流程。                                                                                                |
| 创建产品配置模型模板。                | 在 **配置模板** 页创建产品配置模型模板。 配置模板包括产品配置模型中的属性的值。 在 **配置行** 页选择属性值。 您可以选择在产品模型配置期间加载产品模型配置模板。                                                   |
| 配置物料。                                          | 产品配置模型可以基于销售订单、销售报价单、采购订单或生产订单配置。                                                                                                                                                                                                                                                                           |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]