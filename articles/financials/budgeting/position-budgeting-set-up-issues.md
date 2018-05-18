---
title: "职位预算编制疑难解答"
description: "本文提供对配置职位预算时可能有的问题的解答。 其定位关于如何创建预算成本要素、薪酬组和薪酬网格的常见问题。"
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f2ef04008a5e6339a2193f9fcc77f2e0e6643557
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="position-budgeting-troubleshooting"></a>职位预算编制疑难解答

[!include [banner](../includes/banner.md)]

本文提供对配置职位预算时可能有的问题的解答。 其定位关于如何创建预算成本要素、薪酬组和薪酬网格的常见问题。 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>为什么找不到人力资源中的预测职位页？
---------------------------------------------------------------

预测职位已移动到“预算”。

## <a name="why-cant-i-delete-a-budget-cost-element"></a>为什么无法删除预算成本要素？
您不能删除分配给预测职位的预算成本要素。 您必须从所有预测职位中移除预算成本元素，然后才可将其删除。 **提示：**若要查找预算成本分配到的所有职位，请在**预算成本元素**页上选择成本元素，然后单击**更新职位**。 上部网格中列出使用成本要素的职位。

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>我如何在不打开每个职位的情况下从多个预测职位中删除成本元素？
您不能删除成本元素。 但是如果您更改开始日期和结束日期，以便这些日期在预算计划周期日期之外，成本元素将不再分配给该预算预测计划周期中的预测职位。 若要进行此更改，打开预算成本元素，然后在**成本计算**快速选项卡上，单击**更改日期**，然后更改生效日期或到期日期。 然后单击**确定**自动更新成本元素分配到的所有预测职位。 **提示：**如果您使用此方法，请注意其将从该开始日期和结束日期不再在相应范围内的**所有**预测职位中删除预算成本元素。 如果这不是您期望的效果，则必须打开每个希望从中删除预算成本元素的预测职位，并手动进行更改。

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>为什么在预算成本元素的“成本计算”快速选项卡中无法输入年度金额？
如果**计算基础**快速选项卡上有预算成本元素，则您不能输入年度金额，因为，系统需要百分比来计算该值。 若要更改此值，从**计算基础**快速选项卡删除所有预算成本元素。

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>为什么不能将预算成本类型从收入更改为其他预算成本类型？
某些预算成本要素使用收入成本要素作为计算基础。 若要更改**预算成本类型**字段，从所有预算成本元素的**计算基础**快速选项卡删除收入成本元素。

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>为什么无法更改某个预算成本要素的预算成本元素行上的日期？
当预测职位使用某个预算成本元素时，无法更改预算成本元素行中的日期。 此限制帮助确保预测职位始终在预算成本元素的准则内。 若要更改该日期，在**成本计算**快速选项卡上，单击**更改日期**并输入新日期。 然后单击**确定**更新成本元素分配到的职位。

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>为什么无法更改薪酬组页中的预算成本元素的成本？
您只可以在**预算成本元素**页上创建和更改预算成本元素。

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>当为预测职位的成本元素更改日期时为什么会收到错误消息？
预测职位成本要素行中的日期必须属于以下范围：

-   职位的激活和报废日期。
-   预算成本要素的激活日期和到期日期。
-   与预测职位的预算计划流程相关的预算周期的开始日期和结束日期。





