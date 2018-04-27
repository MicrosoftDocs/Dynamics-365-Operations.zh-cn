---
title: "将 Field Service 中的协议发票同步到 Finance and Operations 中的普通发票"
description: "本主题讨论用于将 Microsoft Dynamics 365 for Field Service 中的协议发票同步到 Microsoft Dynamics 365 for Finance and Operations 中的普通发票的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: zh-cn
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>将 Field Service 中的协议发票同步到 Finance and Operations 中的普通发票

[!include[banner](../includes/banner.md)]

本主题讨论用于将 Microsoft Dynamics 365 for Field Service 中的协议发票同步到 Microsoft Dynamics 365 for Finance and Operations 中的普通发票的模板和基础任务。

## <a name="templates-and-tasks"></a>模板和任务

以下模板和基础任务用于运行从 Field Service 中的协议发票到 Finance and Operations 中的普通发票的同步。

**数据集成中的模板名称：**

- 协议发票（Field Service 到 Fin and Ops）

**数据集成项目中的任务名称：**

- 发票抬头
- 发票行

在发生协议发票同步前，需要执行以下同步任务：

- 科目（Sales 到 Fin and Ops）– 直接

## <a name="entity-set"></a>实体集

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| 发票       | CDS 客户普通发票抬头 |
| invoicedetails | CDS 客户普通发票行   |

## <a name="entity-flow"></a>实体流

可通过 Common Data Service (CDS) 数据集成项目将 Field Service 中从协议创建的发票同步到 Finance and Operations。 对这些发票的更新将同步到 Finance and Operations 中的普通发票，前提是这些普通发票的会计状态为**进行中**。 在 Finance and Operations 中过帐了普通发票并且会计状态更新为**已完成**之后，将不再可以从 Field Service 同步更新。

## <a name="field-service-crm-solution"></a>Field Service CRM 解决方案

已向**发票**实体添加了**具有带协议来源的行**字段。 此字段帮助确保仅同步从协议创建的发票。 如果发票中至少包含一个源自协议的发票行，则该值为 **true**。

已向**发票行**实体添加了**具有协议来源**字段。 此字段帮助确保仅同步从协议创建的发票行。 如果发票行源自协议，则该值为 **true**。

**发票日期**是 Finance and Operations 中的必填字段。 因此，执行同步之前，Field Service 中的该字段必须有值。 为了满足此要求，添加了以下逻辑：

- 如果**发票**实体的**发票日期**字段为空（即无值），将把该字段设置为添加源自协议的发票时的当前日期。
- 用户可更改**发票日期**字段。 但是，用户尝试保存源自协议的发票时，如果发票的**发票日期**字段为空，将出现业务流程错误。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置

### <a name="in-finance-and-operations"></a>在 Finance and Operations 中

必须针对集成设置发票来源，以便区分 Finance and Operations 中创建自 Field Service 中的协议发票的普通发票。 如果发票的发票来源的类型为**协议发票集成**，则**销售发票**抬头中将显示**外部发票编号**字段。

除了在发票抬头中显示，还可以使用**外部发票编号**信息在将发票从 Finance and Operations 同步到 Field Service 期间帮助确保过滤掉创建自 Field Service 协议发票的发票。

1. 转至**应收帐款** \> **设置** \> **发票来源代码**。
2. 选择**新建**创建新的发票来源。
3. 在**发票来源**字段中，输入发票来源的名称，如**FS**。
4. 在**描述**字段中，输入描述，如 **Field Service 协议发票**。
5. 选中**来源类型分配**复选框。
6. 将**发票来源类型**字段设置为**协议发票集成**。
7. 选择**保存**。

### <a name="in-the-data-integration-project"></a>在数据集成项目中

任务：**发票行**  

确保 Finance and Operations 的**主科目显示值**字段的默认值更新为匹配所需值。

默认模板值为 **401100**。

