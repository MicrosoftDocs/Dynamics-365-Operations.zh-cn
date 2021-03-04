---
title: 双写入货币数据类型迁移
description: 本主题介绍如何更改双写入支持的货币的小数位数。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 6a0f114bce6bdb7813c93e9441744d67cd043c30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683716"
---
# <a name="currency-data-type-migration-for-dual-write"></a>双写入货币数据类型迁移

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

您最多可以将货币值支持的小数位数增加到 10。 默认限制是四个小数位。 通过增加小数位数，可以帮助您防止在使用双写入同步数据时丢失数据。 小数位数的增加是一种选择更改。 要实现它，您必须寻求 Microsoft 的帮助。

更改小数位数的流程分为两个步骤：

1. 从 Microsoft 请求迁移。
2. 在 Dataverse 中更改小数位数。

Finance and Operations 应用和 Dataverse 必须在货币值中支持相同数量的小数位数。 否则，在应用之间同步此信息时，可能会发生数据丢失。 迁移流程将重新配置货币和汇率值的存储方式，但不会更改任何数据。 迁移完成后，可以增加币种代码和定价的小数位数，用户输入和查看的数据可以具有更高的小数精度。

迁移是可选的。 如果支持更多小数位可能对您有好处，建议您考虑迁移。 不需要四位以上小数位的值的组织不必迁移。

## <a name="requesting-migration-from-microsoft"></a>从 Microsoft 请求迁移

Dataverse 中现有货币字段的存储无法支持超过四个小数位。 因此，在迁移流程中，货币值将被复制到数据库中的新内部字段。 此流程将持续进行，直到所有数据都已迁移。 在内部，在迁移结束时，新的存储类型将替换旧的存储类型，但是数据值不变。 然后，货币字段最多可以支持 10 个小数位。 在迁移流程中，Dataverse 可以继续使用而不会中断。

同时，汇率将修改，使其支持最多 12 个小数位，而不是当前的 10 个限制。 此更改是必需的，以使 Finance and Operations 应用和 Dataverse 中的小数位数相同。

迁移不会更改任何数据。 货币和汇率字段转换后，管理员可以通过指定每种交易货币和定价的小数位数来配置系统以最多为货币字段使用 10 个小数位。

### <a name="request-a-migration"></a>请求迁移

要使此功能可用，请发送电子邮件到 **CDSExpandDecimal@microsoft.com**，并包含以下信息：

+ **主题：** 请求为 \<organizationID\> 启用扩展的十进制支持
+ **正文：** 我想要为我的组织 \<organizationID\> 启用扩展的十进制支持。

Microsoft 代表将在两到三个工作日内与您联系以完成后续步骤。

当您请求迁移时，您应该了解以下详细信息并相应地进行计划：

+ 迁移数据所需的时间取决于系统中的数据量。 大型数据库的迁移可能需要几天时间。
+ 在迁移运行时，数据库的大小会临时增加，因为索引需要更多空间。 迁移完成后，大多数增加的空间将被释放。
+ 在迁移流程中，如果发生妨碍迁移完成的错误，系统会向 Microsoft 支持部门发出警报，以便支持人员可以进行干预。 但是，即使在迁移过程中发生错误，Dataverse 仍然可以正常使用。
+ 迁移流程是不可逆的。

## <a name="changing-the-number-of-decimal-places"></a>更改小数位数

迁移完成后，Dataverse 可以存储具有更多小数位的数字。 管理员可以选择用于特定币种代码和定价的小数位数。 然后，Microsoft Power Apps、Power BI 和 Power Automate 的用户可以查看和使用具有更多小数位的数字。

要进行此更改，您必须在 Power Apps 中更新以下设置：

+ **系统设置：定价的货币精度** – **设置用于整个系统定价的货币精度** 字段定义当选择 **定价精度** 时货币在组织中的行为方式。
+ **业务管理：货币** – **货币精度** 字段可让您指定特定货币的自定义小数位数。 组织范围的设置可以回退。

存在一些限制：

+ 您无法在实体上配置货币字段。
+ 您只能在 **定价** 和 **交易货币** 级别指定四个以上的小数位。

### <a name="system-settings-currency-precision-for-pricing"></a>系统设置：定价的货币精度

迁移完成后，管理员可以设置货币精度。 转到 **设置 \> 管理**，然后选择 **系统设置**。 然后，在 **常规** 选项卡上，更改 **设置用于整个系统定价的货币精度** 字段的值，如下图所示。

![货币的系统设置](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>业务管理：货币

如果您需要特定货币的货币精度与用于定价的货币精度不同，可以对其进行更改。 转到 **设置 \> 业务管理**，选择 **货币**，然后选择要更改的货币。 然后，将 **货币精度** 字段设置为所需的小数位数，如下图所示。

![特定区域的货币设置](media/specific-currency.png)

### <a name="tables-currency-field"></a>表：货币字段

可以为特定货币字段配置的小数位数限制为四个。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]