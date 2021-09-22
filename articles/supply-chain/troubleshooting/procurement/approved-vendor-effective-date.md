---
title: 无法更改核准供应商的生效日期
description: 按产品实体列出的核准供应商列表不允许更改生效日期
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475644"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>无法更改核准供应商的生效日期


## <a name="symptoms"></a>故障特征

例如，产品有生效日期为 2018 年 1 月 11 日 (*01/11/2018*)，到期日期为 *从不* 的核准供应商。 如果您尝试将生效日期更改为 2018 年 1 月 10 日 (*01/10/2018*) 或 2018 年 1 月 12 日 (*01/12/2018*)，将收到以下错误：

> 无法在核准供应商列表 (PdsApproveVendorList) 中创建记录。 “到期”值必须大于或等于“生效”值。

## <a name="resolution"></a>解决方法

您只能延长供应商的核准期限。 下列规则适用：

- 要更改生效日期，使其早于物料供应商的任何现有记录（期限），新期间的到期日期必须早于现有记录中的所有到期日期。
- 若要更改到期日期，使其晚于任何现有期限，生效日期必须在任何现有记录中的最新到期日期之后。
- 要减少供应商的总核准期限，必须删除或修改现有记录。 或者，您可以在导入期间使用 **截断** 切换。 此切换按物料删除表中核准供应商的所有现有记录。

对于问题描述中描述的示例场景：记录的生效日期为 *01/11/2018*，到期日期为 *从不*，可以导入生效日期为 *01/10/2018*、到期日期为 *从不* 的新记录。 但是，您无法通过数据管理缩短期限，让生效日期更新为 *01/12/2018*。 您必须通过 UI 进行此更改。
