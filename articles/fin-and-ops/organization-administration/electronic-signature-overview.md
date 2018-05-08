---
title: "电子签名概览"
description: "本文提供电子签名的概览并说明如何在 Microsoft Dynamics 365 for Finance and Operations 中使用它们。"
author: maertenm
manager: AnnBe
ms.date: 08/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 698b938e515ff4755c2f111279cda244577ac9f3
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="electronic-signature-overview"></a>电子签名概览

[!include [banner](../includes/banner.md)]

本文提供电子签名的概览并说明如何在 Microsoft Dynamics 365 for Finance and Operations 中使用它们。

<a name="what-is-an-electronic-signature"></a>什么是电子签名？
--------------------------------

电子签名确认要启动或审核计算流程的人员的身份。 在一些行业中，电子签名与手写签名在法律上具有相同效力。 

电子签名是一些受管制行业（如制药业、食品和饮料业以及航空和国防）的法规遵从性要求。 它们也是遵循 21 CFR 第 11 部分（由美国食品和药品管理局颁发）中的法规所必需的。 

**注意：**电子签名本身与数字签名不同。 电子签名只是手写签名的替代品，而数字签名还提供其他安全措施。 数字签名可以帮助标识其他用户或进程是否篡改了数据。 还可以验证数字签名，并且用于对数据签名的证书所有者不能驳倒此验证。 如下所述，Microsoft Dynamics 365 for Finance and Operations 中的电子签名具有内置数字签名功能。

## <a name="electronic-signatures-in-dynamics-365-for-finance-and-operations"></a>Dynamics 365 for Finance and Operations 中的电子签名
在 Finance and Operations 中，可以对关键业务流程使用电子签名。 一些流程具有内置电子签名功能。 还可以为任意数据库表和字段创建自定义签名要求。 

电子签名具有内置数字签名功能。 对文档签名的每个用户必须获取有效的加密证书。 对文档签名时，与此证书相关的私钥进行验证。 Finance and Operations 在日志中记录电子签名信息以提供审计线索。 若要设置电子签名，请参阅[设置电子签名（任务指南）](tasks/set-up-electronic-signatures.md)。

## <a name="users-who-require-access-to-electronic-signatures"></a>需要访问电子签名的用户
以下三类用户通常要求电子签名的安全访问权限：电子签名管理员、签名人和电子签名审计员。

### <a name="electronic-signature-administrator"></a>电子签名管理员

电子签名管理员设置签名要求、一般参数和审核人，并在无法验证签名时接收预警。 默认情况下，属于**信息技术经理**安全角色的用户有权管理电子签名。

### <a name="signer"></a>签名人

签名人为需要签名的文档和流程提供电子签名。 默认情况下，属于**系统用户**安全角色的用户有权对文档进行电子签名。 

**注意：**签名人可能需要其他权限才能被授权访问与将要签名的文档或流程有关的数据。 更改数据后必须为这些更改签名的用户必须具有更改数据的权限。 代表其他用户签名的用户可能不需要访问数据。 此类型的用户示例是为员工的更改签名的主管。

### <a name="electronic-signature-auditor"></a>电子签名审计员

电子签名审计员查看数据库日志和可从数据库日志得到的查看签名日志。 默认情况下，属于**信息技术经理**安全角色的用户有权审核电子签名。 

如果您使用一个角色，而不使用**信息技术经理**，请确保为该角色分配以下特权：

-   查看电子签名故障
-   查看数据库日志

## <a name="signing-documents-electronically"></a>对文档进行电子签名
### <a name="get-a-certificate"></a>获取证书

在 Finance and Operations 中对文档进行电子签名前，每个签名人必须申请证书。 

**注意：**Finance and Operations 使用 Microsoft SQL Server 功能来创建证书并允许进行电子签名。 不需要其他证书或公钥基础结构 (PKI)。 

申请证书时，会在 Finance and Operations 数据库中为您创建一个公钥和一个私钥。 私钥是通过使用只有您知道的密码进行加密。 当对文档进行电子签名时，通过输入密码来验证您的身份。 

要请求证书，在**选项**页，在**帐户**选项卡上，单击**获取证书**。 

您必须输入并确认您将用于签名的密码。 使用该密码来保护您的私钥并授权使用您的证书。 该密码不存储在数据库中，对于任何其他人（甚至 Finance and Operations 管理员）都不可用。 

如果您忘记与证书连接的密码，证书必须重置。 如果重置证书，您不会影响使用旧证书签名的文档。 若要重置证书，在**选项**页上，单击**重置证书**。

### <a name="sign-a-document-electronically"></a>对文档进行电子签名

执行需要电子签名的更改时，将显示**对文档签名**页。

1.  在**对文档签名**页，单击**文档**选项卡查看对文档的更改。
2.  在“**签名**”选项卡上，选择一个原因代码。
3.  输入注释，如果注释是必需的。
4.  如果您的用户 ID 未显示在**签名人**字段中，请在列表中选择它。
5.  输入您所在的位置，如果此信息是必需的。
6.  单击“**OK**”。

### <a name="sign-for-another-users-changes"></a>为其他用户的更改签名

有时您可能需要用户为其他用户的更改签名。 例如，可能要求主管为员工所做的物料清单 (BOM) 更改签名。 使用此过程可以将 Finance and Operations 用户指定为其他用户的签名人。 

**注意：**当某用户为其他用户的更改签名时，必须在执行更改的用户的工作站提供签名。 只有提供签名后，该用户才能保存更改。 

若要指定审核人，请执行以下步骤。

1.  在**选项**页，在**帐户**选项卡上，单击**指定审核人**。
2.  在**审核人用户 ID** 字段中，选择必须为其他用户的更改签名的用户的 ID。
3.  在**为其签名的用户 ID** 字段中，选择必须为其更改签名的用户的 ID。





