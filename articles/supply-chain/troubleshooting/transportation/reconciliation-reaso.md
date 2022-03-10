---
title: 出于对帐原因，您只能将主科目添加为货方科目
description: 在运输管理中设置对帐原因时，只能将主科目添加为货方科目。
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c4ba48c5b6e3476c203eed2fddf053ce8af873dd6a7665df54560c8894f8c2d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750874"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>出于对帐原因，您只能将主科目添加为货方科目

知识库编号：4603538

## <a name="symptoms"></a>故障特征

在运输管理中设置对帐原因时，只能将主科目添加为货方科目。 您不能将成本中心或任何其他维度添加为贷方科目。 但是，贷方科目允许您选择其他维度。

## <a name="resolution"></a>解决方法

如果对帐不是要支付供应商而是要贷记特定主科目，那么在设置对帐原因时，系统将不允许您为贷方科目选择财务维度。

如果科目结构需要贷方主科目使用特定的财务维度值，生成的供应商日记帐将由于缺少财务维度值无法自动过帐。 因此，您必须使用 **发票日记帐** 页首先手动指定贷方科目。

由于贷方科目需要维度值，因此供应商发票日记帐无法自动过帐。 在将维度值手动添加到贷方行的主科目后，您必须手动过帐。
