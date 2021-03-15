---
title: 冲销已过帐租赁交易
description: 本主题说明如何冲销已过帐的租赁交易。 通过资产租赁创建的任何交易都可以冲销。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3e4908ddab2650e5ff7e4a28bf916604d165d08c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969520"
---
# <a name="reverse-posted-lease-transactions"></a>冲销已过帐租赁交易

[!include [banner](../includes/banner.md)]

通过资产租赁创建的任何交易都可以冲销。 通过资产租赁冲销的交易会更新您的租赁数据。 因此，它们还会更新租赁负债和使用权 (ROU) 资产的帐面价值。

要为租赁创建冲销交易，请按照下列步骤操作。

1. 在 **资产交易** 页面或 **负债交易** 页面上，选择交易，然后选择 **冲销交易**。
2. 在出现的对话框中，可以编辑冲销条目的过帐日期。 默认情况下，**日期** 字段设置为所选交易的交易过帐日期。 冲销条目不能早于所选交易的原始过帐日期过帐。
3. 选择 **确定**。 将过帐日记帐条目，以冲销您选择的条目。 将在 **资产交易** 或 **责任交易** 页上显示冲销，并更新该页上显示的当前余额的净额总计。

当您选择 **冲销追踪** 时，会出现一个对话框，其中显示原始交易和冲销的交易，以及一个链接号，称为 *跟踪号*。 为了使冲销更容易理解并提高可见性，您还可以使用租赁计划来跟踪冲销。

**计划** 页上的 **最近日记帐编号** 字段显示交易的日记帐编号。 冲销交易时，将使用冲销交易的日记帐编号更新此字段。 此外，将选中 **已冲销** 复选框，以指示交易已冲销，并且将选中 **已过帐** 字段。

## <a name="revoke-a-reversed-transaction"></a>撤消已冲销交易

要撤消已冲销交易，请按照下列步骤操作。

1. 在 **计划** 页面或 **交易** 页上，选择原始交易。
2. 按以下步骤之一：

    - 如果您在 **计划** 页上选择了交易，请按照[批量创建月度日记帐条目](create-monthly-journals-batch.md)中有关创建日记帐的步骤操作。 您必须手动过帐日记帐。
    - 如果您在 **交易** 页面上选择了交易，请选择 **冲销交易**。 您将收到一条消息，指出该撤回是对先前冲销的撤销，并且您可以编辑此撤销的过帐日期。 但是，一般业务验证会影响可以在 **日期** 字段中输入的日期。 

3. 选择 **确定**。 将过帐日记帐条目，以冲销您选择的条目。 将在 **交易** 页中显示冲销，并将当前总净余额恢复为第一次冲销之前的值。 因此，避免了冲销对余额的影响。

当您选择 **冲销追踪** 时，会出现一个对话框，其中显示原始交易和冲销的交易，以及一个链接号。

您还可以使用相应 **计划** 页来跟踪冲销。 将清除 **冲销** 字段，但选中 **已过帐的日记帐** 字段。 此外，将使用撤回交易的日记帐编号更新 **最近的日记帐编号** 字段，并使用冲销日记帐编号更新 **日记帐编号** 字段。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]