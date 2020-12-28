---
title: 高级银行对帐 MT940 导入 - 综合数据实体升级
description: 需要将序列号添加到银行对账单导入实体以支持 MT940 格式。
author: panolte
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 65970cdac114b72363d2fbbc08766c99ace00b88
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440694"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>高级银行对帐 MT940 导入 - 综合数据实体升级

[!include [banner](../includes/banner.md)]

需要将序列号添加到银行对账单导入实体以支持 MT940 格式。 

使用以下步骤添加银行对账单导入实体以支持 MT940 格式。

1.  编译并同步以下操作：
    -   组合实体\\BankStatementImportEntity
    -   实体\\BankStatementBalanceEntity
    -   实体\\BankStatementDocumentEntity
    -   实体\\BankStatementEntity
    -   实体\\BankStatementLineEntity
    -   表\\BankStatementStaging

2.  数据管理\\数据项目。
    1.  负荷 MT940 导入项目
        1.  变更 XSLT。
            -   单击 **查看映射**。
            -   单击银行对账单单据上的 **查看映射**。
            -   单击 **转换**
            -   删除 BankReconiliation-to-Composite.xslt 文件。
            -   添加 BankReconiliation-to-Composite.xsl 的新版本。

        2.  在 **源数据** 版式上公开 **序列号**。
            1.  源数据格式 = XML 元素。
            2.  实体名称 = 银行对账单。
            3.  上载数据文件 = SampleBankCompositeEntity.xml 的新版本。
            4.  单击 **是** 以覆盖现有文件。
            5.  单击 **是** 生成新的映射。
            6.  验证S **equenceNumber** 是否已映射。
                -   单击对账单实体上的 **查看映射**。
                -   验证 **SequenceNumber** 是否已从源映射到暂存。

3.  导入新的对账单。




