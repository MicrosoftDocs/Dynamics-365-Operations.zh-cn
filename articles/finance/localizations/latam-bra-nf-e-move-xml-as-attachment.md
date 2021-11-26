---
title: 将 NF-e XML 文件作为附件移动
description: 本主题说明如何将 NF-e XML 文件从 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 数据库中移出，并将它们作为附件提供。
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: c7b82d486cecf6b20f1283fa609c360b3003efca
ms.sourcegitcommit: ebf6546835e4d6a80aea1dfae81e119e294387f0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/12/2021
ms.locfileid: "7799441"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>将 NF-e XML 文件作为附件移动

[!include [banner](../includes/banner.md)] 


发布电子会计单据 (NF-e) 时，会创建 XML 文件并将其存储在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 数据库中。 在巴西本地化中，您可以使用 **作为附件移动 NF-e XML** 功能来释放这些 XML 文件占用的数据库空间。

对于特定日期范围和会计设立，此功能会将 NF-e XML 文件从您的 Finance 或 Supply Chain Management 数据库移到您的 Azure 订阅中的 Blob 存储。 此移动使文件只能作为附件提供。 XML 文件成功移动到 Blob 存储后，原始文件将被从 Finance 或 Supply Chain Management 数据库中删除。 因此，这些文件使用的数据库空间会被释放。

按照以下步骤启用 **作为附件移动 NF-e XML** 功能。

1. 在 Finance 或 Supply Chain Management 中，打开 **功能管理** 工作区。
2. 在 **所有** 选项卡上，搜索并选择 **作为附件移动 NF-e XML** 功能。
3. 选择 **立即启用**。

按照这些步骤作为附件移动 NF-e XML 文件。

1. 转到 **应收帐款** \> **会计单据** \> **电子会计单据** \> **作为附件移动 NF-e XML**。
2. 在 **开始日期** 和 **结束日期** 字段中，选择开始和结束日期。
3. 在 **会计设立 ID** 字段中，选择一个值。
4. 选择 **确定**。

> [!IMPORTANT]
> 此流程是不可逆的。 移动 NF-e XML 文件后，用户只能通过选择 **会计单据** 页面顶部的 **附件** 查看这些文件。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
