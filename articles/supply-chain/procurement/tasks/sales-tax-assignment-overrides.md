---
title: 销售税分配和覆盖
description: 此过程演示如何为商业渠道分配增值税组。
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74a7eed04648c63c0b19d5de26d2bdbef59aec7d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423048"
---
# <a name="sales-tax-assignment-and-overrides"></a> 销售税分配和覆盖

[!include [banner](../../includes/banner.md)]

此过程演示如何为商业渠道分配增值税组。 还逐步演示了新建增值税覆盖并分配给现有增值税覆盖组的过程。 此程序使用 USRT 演示数据公司。

1. 转至“Retail 和 Commerce”>“渠道”>“商店”>“所有商店”。
2. 在列表中，单击“休斯敦”的“渠道 ID”链接。
3. 单击“编辑”。
    * “增值税组”字段中包含当前公司的增值税组列表。 当前分配的组是普通的“德克萨斯”增值税组。 “华盛顿”和“华盛顿，金县”也有增值税组。 增值税组中可以包含多个城市的适用税。  
    * 可以在“增值税覆盖”字段中将增值税覆盖组映射到渠道。 增值税覆盖组可用于将多个商店适用的增值税覆盖组合在一起。 可以创建该组并直接分配给渠道来节约时间，而不是手动逐一分配增值税覆盖。  
4. 单击“保存”。
5. 关闭该页面。
6. 转到“Retail 和 Commerce”>“渠道设置”>“增值税”>“增值税覆盖”。
7. 单击“新建”。
8. 在“增值税覆盖”字段中，为新覆盖提供名称。
9. 在“描述”字段中，提供该覆盖的描述。
10. 将状态设置为“启用”。
11. 展开或折叠“覆盖”部分。
12. 在“类型”字段中，选择一个选项。
    * 物料增值税组可用于覆盖属于该组的具体物料的税。 例如，食品物料的征税通常与耐用品的征税不同，所以可能有自己的增值税组。 增值税组是适用于特定渠道的税的组合。 例如，如果某个渠道同时开展零售和批发业务，则可以使用不同的物料增值税组。 将把所有适用的税映射到该增值税组。  
    * 现在可以选择“源”和“目标”税或“源税组”和“目标税组”来创建增值税覆盖。 “源”字段指示要覆盖的税或税组。 通过物料增值税组覆盖提供的选项比通过增值税组覆盖提供的选择多。 可以将增值税覆盖设置为覆盖整个交易记录中的税，或覆盖交易记录的特定行中的税。  
13. 单击“保存”。
14. 关闭该页面。
15. 转到“Retail 和 Commerce”>“渠道设置”>“增值税”>“增值税覆盖组”。
    * 此步骤，您将把新建的增值税覆盖分配给为休斯敦渠道分配的增值税覆盖组。  
16. 单击“编辑”。
17. 展开或折叠“设置”部分。
18. 单击“添加”。
19. 在“增值税覆盖”字段中，单击下拉按钮以打开查找。
20. 在列表中选择前面创建的增值税覆盖。
21. 在列表中，单击所选行中的链接。
22. 单击“保存”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]