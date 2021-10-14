---
title: 定义生产流版本的到期日期
description: 若要在给定日期终止某个生产流版本的有效性和处理，或计划将某个有效版本替换为新版本，必须为该版本设置到期日期。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f6ee9177664767c31eaa3e9b65d7559a1a9662f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574417"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>定义生产流版本的到期日期

[!include [banner](../../includes/banner.md)]

若要在给定日期终止某个生产流版本的有效性和处理，或计划将某个有效版本替换为新版本，必须为该版本设置到期日期。 不必停用该版本。


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>设置到期日期以结束生产流版本
1. 转到“生产控制”>“设置”>“精益生产流程”>“生产流程”。
2. 在列表中，找到并选择所需记录。
    * 选择已为其定义了版本的任何生产流。  
3. 在列表中，单击所选行中的链接。
4. 单击“编辑”。
5. 在列表中，标记所选的行。
6. 在“到期日期”字段中，输入日期和时间。
    * 对于到期日期，新版本将不启动或进入已激活状态。 并且还不能为此生产流创建或启动作业。 到期日期后，仍然可以完成已开始的作业。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]