---
title: "为 POS 配置现金面额"
description: "可以在后端办公系统中定义商店的收银员、销售内勤和经理从 POS 内使用的纸币和硬币的现金面额。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d280a11670b5887ae5ae582cedf30c093b4b5d7c
ms.openlocfilehash: 9abcbb706d7120c6bcd91fc759b33cb518802a5b
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="configure-cash-denominations-for-pos"></a>为 POS 配置现金面额

[!include[banner](includes/banner.md)]

可以在后端办公系统中定义商店的收银员、销售内勤和经理从 POS 内使用的纸币和硬币的现金面额。 这些面额可用于为日结钱币清点或快速清点一笔销售时帮助清点现金。

## <a name="define-denominations"></a>定义面额
面额在**设置** > **商店属性中的现金清点选项**页中根据商店设置。 

![现金面额](./media/image1-denomination.png)

若要定义面额：
1. 单击“**新建**”。
1. 指定类型（硬币还是纸币）。
1. 指定金额（值）。

![现金面额](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>配置功能配置文件
使用 POS 现金付款时，用户可使用纸币面额快速输入客户支付的金额。 在功能配置文件中，可以配置两种 POS 中的面额显示选项。

**大于或等于应付款金额**：默认情况下，POS 仅显示大于应付款金额的纸币面额，这样就可以进行一键式付款。 例如，如果应付款金额为 7.50 美元，POS 将显示以下金额：10 美元、20 美元、50 美元和 100 美元。 触摸这些金额中的任何一个都将自动为销售收取这笔金额。 不显示 1 美元和 5 美元纸币，因为这些金额低于应付款金额。

**全部面额**：选择此选项将在 POS 中始终显示所有纸币面额，不受应付款金额的影响。 这意味着用户可以使用纸币组合以凑够应付款金额。 例如，如果应付款金额为 25 美元，则用户可选择 20 美元和 5 美元来完成销售。

