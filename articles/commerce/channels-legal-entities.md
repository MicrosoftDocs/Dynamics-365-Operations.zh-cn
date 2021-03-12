---
title: 创建法人
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建法人，必须在创建渠道之前创建和配置法人。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9491feb004366a02155225bfb323773e130f3dc9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993595"
---
# <a name="create-legal-entities"></a>创建法人


[!include [banner](includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建法人，必须在创建渠道之前创建和配置法人。

## <a name="overview"></a>概览

法人是具有已登记的或法律允许的法律结构的组织。 法人可以输入到法律合同，并需要准备报告它们的业绩的报表。

公司是法人的一种类型。 现在，公司只能是您能创建的这类法人，每个法人与公司 ID 相关联。 因为程序中的某些功能区域在它们的数据模型中使用了公司 ID 或 *DataAreaId*，所以此关联存在。 在这些功能区域中，公司用作了数据安全性的边界。 用户只能访问他们当前登录到的公司的数据。 

创建渠道时，必须指定该渠道所属的法人。

## <a name="create-a-new-legal-entity"></a>创建新法人

若要在 Dynamics 365 Commerce 中创建新法人，请按以下步骤进行操作。

1. 在导航窗格中，转到 **模块 \> 总部设置 \> 法人**。
1. 在操作窗格上，选择 **新建**。 **新法人** 窗格会出现在右侧。
1. 在 **名称** 字段中，输入一个值。
1. 在 **公司** 字段中，输入一个值。
1. 在 **国家/地区** 字段中，输入或选择一个值。
1. 选择 **确定**。 

   ![法人创建](media/legal-entities.png)

1. 在 **常规** 部分中，请提供有关法人的以下一般信息： 
   1. 如果需要搜索名称，请输入搜索名称。 搜索名称是可用于搜索此法人的替代名称。 
   1. 选择此法人是否被用作合并公司。
   1. 选择此法人是否被用作清除公司。 
   1. 选择实体的 **默认语言**。 
   1. 为该实体选择 **时区**。
1. 在 **地址** 部分，选择 **编辑** 以输入街道名称和门牌号、邮政编码和城市之类的地址信息。
1. 在 **联系人信息** 部分，输入有关通信方法的信息，如电子邮件地址、URL 和电话号码。
1. 在 **法定申报** 部分，输入法定申报的登记编号。
1. 在 **登记编号** 部分，输入法人所需的所有信息。
1. 在 **银行帐户信息** 部分，输入法人的银行帐户和银行代号。
1. 在 **外贸和物流** 部分，输入法人的装运信息。
1. 在 **编号规则** 部分，您可以查看与法人关联的编号规则。 开始时将是空的。
1. 在 **仪表板图像** 部分，查看或更改与法人关联的徽标和仪表板图像。
1. 在 **税务登记** 部分，输入用于向税务主管机构申报的登记编号。
1. 在 **1099 税** 部分，输入法人的 1099 信息。
1. 在 **税务信息** 部分，输入法人税务信息。
1. 选择 **保存**。

下图显示了示例法人的详细信息。

![法人常规部分](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>其他资源

[组织和组织层次结构概览](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[规划组织层次结构](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[组织层次结构](channels-org-hierarchies.md)

[渠道概览](channels-overview.md)

[渠道设置先决条件](channels-prerequisites.md)
