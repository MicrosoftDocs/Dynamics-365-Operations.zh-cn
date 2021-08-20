---
title: 设置原因代码
description: Dynamics 365 Human Resources 使用原因代码来解释为什么员工的福利正在更改。
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bd7c5a35a6d4b40eb376eee2580af681f7bfd7f8f93aab8aad67f238fc40470b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732673"
---
# <a name="set-up-reason-codes"></a>设置原因代码

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources 使用原因代码来解释为什么员工的福利正在更改。

> [!NOTE]
> 自 2021 年 1 月起，原因代码将迁移到 **人事管理** 工作区，而不是 **福利管理** 工作区。 有关详细信息，请参阅[将原因代码手动迁移到“人事管理”](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management)。

## <a name="create-reason-codes"></a>创建原因代码

1. 在 **人事管理** 工作区（或 **福利管理** 工作区(如果您的原因代码尚未迁移)），选择 **链接**，然后选择 **原因代码**。

2. 选择 **新建**。

3. 为以下字段指定值：

   | 字段 | 说明 |
   | --- | --- |
   | **原因代码** | 用于标识员工更改福利计划登记的原因的唯一名称。 |
   | **说明** | 原因代码的描述。 |

4. 在 **适用场景** 下，将 **福利管理** 设置为 **是**。 （如果原因代码尚未迁移到 **人事管理** 工作区则不适用。）

5. 选择 **保存**。

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>将原因代码手动迁移到“人事管理”

2021 年 1 月，原因代码将迁移到 **人事管理** 工作区，而不是 **福利管理** 工作区。 大部分原因代码数据将在您的环境中自动迁移。 部分原因代码数据可能无法迁移。 例如，原因码现在最多包含 15 个字符，因此任何长度超过 15 个字符的原因码都不会自动迁移。

您会在 **福利管理** 工作区的 **链接** 页上看到一个横幅，通知您有关迁移以及是否有任何原因代码未迁移的信息。

1. 选择 **原因代码** 了解有关迁移状态的详细信息。

   [![原因代码。](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. 选择迁移失败的原因代码。

   [![原因代码迁移状态。](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. 选择 **迁移原因代码**。

   [![迁移原因代码。](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. 在 **福利原因代码迁移** 窗格中，有两个用于映射到人事管理原因代码的选项：

   - 要在“人事管理”中使用现有原因代码，从 **使用现有原因代码** 下拉列表中选择一个。
     > [!NOTE]
     > 如果尚未将另一个福利管理原因代码迁移到“人事管理”，您只能在其中使用现有原因代码。
   - 要在“人事管理”中创建新的原因代码，在 **新建原因代码** 中输入新的原因代码，然后在 **新增描述** 中输入描述。

   [![映射到人事管理原因代码。](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

原因代码迁移到“人事管理”后，在“福利管理”中使用它们的选项将自动设置为 **是**。

[![在“福利管理”中使用原因代码。](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]