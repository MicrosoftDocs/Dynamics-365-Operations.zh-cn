---
title: 设置销售订单状态字段的映射
description: 本主题说明如何为双写入设置销售订单状态字段。
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: dce4b6310e2f6d31a115302efa7fbc132799e48f
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829277"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a>设置销售订单状态字段的映射

[!include [banner](../../includes/banner.md)]

指示销售订单状态的字段在 Microsoft Dynamics 365 Supply Chain Management 和 Dynamics 365 Sales 中具有不同的枚举值。 采用双写入映射这些字段需要进行其他设置。

## <a name="fields-in-supply-chain-management"></a>Supply Chain Management 中的字段

在 Supply Chain Management 中，两个字段反映销售订单的状态。 您必须映射的字段是**状态**和**文档状态**。

**状态**枚举指定订单的整体状态。 此状态显示在订单标题上。

**状态**枚举具有以下值：

- 未结订单
- 已交货
- 已开单
- 已取消

**文档状态**枚举指定为订单生成的最新文档。 例如，如果订单已确认，此文档为销售订单确认。 如果销售订单已部分开票，然后确认其余行，文档状态仍为**发票**，因为发票是在流程后期生成的。

**文档状态**枚举具有以下值：

- 确认单
- 领料单
- 装箱单
- 账单

## <a name="fields-in-sales"></a>Sales 中的字段

在 Sales 中，两个字段指示订单的状态。 您必须映射的字段是**状态**和**处理状态**。

**状态**枚举指定订单的整体状态。 它具有以下值：

- 在职
- 提交日期
- 已履行
- 已开单
- 已取消

引入了**处理状态**枚举，以便可以通过 Supply Chain Management 更准确地映射状态。

下表显示了 Supply Chain Management 中**处理状态**的映射。

| 处理状态   | Supply Chain Management 中的状态 | Supply Chain Management 中的文档状态 |
|---------------------|-----------------------------------|--------------------------------------------|
| 在职              | 未结订单                        | None                                       |
| 已确认           | 未结订单                        | 确认单                               |
| 已领料              | 未结订单                        | 领料单                               |
| 已部分交货 | 未结订单                        | 装箱单                               |
| 已交货           | 已交货                         | 装箱单                               |
| 已部分开票  | 已交货                         | 账单                                    |
| 已开单            | 已开单                          | 账单                                    |
| 已取消           | 已取消                         | 不适用                             |

下表显示了 Sales 与 Supply Chain Management 之间的**处理状态**的映射。

| 处理状态   | Sales 中的状态 | Supply Chain Management 中的状态 |
|---------------------|-----------------|-----------------------------------|
| 在职              | 在职          | 未结订单                        |
| 已确认           | 提交日期       | 未结订单                        |
| 已领料              | 提交日期       | 未结订单                        |
| 已部分交货 | 在职          | 未结订单                        |
| 已部分开票  | 在职          | 未结订单                        |
| 已部分开票  | 已履行       | 已交货                         |
| 已开单            | 已开单        | 已开单                          |
| 已取消           | 已取消       | 已取消                         |

## <a name="setup"></a>设置

要为销售订单状态字段设置映射，必须启用 **IsSOPIntegrationEnabled** 和 **isIntegrationUser** 属性。

要启用 **IsSOPIntegrationEnabled** 属性，请按照下列步骤操作。

1. 在浏览器中，转到 `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`。 将 **\<test-name\>** 替换为您公司的 Sales 链接。
2. 在打开的页面上，找到 **organizationid**，记下值。

    ![查找 organizationid](media/sales-map-orgid.png)

3. 在 Sales 中，打开浏览器控制台，运行以下脚本。 使用步骤 2中的 **organizationid** 值。

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![浏览器控制台中的 JavaScript 代码](media/sales-map-script.png)

4. 确认 **IsSOPIntegrationEnabled** 已设置为 **true**。 使用步骤 1 中的 URL 检查此值。

    ![IsSOPIntegrationEnabled 设置为 true](media/sales-map-integration-enabled.png)

要启用 **isIntegrationUser** 属性，请按照下列步骤操作。

1. 在 Sales 中，转到**设置 \> 自定义 \> 自定义系统**，选择**用户实体**，然后打开**窗体 \> 用户**。

    ![打开用户窗体](media/sales-map-user.png)

2. 在字段资源管理器中，找到**集成用户模式**，然后双击它将它添加到窗体中。 保存所做的更改。

    ![将“集成用户模式”字段添加到窗体](media/sales-map-field-explorer.png)

3. 在 Sales 中，转到**设置 \> 安全 \> 用户**，将视图从**已启用用户**更改为**应用程序用户**。

    ![将视图从“已启用用户”更改为“应用程序用户”](media/sales-map-enabled-users.png)

4. 选择 **DualWrite IntegrationUser** 的两个条目。

    ![应用程序用户列表](media/sales-map-user-mode.png)

5. 将**集成用户模式**字段的值更改为**是**。

    ![更改“集成用户模式”字段的值](media/sales-map-user-mode-yes.png)

现在，您的销售订单已映射。