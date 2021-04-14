---
title: 从 Azure Active Directory 导入用户
description: 系统管理员可通过此过程从 Azure Active Directory 手动导入所选用户或导入大量用户。
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9f03ae7197790c1aac6ebf3cb94ff7963b1291e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745781"
---
# <a name="import-users-from-azure-active-directory"></a>从 Azure Active Directory 导入用户

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>导入所选用户

系统管理员可通过此过程从 Azure Active Directory (Azure AD) 导入所选用户。

1. 将使用当前会话公司作为默认公司导入用户。 导入用户之前，请更改当前公司（如果适用）。
2. 转到 **系统管理 > 用户 > 用户**。
3. 单击 **导入用户**。
4. 选择应导入的用户，然后选择 **导入用户**。

导入完成后，将需要为用户分配角色。

## <a name="import-users-in-bulk"></a>批量导入用户

系统管理员可通过此过程从 Azure Active Directory 导入大量用户。
请注意，使用“批量导入”选项时不能选择用户。

## <a name="run-the-import-as-a-batch-job"></a>将导入作为批处理作业运行
1. 将使用当前会话公司作为默认公司导入用户。 导入用户之前，请更改当前公司（如果适用）。
2. 转到 **系统管理 > 用户 > 用户**。
3. 单击 **批量导入**。
4. 展开 **后台运行** 部分。
4. 在 **批处理** 字段中选择 **是**。
6. 在 **批处理组** 字段中，输入或选择一个值。 这是可选步骤。  
7. 在 **专用** 字段中选择 **是**。 这是可选步骤。  
8. 在 **关键作业** 字段中，选择 **是**。 这是可选步骤。  
9. 在 **监视类别** 字段中，选择一个选项。
10. 单击 **确定**。

导入完成后，将需要为用户分配角色。

## <a name="run-in-a-sandbox-environment"></a>在沙盒环境中运行
1. 选择 **批量导入**。
2. 选择 **确定**。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]