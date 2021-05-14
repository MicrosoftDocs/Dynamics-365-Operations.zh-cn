---
title: 未生成 TaxTrans 记录
description: 本主题提供可以在未生成 TaxTrans 记录时提供帮助的故障排除信息。
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947601"
---
# <a name="taxtrans-record-isnt-generated"></a>未生成 TaxTrans 记录

[!include [banner](../includes/banner.md)]

如果您为交易选择 **已过帐销售税**，但是 **已过帐销售税** 页上未显示税务行或缺少税务行，有可能是未生成 **TaxTrans** 记录。

[![没有行项的“已过帐销售税”页](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

要解决此问题，请根据需要按照以下各节中的步骤操作。

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>过帐交易前检查销售税

1. 在过帐交易之前，在 **过帐发票** 页上，选择 **销售税** 检查计算。

    [![“过帐发票”页上的“销售税”按钮](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. 在 **临时销售税交易** 页上，查看计算结果。 如果未计算税款，请参阅[未计算税款或税额为零](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md)。

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>在所有过帐的销售税中查找 TaxTrans 记录

1. 转到 **税** \> **查询和申报** \> **销售税查询** > **已过帐销售税**。
2. 在 **凭证** 列标题中，选择筛选符号查找 **TaxTrans** 记录。
3. 如果找到了所需的销售税记录，请检查日期。 如果日期不同于日记帐标头的日期，请创建 Microsoft 服务请求寻求其他支持。

    [![已过帐的销售税页面](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>调试以检查详细信息

1. 有关如何调试和确定是否正确生成了 **TmpTaxWorkTrans** 和 **TaxUncommitted** 的信息，请参阅 [TaxTrans 中的字段值不正确](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md)。
2. 如果正确生成了 **TaxTmpWorkTrans** 或 **TaxUncommitted**，在 **TaxPost::SaveAndPost()** 和 **Tax::SaveAndPost** 处添加中断点来调试未插入 **TaxTrans** 的原因。

    [![在代码中添加的中断点](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![添加的中断点的结果](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>确定是否存在自定义

如果您已经完成了前面几节中的步骤，但未发现问题，请确定是否存在自定义。 如果不存在自定义，请创建 Microsoft 服务请求寻求进一步支持。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
