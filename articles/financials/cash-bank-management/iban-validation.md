---
title: "管理国际银行帐号 (IBAN) 帐户验证"
description: "此主题介绍如何管理国际银行帐号 (IBAN) 帐户验证。"
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: zh-cn
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>管理国际银行帐号 (IBAN) 帐户验证

[!include [banner](../includes/banner.md)]

验证国际银行帐号 (IBAN) 帐户可以增加在向银行帐户添加 IBAN 时完成的验证量。

IBAN 的结构存储在 Microsoft Dynamics 365 for Finance and Operation 中，在你首次对银行帐户使用 IBAN 时自动加载。 银行帐号是为 IBAN 号定义的结构的一部分。 根据该结构，如果 IBAN 中帐号的位置和长度与每个国家或地区的结构中定义的位置不匹配，将收到警告消息。

## <a name="set-up-iban-structures"></a>设置 IBAN 结构

1. 转到**现金和银行管理 \> 设置 \> IBAN 结构**。
2. 请注意，已自动设置了每个国家或地区的 IBAN 结构。
3. 如果必须自定义特定国家或地区的结构，可以进行编辑。
4. 每个新发行版中都有结构定义。 每次更新之后，可使用**重置结构**菜单加载最新定义。

## <a name="validate-the-iban-structure-in-a-bank-account"></a>验证银行帐户中的 IBAN 结构

1. 转至**现金和银行管理 \> 银行帐户 \> 银行帐户**。
2. 创建银行帐户。
3. 在**附加信息**快速选项卡上，输入一个 IBAN。

    如果 IBAN 中帐号的位置和长度与每个国家或地区的结构中定义的位置不匹配，将收到消息。 如果 IBAN 的长度与 IBAN 结构中的长度不匹配，则不能继续操作。

    此项验证还会验证银行帐号是否与表示银行帐号的 IBAN 部分匹配。 如果银行帐号不匹配，将收到警告消息。 此消息只是警告。 即使银行帐号不匹配，也可以继续操作。

