---
title: 创建和更新商店营业时间
description: 此主题介绍如何在商业总部中创建和更新商店营业时间。
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 96ae5f33b1ab5fda98da4fc48b1fb883ca4d54b8
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024470"
---
# <a name="create-and-update-store-hours"></a>创建和更新商店营业时间

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>概览

零售商可以从一个位置为不同地理区域的不同商店创建、维护和管理商店营业时间。 然后可以在销售点 (POS) 终端显示商店营业时间。 通过这种方法，收银员可以与客户共享商店营业时间，并更好地帮助对其他商店库存感兴趣的购物者。 也可以将商店营业时间打印到收银条上，以防客户希望以后再来商店。

可以为不同渠道配置多个商店营业时间。 这些渠道包括实体商店、呼叫中心、移动设备和电子商务网站。

如果客户有其他商店的提货单，收银员可以选择该商店的可提货日期。 商店查找将提供对日期和商店营业时间的引用。 收银员可选择日期和位置，还可以打印其中包括商店营业时间的提货收据。

Microsoft Dynamics 365 Retail 版本 8.1.2 及更高版本中提供此功能。

## <a name="configure-store-hours"></a>配置商店营业时间

请执行以下步骤配置商店营业时间。

1. 转到 **Retail 和 Commerce** \> **渠道设置** \> **商店营业时间**。
2. 选择**新建**以创建新的商店营业时间模板。 若要使用现有模板，请在左窗格中选择模板。
3. 在**添加范围**对话框中，定义所需日期范围、商店营业时间和任何节假日。

    - 如果商店营业时间不会改变，请在**结束日期**字段中选择**一直持续**。
    - 如果商店营业时间适用于特定月份、周或日期，请在**开始日期**和**结束日期**字段中设置相应日期。

    > [!NOTE]
    > 可创建开始和结束日期重合的多个模板。 因此，可以执行为不同时区的商店定义商店营业时间之类操作。

    ![“添加范围”对话框](../dev-itpro/media/Storehours1.png "“添加范围”对话框")

4. 将商店营业时间模板与其使用商店关联。 在**选择组织节点**对话框中，选择应与模板关联的商店、地区和组织。

    - 只能为每个商店关联一个商店营业时间模板。
    - 使用箭头按钮选择商店、地区或组织。 商店或商店组可使用日历，POS 中将显示日历供参考。

    ![选择组织节点对话框](../dev-itpro/media/Storehours2.png "选择组织节点对话框")

5. 在**配送计划**页中，运行 **1070** 和 **1090** 作业以便将商店营业时间提供给 POS。

## <a name="add-store-hours-to-printed-receipts"></a>向纸质收银条添加商店营业时间

执行以下步骤向纸质 POS 收银条添加商店营业时间。

1. 打开收银条设计器。
2. 在左下角选择**页脚**。
3. 将**商店营业时间**元素从左窗格拖到收银条模板底部的页脚。
4. 可根据需要编辑**商店营业时间**元素上的默认标签。
5. 保存收银条，然后关闭收银条设计器。
6. 在**配送计划**页上，运行 **1070** 和 **1090** 作业。
7. 登录到 POS。
8. 完成一笔交易，然后选择打印收银条。

POS 收银条中现在包含商店营业时间。 如果模板中包含任何节假日，将在收银条中显示这些节假日。

![收据示例](../dev-itpro/media/Storehours3.png "收据示例")
