---
title: 使会计科目表分隔符的成为唯一的
description: 在 Dynamics 365 for Finance and Operations 中，科目表和维度值的分隔符不能相同。 必须在升级后更改分隔符值。
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559520"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>使会计科目表分隔符的成为唯一的

[!include [banner](../includes/banner.md)]

在 Microsoft Dynamics AX 2012 中，可为科目表和维度值使用相同分隔符。 在 Dynamics 365 for Finance and Operations 中，科目表和维度值的分隔符不能相同。 如果有相同分隔符，可在升级后更改。 

以下产品中有此功能：
- Dynamics 365 for Finance and Operations 版本 8.0
- Dynamics 365 for Finance and Operations 版本 7.1 KB 4094701：维度值中包含科目表分隔符时，不能输入财务维度
- Dynamics 365 for Finance and Operations 版本 7.2 KB 4092967：子项目格式中包含维度分隔符时，不能选择子项目作为维度

## <a name="update-delimiter"></a>更新分隔符
如果科目表存在冲突，则可更改科目表分隔符和项目/子项目 ID。 不能更改其他维度分隔符。 
- 升级到 Finance and Operations 之后，可在**总帐参数** > **会计科目表和维度** > **更改分隔符**中更改会计科目表分隔符。 
- 如果只有项目/子项目 ID 格式冲突，则可在**项目管理与核算参数** > **常规** > **修改子项目格式**中更改该值。 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>如何确定环境是否需要更新后的分隔符 
如果升级后的环境中的分隔符冲突，在细分条目控件或维度条目控件中输入值时，可能遇到不稳定。 这意味着输入科目和维度组合时，始终需要使用查找或弹出菜单。
