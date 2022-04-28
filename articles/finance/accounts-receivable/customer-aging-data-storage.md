---
title: 客户帐龄数据存储
description: 本主题介绍对客户帐龄数据使用外部存储的过程。 您可以运行客户帐龄数据存储流程，以使输出可导出到外部系统。
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 497d49da84f4df90877908bef3031e079bc36066
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557869"
---
# <a name="customer-aging-data-storage"></a>客户帐龄数据存储

[!include [banner](../includes/banner.md)]


本主题介绍对客户帐龄数据使用外部存储的过程。 在 Microsoft Dynamics 365 Finance 中，您可以运行客户帐龄数据存储流程，以使输出可导出到外部系统。 运行此流程时，系统中可用的相同帐龄报表选项可用于外部系统。 导出的数据中始终包含详细信息。

在输出包含许多客户和/或多个交易记录的情况下，将客户帐龄数据提供给外部系统进行存储很有用。 如果现有 **客户帐龄** 报表因数据过多无法打印从而导致超时，则此功能可提供获取相同数据的替代方法。

## <a name="enable-the-customer-aging-data-storage-feature"></a>启用客户帐龄数据存储功能

此功能只有在系统中启用了之后才能使用。 管理员可以使用功能管理设置检查功能状态和启用功能（如果需要）。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块：** 信用和收款
- **功能名称：** 客户帐龄数据存储

## <a name="run-the-customer-aging-data-storage-process"></a>运行客户帐龄数据存储流程

1. 转到 **信贷和收款 \> 查询和报表 \> 客户 \> 客户帐龄数据存储**。
2. 选择 **新建**。
3. 在 **名称** 字段中，为流程输入一个名称。
4. 根据需要设置剩余参数。

    > [!NOTE]
    > 交易记录详细信息始终包含在内，并且处理始终在批处理作业中完成。

5. 选择 **确定**。
6. 刷新 **客户帐龄数据存储** 页，以查看与 **处理状态** 值一起显示的 **批处理名称** 和 **批处理运行时间** 值。 完成批处理作业后，**处理状态** 字段被设置为 **已结束**，并且会设置 **帐龄行数** 字段。 如果批处理作业是定期作业，则 **处理状态** 字段会设置为 **正在等待**。
7. 选择 **帐龄行数** 字段旁边的 **筛选器** 按钮，以查看已为批处理作业添加的筛选器。

**客户帐龄数据存储** 页不包括结果。 但是，**客户帐龄数据存储** 数据实体允许您将输出导出为数据管理支持的任何格式。

> [!NOTE]
> 在执行导出之前，添加筛选器以将导出的结果限制为最近的帐龄。 例如，添加以下条件以返回最近的批处理运行：
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchName())
>
> 或者，添加以下条件以返回当前用户的最近批处理运行：
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchNameForCurrentUser())
