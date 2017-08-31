--- 
title: "停用生产流版本"
description: "如果不再需要某个有效生产流版本，可将其停用。"
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 06daa5e7d2b8e88bca281dc9bcaa73927253553c
ms.contentlocale: zh-cn
ms.lasthandoff: 07/28/2017

---
# <a name="deactivate-a-production-flow-version"></a>停用生产流版本

[!include[task guide banner](../../includes/task-guide-banner.md)]

如果不再需要某个有效生产流版本，可将其停用。 仅当所有看板规则和活动已结束且将不再激活，才应使用此选项。 请注意，将使用当前日期和时间更新与此生产流版本有关的所有看板规则的到期日期。 

若要修改有效生产流版本，请考虑设置有效版本的到期日期和创建新版本。 这样您就可以继续生产操作，同时准备新版本和相关看板规则。 

若要让有效生产流版本到期，需要设置到期日期。 在这种情况下，停用更像异常，而不是规则。 

对于此过程，您需要具有可停用版本的生产流。 除非您百分百确定版本已完全过时，否则请勿在生产环境中尝试此操作。


## <a name="deactivate-a-production-flow-version"></a>停用生产流版本
1. 转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 在列表中，找到并选择所需记录。
5. 单击“停用”。
    * 如果不是百分百确定此生产流版本已过时，否则请勿继续操作。 单击“确定”将让所有有效看板规则过期，并立即停止此生产流版本的所有生产和补货活动。  
6. 单击“确定”。


