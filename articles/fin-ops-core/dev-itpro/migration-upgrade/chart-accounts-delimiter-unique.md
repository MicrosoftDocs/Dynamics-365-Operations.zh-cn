---
title: 设置唯一的会计科目表分隔符
description: 本文说明为何科目表和维度值的分隔符不能相同。 必须在升级后更改分隔符值。
author: RyanCCarlson2
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: RCarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.openlocfilehash: 2184d26e104f803ae1bf59155cf18f560652f318
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292487"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>使会计科目表分隔符的成为唯一的

[!include [banner](../includes/banner.md)]

在 Microsoft Dynamics AX 2012 中，可为科目表和维度值使用相同分隔符。 在财务和运营的当前版本中，科目表和维度名称或值的分隔符不能相同。 如果有相同分隔符，可在升级后更改。 

## <a name="update-delimiter"></a>更新分隔符
如果科目表存在冲突，则可更改科目表分隔符和项目/子项目 ID。 不能更改其他维度分隔符。 
- 升级之后，可在 **总帐参数** > **会计科目表和维度** > **更改分隔符** 中更改会计科目表分隔符。 
- 如果只有项目/子项目 ID 格式冲突，则可在 **项目管理与核算参数** > **常规** > **修改子项目格式** 中更改该值。 

### <a name="other-considerations"></a>其他注意事项
与项目/子项目 ID 类似，用作财务维度的任何其他主数据记录（如供应商或客户）均不应具有使用与会计科目表分隔符相同的字符的科目 ID 值。 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>如何确定环境是否需要更新后的分隔符 
如果升级后的环境中的分隔符冲突，在细分条目控件或维度条目控件中输入值时，可能遇到不稳定。 这意味着输入科目和维度组合时，始终需要使用查找或弹出菜单。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

