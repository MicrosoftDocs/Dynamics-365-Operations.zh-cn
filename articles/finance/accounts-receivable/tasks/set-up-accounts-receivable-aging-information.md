---
title: 设置并生成应收帐款的帐龄信息
description: 本指南将帮助您设置帐龄期间定义、帐龄客户余额以及查看“帐龄余额表”和“收款”页的余额。
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b21fe217aacd11821ff8d5cf7c7682b2181e36c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220075"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>设置并生成应收帐款的帐龄信息

[!include [banner](../../includes/banner.md)]

本指南将帮助您设置帐龄期间定义、帐龄客户余额以及查看“帐龄余额表”和“收款”页的余额。 此记录使用 USMF 公司演示。


## <a name="create-an-aging-period-definition"></a>创建帐龄期间定义
1. 转到 **导航窗格 > 模块 > 信用和收款 > 设置 > 帐龄期间定义**。
2. 单击 **新建**。
3. 在 **帐龄期间定义** 字段中，输入一个值。
4. 在 **描述** 字段中，键入一个值。
5. 单击 **添加低于** 按钮插入新的帐龄期间。
6. 在 **期间** 字段中，输入在帐龄分析表中显示的描述。
7. 在 **单位** 字段中，输入一个数字。
8. 在 **间隔** 字段中，选择一个选项。 分类帐期间与您的分类帐日历期间匹配。 日、周、月、季度和年份定义日期类型的间隔范围。 根据是否为首个或最后期间，不限量选择前一期间之前或之后的所有交易记录。  
9. 在 **帐龄指示器** 字段中，选择一个选项。
10. 在网格顶部选择期间。 更新该描述以说明帐龄期间定义的最早期间。
11. 在 **期间** 字段中，输入帐龄期间的新描述。
12. 关闭该页面。

## <a name="age-the-balances"></a>设置余额帐龄
1. 转到 **贷记和收款 > 定期任务 > 帐龄客户余额**。
2. 在 **帐龄期间定义** 字段中，选择您要创建的帐龄期间定义。
    + 您可以获取每个帐龄期间定义的有效快照。  
    + 所有客户均按默认处理。 您可以使用此选择计算单一客户池。  
    + 从交易记录中选择您将用于帐龄的日期。  
    + 为帐龄选择“截止”日期。 默认日期为今天，但是如果您将此字段更改为选定的日期，您将能够选取您想要的日期。 对于批处理，请使用今天的日期。  
3. 扩大 **公司** 范围。 您可以选择加入到快照中的公司。 默认选择当前公司。
4. 单击 **确定** 处理该快照。 处理需要一些时间，因此请等待滑块消失并检查消息中心的消息。

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>查看“帐龄余额表”和“收款”页上的余额。
1. 转到 **贷记和收款 > 收款 > 帐龄余额**。 列表页显示客户的余额。 帐龄图标显示最早交易记录的帐龄期间。  
2. 选择一位有余额的客户。
3. 展开 **帐龄速见表** 区域，以查看帐龄余额。 速见表的帐龄期间定义取自参数中设定的默认帐龄期间。 您可以使用“收集”菜单进行更改。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]