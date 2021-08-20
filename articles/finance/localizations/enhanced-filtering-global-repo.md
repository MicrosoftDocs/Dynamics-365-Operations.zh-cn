---
title: RCS/全局知识库中的 RCS 增强筛选
description: 此主题介绍 RCS 全局知识库的增强筛选功能，已经改进了这些功能，以便包含更多筛选器。
author: JaneA07
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2def3b653ac7c90318feb696c0dd197217ac29f64f0f08d26a7069918c67922b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778104"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>RCS 增强筛选选项，用于在 RCS/全局知识库中查找配置

[!include [banner](../includes/banner.md)]

此主题介绍 Regulatory Configuration Service (RCS) 全局知识库的增强筛选功能，经过改进，包括了具有以下条件的筛选功能： 
- **国家/地区** - 基于 ISO 国家/地区代码  
- 以下 **标记** 类型：
  - 功能区域
  - 特征区域
  - 行业 
  - 业务文档 

为了更容易发现特定或相关的配置，您可以单独或成组应用筛选器。 例如，要查找与供应商发票相关的单一类型的“可配置业务文档”，可以应用 **业务文档类型** 筛选器来搜索该类型的文档。 

[![全局存储库的“筛选器”部分。](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

您可以通过选择文档类型（例如，“供应商发票”）并单击 **应用筛选器** 来进一步细化搜索。 以下示例显示基于添加了文档类型的 **业务文档类型** 进行筛选时的结果。 

[![为业务文档类型应用的筛选器和导入。](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

可以将筛选结果单独或作为一组导入到用户 RCS 存储库或 Dynamics 365 Finance 环境中。 为此，请选择配置组，然后单击 **导入**。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]