---
title: 创建固定资产
description: 本主题介绍了如何从“固定资产”列表页面创建新的固定资产记录。
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 770390092342e2db496dde850a75b2f7736bd4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817093"
---
# <a name="create-a-fixed-asset"></a>创建固定资产

[!include [banner](../../includes/banner.md)]

本主题介绍了如何从 **固定资产** 列表页面创建新的固定资产记录。

系统根据分配给固定资产组的编号序列分配资产编号。 如果您使用固定资产模板来通过 Microsoft Excel 加载项导入资产，或者如果您使用其他导入作业，系统将自动创建固定资产记录并递增资产编号。

若要手动创建资产记录，请按照下列步骤操作。

1. 转到 **导航窗格 \> 模块 \> 固定资产 \> 固定资产 \> 固定资产**。
2. 在 **操作窗格** 上，选择 **新建**。
3. 在 **固定资产组** 字段中，输入或选择一个值。 如果您在 **固定资产参数** 和 **固定资产组** 中启用 **固定资产自动编号功能**，将会默认显示 **编号** 字段。 如果没用启用，您必须输入唯一编号以识别固定资产。
4. 在 **名称** 字段中，输入一个值。 输入您的企业为该资产所需的其他信息。
5. 在 **操作窗格** 上，选择 **帐簿**。
6. 在 **购置日期** 字段中输入日期。
7. 在 **购置价格** 字段中输入数字。

    - 输入您的企业为该帐簿所需的其他信息。
    - 输入您的企业为其余帐簿所需的其他信息。

8. 关闭该页面。

您也可以通过使用 Excel 加载项或通过从 **数据管理** 工作区运行导入作业来导入固定资产。 在运行导入之前，请在模板中输入必填字段的值。

如果您没有在 Excel 加载项的模板中或在数据管理中定义固定资产编号，系统会为每个导入的资产创建固定资产编号，并自动递增每个编号序列。 但是，如果您导入资产并在模板中定义资产编号，系统 **不会** 自动递增编号序列。 在这种情况下，管理员必须手动更新编号序列。 如果您在 Excel 加载项的模板中定义了固定资产编号，系统将使用定义的固定资产编号并递增编号序列。

> [!NOTE]                                                                                                         
> 过帐折旧后，将锁定 **帐簿** 页面中的 **投入使用** 和 **折旧运行日期** 字段。 此外，还将从数据实体更新这两个字段。

> [!WARNING]
> 如果将交易记录过帐到关联的帐簿，或者在日记帐行中输入了新创建的固定资产但未过帐，则不会删除固定资产记录。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]