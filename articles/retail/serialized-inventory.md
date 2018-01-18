---
title: "序列化产品中的 POS 改进"
description: "此主题列出了为了帮助您节省时间和提高生产效率而对序列化产品做出的改进。"
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 83c2ce79f5bef058f55af0ecf498b207efc0507a
ms.contentlocale: zh-cn
ms.lasthandoff: 12/14/2017

---

# <a name="pos-improvements-for-serialized-products"></a>序列化产品中的 POS 改进

[!include[banner](includes/banner.md)]

## <a name="overview"></a>概览 
基于零售总部中的设置，产品可归类为序列化或非序列化。 产品序列化时，可以为每个物料分配一个唯一编号，以便跟踪保修、跟踪物料和确认所有权。 尽管在我们的现代/云销售点 (POS) 中存在为序列化产品提供序列号的能力，我们仍然增加了一些改进，以帮助出纳节省时间和提高生产效率。  

## <a name="pos-improvements"></a>POS 改进

- **在结帐时才需要使用序列号** - 以前，出纳向交易记录添加序列化产品时必须提供序列号。 在客户服务解决方案中，如果出纳和销售内勤有机会向上销售产品，该要求就成为了一个问题。 在付款步骤之前，经常要在购物车中更新产品。 因此，出纳每次添加新产品时，系统就会提示出纳提供序列号。 序列号对话框现在包括一个**稍后添加**按钮。 因此，销售内勤可以将物料添加到交易记录中，但可以稍后提供序列号。 销售内勤可以迅速添加和替换购物车中的序列化物料，然后在要结帐时提供序列号。 如果未提供任何序列化产品的序列号，出纳在尝试完成交易时会收到错误消息。 该消息指出出纳必须提供缺失的序列号后才能继续。

    对于跳过序列号的每个序列化物料，交易记录行下都会显示一条注释。 该注释指出未提供该物料的序列号。 因此，出纳可以快速找到缺少序列号的物料。

    新的**添加序列号**操作也为缺少序列号的物料提供序列号。 提供序列号后，无法编辑该序列号。 出纳必须使该行失效并重新添加产品。 
    
- **下达客户订单不需要提供序列号** - 可以在一个商店下达客户订单，并从另一个商店完成该订单。 下达客户订单的出纳不必提供序列号。 在领料或装货步骤中将提供该序列号。 但是，选择了**自提**交货类型的所有行项都必须提供序列号。 否则无法完成交易记录。    
- **序列化产品没有在交易记录屏幕上聚合** - 使用**功能配置文件**页的**终端**字段组中的**聚合产品**设置可以在交易记录屏幕上聚合相同的非序列化产品。 聚合相同产品时，更容易在交易记录网格中进行查看。 但是，由于序列号通常是唯一的，且销售内勤在结帐前无需输入序列号，因此**聚合产品**设置不适用于序列化产品。 因此，如果选择了**聚合产品**设置，则不会在交易记录屏幕上聚合序列化产品。
- **按序列号搜索日记帐的功能** - 现在可以额外按序列号搜索日记帐。 若要执行此操作，请打开“日记帐”操作，并按下应用栏上的“高级搜索”按钮。 使用“添加筛选器”按钮，也可以应用筛选器来搜索序列号。

