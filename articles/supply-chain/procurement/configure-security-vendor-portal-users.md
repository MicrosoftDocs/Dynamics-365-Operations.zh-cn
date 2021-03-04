---
title: 供应商门户用户安全性
description: 本文说明如何设置使用供应商门户的外部供应商的安全性。 此信息仅适用于 Dynamics AX 2016 年 2 月和 2016 年 5 月版本。
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72f353448f3b5d1f816bb240a230e26529c9cec3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423283"
---
# <a name="vendor-portal-user-security"></a>供应商门户用户安全

[!include [banner](../includes/banner.md)]

本文说明如何设置使用供应商门户的外部供应商的安全性。 此信息仅适用于 Dynamics AX 2016 年 2 月和 2016 年 5 月版本。

在 Dynamics 365 for Operations 版本 1611 中，供应商门户功能被扩展的供应商协作功能所取代。 有关设置供应商协作安全性的详细信息，请参阅[设置和维护供应商协作](set-up-maintain-vendor-collaboration.md)。 供应商门户向外部供应商公开了有关采购订单 (PO) 的一组有限的信息。 请您务必在 Microsoft Dynamics AX 中为供应商门户正确设置用户权限，这样供应商就不会意外访问您 Dynamics AX 安装中的其他信息。 **重要信息：** 与其他用户不同，外部供应商不应具有 **系统用户** 角色。 **系统用户** 角色将授予对一组不适用于外部用户的特权的访问权限。

## <a name="setting-up-a-vendor-portal-user"></a>设置供应商门户用户
在为即将使用供应商门户的人创建用户帐户之前，您必须设置供应商以允许供应商门户协作。 在 **供应商** 页面的 **常规** 选项卡上，使用 **采购订单协作** 字段。 使用供应商门户的外部供应商必须具有以下设置：

-   供应商必须在 Dynamics AX 中的 **用户** 页面上注册一个 Microsoft Azure Active Directory (AAD) 用户帐户。
-   供应商必须具有 **供应商（外部）** 安全角色，而不是 **系统用户** 角色。 **注意：** 您在 Dynamics AX 中创建新用户帐户时，将自动授予 **系统用户** 角色。 因此，您必须删除该角色并确认收到的警告消息。
-   不应向供应商用户授予将 PO 表中的其他字段添加到他们的 PO 视图的权限。 在 **个性化** 选项卡上，在 **用户** 选项卡上，将用户的 **允许显式个性化设置** 选项设置为 **否**。
-   用户帐户必须与已注册的联系人相关联。 在 **用户** 页面上的 **名称** 字段中选择一个联系人。 您选择的人员应具有相关供应商的 **联系人** 角色。

如果同一个人需要访问多个供应商帐户（可能是不同的法人）的供应商门户，那么这个人的每一个用户帐户都必须与相同的已注册联系人相关联。 **供应商（外部）** 角色包括使用供应商门户中提供的功能所需的所有基本功能。 此设置有助于确保外部用户看到的用户界面仅集中于预期场景。

<a name="additional-resources"></a>其他资源
--------

[通过使用供应商门户与供应商协作](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]