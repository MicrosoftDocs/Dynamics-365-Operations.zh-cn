---
title: 未生成凭证
description: 本文提供可以在凭证应生成但未生成时提供帮助的故障排除信息。
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1200fe50bf9be4c6d1ca809ad9a86da2ff3e0ced
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909002"
---
# <a name="voucher-isnt-generated"></a>未生成凭证

[!include [banner](../includes/banner.md)]

如果应生成凭证，但 **凭证交易** 页未显示任何凭证，请根据需要按照以下各节中的步骤解决此问题。

[![没有凭证的“凭证交易”页面。](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>检查税适用性

1. 转到 **税** \> **定期任务** \> **未转移的子分类日记帐分录**。
2. 如果有日记帐记录，选择它，然后选择 **立即转移**。

    [![“未转移的子分类帐日记帐条目”页面上的“立即转移”按钮。](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. 再次打开 **凭证交易** 页，查看是否生成了凭证。

## <a name="determine-whether-customization-exists"></a>确定是否存在自定义

如果您已经完成了上一节中的步骤，但未发现问题，请确定是否存在自定义。 如果不存在自定义，请创建 Microsoft 服务请求寻求进一步支持。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
