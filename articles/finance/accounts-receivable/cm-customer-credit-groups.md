---
title: 客户信用组
description: 本主题提供有关客户信用组的信息。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7121b78f3318bae9f82b2f0f951bc7bfe6c4358
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015131"
---
# <a name="customer-credit-groups"></a>客户信用组

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

您可以定义具有相同信用额度的客户组。 还考虑了在客户发票帐户上定义的个人信用额度。

可以从不同的法人中选择客户信用组的成员。 当您将一个客户添加到客户信用组中的客户列表时，每个客户的信用额度的到期日期将更改为分配给该组的到期日期。

您可以在**客户信用组**页（**信用管理 \> 客户信用组 \> 客户信用组**）上设置客户信用组。

1. 在**组号**和**描述**字段中，输入组的标识符和描述。
2. 在**信用额度**和**货币**字段中，输入系统检查组中任何成员的信用额度时应使用的信用额度和货币。
3. 在**信用额度结束日期**字段中，输入信用额度的到期日期。 客户信用组必须具有到期日期。

设置完客户信用组后，您可以通过指定其法人和客户帐户 ID 将客户添加到该组中。 当您将新客户添加到客户信用组时，系统会在所有法人中搜索相同的客户帐户，并提示您将其添加到客户信用组中。

使用**帐龄余额**菜单查看客户信用组中所有发票客户的帐龄余额详细信息。 **帐龄余额**页显示了发票客户帐户的帐龄余额摘要。
