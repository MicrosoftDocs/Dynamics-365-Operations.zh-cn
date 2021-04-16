---
title: 创建消耗报表
description: 本主题说明如何在资产管理中创建消耗报表。
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8add0602e0ebe7a5c0cf2c76de6fa2f4f21a2f72
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837913"
---
# <a name="create-consumption-reports"></a>创建消耗报表

[!include [banner](../../includes/banner.md)]

 

在资产管理中为工作订单创建和过帐消耗登记之后，将提供两个报告来显示消耗详细信息。


## <a name="asset-consumption-report"></a>资产消耗报表

过帐工作订单的消耗后，可打印资产消耗报表。 该报告显示为资产过帐的工时、工时成本、物料成本和费用。

1. 单击 **资产管理** > **报表** > **资产** > **资产消耗**。

2. 在 **资产消耗** 对话框中，选择要查看的参数和详细程度，方法是在相关切换按钮上选择 **是**，然后在 **显示** 部分中插入功能位置级别。
    - 可使用 **级别** 字段指示要与功能位置有关的资产行的详细程度。 
    
        例如，如果在字段中输入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有资产行，因此，可以从较低级别的功能位置叠加行。 
        
        如果在 **级别** 字段中输入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有资产。 
        
    - 在 **所有子资产之和** 切换按钮上选择 **是** 可在报表中查看每个子资产之和。

3. 在 **日期** 部分中选择日期期间。

4. 在 **目标** 快速选项卡上，选择要在屏幕上显示报表，打印报表还是另存为文件或电子邮件。

5. 如果需要，可选择在报表中显示特定资产。 在 **要包括的记录** 快速选项卡上，单击 **筛选**，然后添加报表中要包括的资产。

6. 单击 **确定** 以生成报表。


## <a name="work-order-consumption-report"></a>工作订单消耗报表

过帐工作订单的消耗后，可打印工作订单消耗报表。 该报告显示为工作订单过帐的工时、工时成本、物料成本和费用。

1. 单击 **资产管理** > **报告** > **工作订单报告** > **工作订单消耗**。

2. 在 **工作订单消耗** 对话框中，显示报表中要包含的参数，方法是在 **显示** 部分中的相关切换按钮上选择 **是**。

3. 在 **日期** 部分中选择日期期间。

4. 在 **目标** 快速选项卡上，选择要在屏幕上显示报表，打印报表还是另存为文件或电子邮件。

5. 如果需要，可选择在报表中显示特定工作订单。 在 **要包括的记录** 快速选项卡上，单击 **筛选**，然后添加报表中要包括的工作订单。

6. 单击 **确定** 以生成报表。


>[!NOTE]
>也可以生成[工作订单报表](../work-orders/work-order-report.md)，其中包含更多工作订单详细信息。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]