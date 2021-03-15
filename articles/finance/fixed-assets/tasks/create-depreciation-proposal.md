---
title: 创建折旧方案
description: 本主题描述折旧批处理建议的工作原理，并说明如何为固定资产建议折旧。
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3d62e982d26afbec7ac04dd80592a73f4a3286f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968895"
---
# <a name="create-a-depreciation-proposal"></a>创建折旧方案

[!include [banner](../../includes/banner.md)]

本主题描述折旧批处理建议的工作原理，并说明如何为固定资产建议折旧。 此任务使用 USMF 演示公司和会计角色。


## <a name="create-a-depreciation-proposal"></a>创建折旧方案
1. 在导航窗格中，转到 **模块 > 固定资产 > 日记帐条目 > 创建折旧方案**。
2. 在 **日记帐的名称** 字段中，从下拉菜单中选择一个选项。
3. 在 **结束日期** 字段中输入日期。

    - 选择 **汇总折旧** 选项，将按月折旧汇总到一个日记帐行。  
    - 例如，如果“结束日期”值为 2015 年 3 月 31 日，则会生成以下描述：“自 2015 年 1 月 31 日起折旧”。 建议日记帐行的 **日期** 字段随后将设置为 2015 年 3 月 31 日。  
    - 使用 **筛选** 选项，按资产、资产组或其他条件筛选折旧方案。  
    - 如果您为固定资产表格使用 **创建购置或折旧方案**，可以批处理折旧方案。 对于使用较多系统资源的较大方案，建议使用此方案。 如果选择批处理选项，您仍可以在该期间完成其他任务。 在您这样建议折旧时，则为固定资产价值模型计算折旧。  

4. 选择 **创建日记帐**。

## <a name="review-depreciation-entries"></a>查看折旧条目
1. 在导航窗格中，转到 **模块 > 固定资产 > 日记帐条目 > 固定资产日记帐**。
2. 在列表中，找到并选择所需记录。
3. 选择 **行**。
4. 选择 **过帐**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]