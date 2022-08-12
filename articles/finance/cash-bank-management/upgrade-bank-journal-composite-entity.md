---
title: 更新银行日记帐组合实体
description: 本文列出了将更多 BankTransactionType 字段添加到组合 BankJournalEntity 中所需的步骤。
author: angelad116
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f8bf3bbcbd8036015757799a2e58b23fd9bd2b38
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151601"
---
# <a name="update-the-bank-journal-composite-entity"></a>更新银行日记帐组合实体

[!include [banner](../includes/banner.md)]

本文列出了将更多 BankTransactionType 字段添加到组合 BankJournalEntity 中所需的步骤。

按照以下步骤将更多 BankTransactionType 字段添加到组合 BankJournalEntity 中。

1.  编译和同步以下银行日记帐组合实体、实体和暂存表：
    -   组合实体\\BankJournalEntity
    -   实体\\BankJournalHeaderEntity
    -   实体\\BankJournalLineEntity
    -   表\\BankJournalHeaderStaging
    -   表\\BankJournalLineStaging

2.  数据管理\\数据项目
    -   在 **源数据** 版式上公开 **银行交易记录** 类型。
        -   源数据格式 = XML-元素
        -   实体名称 = 银行日记帐
        -   上载数据文件 = SampleBankJournalCompositeEntity.xml 的新版本
        -   单击 **是** 以覆盖现有文件。
        -   单击 **是** 从头开始生成新的映射。
        -   验证银行交易记录类型是否已映射。
            -   单击“行”实体上的 **查看映射**。
            -   验证“银行交易记录”类型是否已从源映射到暂存。

3.  导入新的对账单。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
