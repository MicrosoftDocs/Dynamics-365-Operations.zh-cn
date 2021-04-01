---
title: 维护状态
description: 本主题说明如何在资产管理中计算维护状态。
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f65bfc7b5ef9651853a12bab2ed83dbb8562ba6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253726"
---
# <a name="maintenance-status"></a>维护状态

[!include [banner](../../includes/banner.md)]

 

在资产管理中，您可以针对新的、有效的和已完成的维护请求、工作订单和维护停机时间活动，在特定期间进行概览计算。 也可以查看同一期间的已完成条件评估数量。 可使用此计算获取传入的和已完成的维护请求和工作订单的工作负载的概览。

## <a name="make-a-maintenance-status-calculation"></a>创建维护状态计算

1. 单击 **资产管理** > **查询** > **维护状态**。

2. 在 **计算状态** 对话框的 **开始日期** 和 **结束日期** 字段中选择要进行计算的时间范围。

3. 可使用 **级别** 字段指示要与功能位置有关的维护行的详细程度。 

  例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有维护安排行，因此，可以从较低级别的功能位置叠加行中的状态。 
  
  如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有维护行。

4. 单击 **确定** 开始计算。

5. 单击 **分组依据** 按钮显示所需的计算详细程度。 将突出显示所选 **分组依据** 按钮。 单击按钮将其激活或停用。

6. 每次通过激活或停用 **分组依据** 按钮或通过为新期间创建计算来进行更改时，都应该单击 **更新** 按钮以更新计算。

7. 如果要创建新的维护状态计算，请单击 **状态**。

>[!NOTE]
>**维护状态** 中显示的结果仅包括具有实际开始日期和时间的维护请求和工作订单。 结束日期和时间可以为空。

## <a name="example-1"></a>示例 1

在下面的屏幕截图中，已激活 **年** 和 **月** 按钮。 选择这些 **分组依据** 选项后，您将获取基于与维护请求和工作订单关联的月工作负载和吞吐量的一般概览。 

![月工作负载示例](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>示例 2

在下面的屏幕截图中，已添加了有关功能位置的信息。 请注意，可以比较多个功能位置（可以是地理位置、工厂或工作区域）的工作负载和吞吐量。 

![包含功能位置的月工作负载示例](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]