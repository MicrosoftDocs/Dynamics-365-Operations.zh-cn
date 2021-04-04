---
title: ER 配置格式以执行盘点和合计（第 1 部分 - 创建格式）
description: 本主题介绍如何配置电子报告格式以基于已经生成的文本输出的数据执行盘点和合计。 （第 1 部分）
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 64bf9f48319029e835f9e3fe2b888625100cc408
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565134"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>ER 配置格式以执行盘点和合计（第 1 部分 - 创建格式）

[!include [banner](../../includes/banner.md)]

以下步骤介绍指定为系统管理或电子申报开发人员角色的用户如何配置电子申报 (ER) 格式，以便基于已生成的文本输出的数据执行盘点和合计。 这些步骤可以在任何公司执行。

为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。

此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>访问 Microsoft 提供的配置列表
1. 转到“组织管理”>“工作区”>“电子申报”。
    * 确保“Litware 公司” 提供程序可用且标记为有效。  
2. 选择“Litware 公司” 提供程序。
3. 单击“存储库”。
    * 如果已存在“运营资源”的存储库，请跳过当前子任务的其余步骤。  
4. 单击“添加”以打开下拉对话框。
5. 在“配置存储库类型”字段中，输入“运营资源”。
6. 单击“创建存储库”。
7. 单击“确定”。

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>获取 Microsoft 提供的内部统计配置
1. 单击“打开”。
2. 在树中，选择“内部统计模型\内部统计 (DE)”。
3. 单击“导入”。
    * 单击所选配置的版本 1.1 的“导入”。  
4. 单击“是”。
5. 关闭该页面。
6. 关闭该页面。
7. 单击“申报配置”。
8. 在树中，展开“内部统计模型”。
9. 在树中，选择“内部统计模型\内部统计 (DE)”。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]