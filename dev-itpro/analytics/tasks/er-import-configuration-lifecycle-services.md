--- 
title: "针对电子申报 (ER) 从 Lifecycle Services 导入配置"
description: "以下步骤说明系统管理员或电子报表开发人员角色的用户可如何从 Microsoft Lifecycle Services (LCS) 导入新电子申报 (ER) 配置版本。"
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ab453d3ee44e206aea148de8dc3b428dc5056576
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a>针对电子申报 (ER) 从 Lifecycle Services 导入配置

[!include[task guide banner](../../includes/task-guide-banner.md)]

以下步骤说明系统管理员或电子报表开发人员角色的用户可如何从 Microsoft Lifecycle Services (LCS) 导入新电子申报 (ER) 配置版本。

在此示例中，您将为示例公司 Litware 公司选择所需的 ER 配置版本并将其导入。这些步骤适用于所有公司，因为这些公司共享 ER 配置。 为了完成这些步骤，您必须首先完成“将 ER 配置上载到 Lifecycle Services”这一过程中的步骤。 完成这些步骤还需要能够访问 LCS。

1. 转到“组织管理”>“工作区”>“电子申报”。
2. 单击“配置”。

## <a name="delete-a-shared-version-of-data-model-configuration"></a>删除数据模型配置的共享版本
1. 在树结构中，选择“示例模型配置”。
    * 在“将 ER 配置上载到 Lifecycle Services”过程中，示例数据模型配置的第一个版本已创建并发布到 LCS。 在此过程中，您将删除 ER 配置的这一版本。 此示例数据模型配置版本以后将从 LCS 导入。  
2. 在列表中，找到并选择所需记录。
    * 选择状态不为“已共享”的此配置的版本。 此状态指示配置已发布到为 LCS。  
3. 单击“更改状态”。
4. 单击“中断”。
    * 将所选版本的状态从“已共享”更改为“已中断”以使它可删除。  
5. 单击“确定”。
6. 在列表中，找到并选择所需记录。
    * 选择状态为“已中断”的此配置的版本。  
7. 单击“删除”。
8. 单击“是”。
    * 请注意，仅所选数据模型配置的草稿版本 2 可用。  
9. 关闭该页面。

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>从 LCS 导入数据模型配置的共享版本
1. 在列表中，标记所选的行。
    * 打开‘Litware 公司’ 配置提供程序的存储库列表。  
2. 单击“存储库”。
3. 单击“打开”。
    * 选择 LCS 存储库然后打开它。  
4. 在列表中，标记所选的行。
    * 选择版本列表中“示例模型配置”的第一个版本。  
5. 单击“导入”。
6. 单击“是”。
    * 确认将所选版本从 LCS 导入。  
    * 请注意，信息消息（在窗体上方）确认所选版本导入的成功完成。  
7. 关闭该页面。
8. 关闭该页面。
9. 单击“配置”。
10. 在树结构中，选择“示例模型配置”。
11. 在列表中，找到并选择所需记录。
    * 选择状态为“已共享”的此配置的版本。  
    * 请注意，所选数据模型配置的共享版本 1 现在也可用。  


