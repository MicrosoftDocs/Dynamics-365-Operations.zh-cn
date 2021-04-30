---
title: 手动修改需求预测
description: 本主题介绍了如何修改物料的预测
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889016"
---
# <a name="modify-a-demand-forecast-manually"></a>手动修改需求预测

[!include [banner](../../includes/banner.md)]

此过程显示如何修改物料预测。 创建此程序的演示数据公司是 USMF。 此程序是专为生产规划员设计的。

## <a name="modify-the-forecast-for-a-selected-item"></a>修改选定物料的预测

若要修改选定物料的预测：

1. 转到 **模块 \> 产品信息管理 \> 产品 \> 已发布产品**。
1. 在列表中，找到并选择所需记录。 选择要更改预测的物料。
1. 在操作窗格上，打开 **计划** 选项卡并选择 **需求预测**。
1. 在列表中，选择一行。 如果没有预测行，通过在操作窗格上选择 **新建** 来创建新行。  
1. 在 **销售数量** 字段中，输入一个正数。 此数字代表该物料的预测数量。 如果输入负数，将显示错误。
1. 根据需要填写其他字段。
1. 在操作窗格上选择 **保存**。

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a>修改 Microsoft Excel 中一个或多个物料的预测

若要修改 Microsoft Excel 中一个或多个物料的预测：

1. 执行以下选项之一：
    - 针对上一部分中所述的任何物料（无论是哪一个）打开 **需求预测** 页面。
    - 转到 **主计划 \> 预测 \> 手动预测条目 \> 需求预测行**。
1. 在操作窗格上，选择 **在 Microsoft Office 中打开 \> 需求预测条目**。
1. 选择下载位置，保存，然后在 Excel 中打开下载的文件。
1. 如果看到警告，请选择 **启用编辑**。
1. 在 Excel 中，使用 Microsoft Dynamics 任务窗格登录到 Supply Chain Management。 您必须使用启用的 **我保持登录状态** 选项登录，并且必须信任数据连接应用。
1. Excel 电子表格现在显示您的公司的所有当前需求预测行。  根据需要添加、删除和编辑需求预测行。
1. 在 Microsoft Dynamics 任务窗格上选择 **发布** 以将您的更改上传回 Supply Chain Management。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
