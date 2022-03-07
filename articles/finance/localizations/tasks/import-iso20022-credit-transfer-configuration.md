---
title: 导入 ISO20022 贷方转帐配置
description: 此过程显示如何导入供应商付款电子申报配置。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af34a91b2a265755cd1905401e0b7451f9fc1168
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218774"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>导入 ISO20022 贷方转帐配置

[!include [banner](../../includes/banner.md)]

此过程显示如何导入供应商付款电子申报配置。 以德国 ISO 20022 贷方转帐格式为例。 此过程可用于其他可用电子申报格式。 

此任务是使用演示数据公司 DEMF 创建的，但是您可以使用任何演示数据公司完成此任务。

这是五个共同用于演示使用电子申报配置的供应商付款流程的任务中的第一个。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。

1. 转到“组织管理”>“工作区”>“电子申报”。
2. 在可用配置提供商列表中，选择“Microsoft”。
3. 单击“设置有效”。
4. 单击“存储库”。
5. 单击“打开”。
6. 单击“显示筛选器”。
7. 应用以下筛选器：使用“开头为”筛选器运算符在“配置名称”字段中输入筛选器值“ISO20022 贷方转帐（德国）”。
    * 也可以在列表中查找配置，选择该配置，然后将其移至“导入任务”。  
8. 单击“导入”。
    * 如果导入按钮没出现，表示该配置文件已经被导入了。  
9. 单击“是”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]