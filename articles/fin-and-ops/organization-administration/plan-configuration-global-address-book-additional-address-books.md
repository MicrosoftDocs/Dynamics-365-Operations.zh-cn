---
title: "计划如何配置全局通讯簿和附加通讯簿"
description: "本主题介绍您在 Microsoft Dynamics 365 for Finance and Operations 中设置和配置全球通讯簿和任何其他通讯簿前，在计划流程中的考虑事项和必须做的决定。 某些决策需要您确认已为产品的其他区域做出了决策，例如组织层次结构。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b872603f987b72faacc0a987aa44c31e773636f8
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a>计划如何配置全局通讯簿和附加通讯簿

[!include [banner](../includes/banner.md)]

本主题介绍您在 Microsoft Dynamics 365 for Finance and Operations 中设置和配置全球通讯簿和任何其他通讯簿前，在计划流程中的考虑事项和必须做的决定。 某些决策需要您确认已为产品的其他区域做出了决策，例如组织层次结构。

<a name="global-address-book"></a>全球通讯簿
-------------------

在您开始使用全球通讯簿前，必须确定其默认值。 然后这些默认值用于您创建的任何附加通讯簿。 

**决策：**

-   对于**“人员”**类型的当事方记录，名称应以何种顺序显示？ 例如一个顺序是姓氏、中间名、名字。
-   在删除角色记录时，是否应从通讯簿中删除当事方记录？ 例如，如果删除了客户记录，是否还应删除相应的当事方记录？
-   创建新记录时，如果在全球通讯簿中找到重复的记录，是否应通知用户？
-   是否应在当事方记录信息中包括数据统一编码系统 (DUNS) 编号？
-   如果 DUNS 编号包括在当事方记录中，是否应检查该编号的唯一性？
-   在全球通讯簿中创建当事方记录时，您是否需要默认当事方类型、人员或组织？
-   哪些用户角色应有权访问当事方记录的私人地址和联系信息？

## <a name="additional-address-books"></a>附加通讯簿
在创建全球通讯簿后，您可以根据需要在您的组织中创建附加通讯簿，如组织中每个公司一个单独的通讯簿或每个经营范围一个单独的通讯簿。 例如，Fabrikam 是一家具有多个公司和多个经营范围的国际组织。 Fabrikam 计划为每个经营范围创建通讯簿。 对于在多个位置出现的经营范围（如气动工具业务），Fabrikam 计划为每个位置创建一个通讯簿。 Fabrikam 的 IT 经理 Chris 创建了以下必需的通讯簿列表。 此列表中还描述每个通讯簿必须包括的当事方记录。

-   **公共部门合同 (PubSC)** – Fabrikam 持有的公共部门合同中涉及的所有当事方的当事方记录。
-   **私人部门合同 (PriSC)** – Fabrikam 持有的私营部门合同中涉及的所有当事方的当事方记录。
-   **电子工具 (ET)** – 电子工具采购或销售中涉及，或以其他方式与在 Fabrikam 日本公司中由 Fabrikam 提供的电子工具或为其购买的电子工具交互的所有当事方的当事方记录。
-   **气动工具 (PTJPN)** – 气动工具采购或销售中涉及，或以其他方式与在 Fabrikam 日本公司中由 Fabrikam 提供的气动工具或为其购买的气动工具交互的所有当事方的当事方记录。
-   **气动工具 (PTUSA)** – 气动工具采购或销售中涉及，或以其他方式与在 Fabrikam 美国公司中由 Fabrikam 提供的气动工具或为其购买的气动工具交互的所有当事方的当事方记录。

**决策：**

-   您要创建多少附加通讯簿？

### <a name="address-book-security"></a>通讯簿安全性

您可以随时创建通讯簿，您还可以随时为通讯簿设置安全参数。 为通讯簿设置安全权限并非必需操作，但如果您未设置，则您的组织中的所有工作人员可以查看该通讯簿中的所有当事方记录。 您可以通过通讯簿设置当事方记录的安全权限： 安全权限基于团队。 此方法可保证，仅分配至有权访问通讯簿的团队的工作人员才可以查看该通讯簿中的当事方记录。 您必须选择有权访问每个通讯簿的团队。 对于每个通讯簿，您可以设置允许或拒绝访问特定团队的安全权限。 如果您授予团队通讯簿权限，则该团队的所有成员都可以查看通讯簿中的记录。 如果您不授予对通讯簿的团队访问权限，则该团队的成员不能查看通讯簿或其内容。 

**决策：**

-   哪些团队应有权访问您要创建的每个新通讯簿？





