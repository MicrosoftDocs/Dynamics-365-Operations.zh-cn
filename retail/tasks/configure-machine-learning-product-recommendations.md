--- 
title: "配置机器学习支持的产品建议"
description: "此过程刷新实体商店中为生产建议提供支持的机器学习系统使用的数据，然后启用有关 POS 客户端的产品建议。"
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c51c5f82efb50db1e238f4046506920975f33218
ms.contentlocale: zh-cn
ms.lasthandoff: 07/28/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a>配置机器学习支持的产品建议

[!include[task guide banner](../includes/task-guide-banner.md)]

此过程刷新实体商店中为生产建议提供支持的机器学习系统使用的数据，然后启用有关 POS 客户端的产品建议。 此程序使用 USRT 演示数据公司。

1. 转到“系统管理”>“设置”>“实体商店”。
2. 在列表中，找到并选择记录“RetailSales”。
3. 单击“刷新”。
4. 单击“确定”。
5. 关闭该页面。
6. 转到“零售和商业”>“总部设置”>“参数”>“零售参数”。
7. 单击“机器学习”选项卡。
8. 在“启用产品建议”字段中选择“是”。
    * 如果收到消息“无法检索建议模型”，这是因为您最近刷新了实体商店，并且系统可能尚未完成新数据的吸收。 等待 2-3 小时再重试。  
9. 单击“保存”。
10. 关闭该页面。


