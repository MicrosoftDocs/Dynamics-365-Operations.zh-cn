---
title: 维修管理
description: 可以系统化地将多个问题进行分组，以便帮助建议在过去成功的解决方案。
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32372a6a54e2adfbf511e2247be4a9baa28b4b53
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015192"
---
# <a name="repair-management"></a>维修管理       

[!include [banner](../includes/banner.md)]


对于您可以系统化地分组问题的维修管理。 这是为了帮助在过去成功的解决办法的建议。

您设置了故障、诊断和解决方法设置。 在您接受维修的类似的物料时，能在以后适用所有这些。 您还可以设置能够跟踪某一维修问题的进展情况的维修阶段。

## <a name="setting-up-repair-management"></a>设置维修管理

使用以下设置窗体可以输入将用于指定维修的故障、诊断和解决方法的信息。

- **服务管理** \> **设置** \> **维修** \> **条件**。
- **服务管理** \> **设置** \> **维修** \> **故障区域**。
-  **服务管理** \> **设置** \> **维修** \> **诊断区域**。
- **服务管理** \> **设置** \> **维修** \> **解决方法**。
- **服务管理** \> **设置** \> **维修** \> **维修阶段**。

## <a name="symptoms-and-conditions"></a>故障和条件

故障是客户如何表述问题。 症状包括指示需要维修的客户观察。

您可以设置故障区域、故障代码和情况。 故障区域涉及出问题的区域，故障代码涉及出问题的故障。 在该问题发生时，条件描述仍然存在的情况或环境。

**示例**

因为硬盘在一个扩展的使用期后失败，所以为修理带来一台计算机。 硬盘故障生成一个蓝屏错误。 接收计算机的技术人员输入以下故障和条件：

1.  故障区域是硬盘

2.  故障代码是蓝屏错误

3.  该条件是硬盘在分散使用后失败

## <a name="diagnosis-and-resolutions"></a>诊断和解决方法

诊断和解决方案字段是从维修角度进行的陈述。 它们是技术人员为调查问题所执行的步骤。

诊断区域涉及为解决问题而必须执行的操作。 诊断代码指示处理问题的方式，解决方法可以是维修或更换物料，也可以是客户取消订单。 例如，如果计算机已维修，则诊断区域可以是“有缺陷部件”，诊断代码可以是“安装了新显卡”，解决方法可以是“已更换”。

## <a name="repair-stages"></a>维修阶段

维修阶段指示维修过程的进度。 维修阶段具有 **已完成** 验证参数，指示维修行已完成，并且完工日期和时间已记录。

## <a name="applying-repair-management"></a>应用维修管理

若要将维修管理应用于某一物料，必须用某一服务订单上的服务对象关系设置该物料。 然后，从该服务订单，您可以创建一个维修行，行中具有与当前问题有关的信息。 在该维修行上，您定义处于维修中的服务对象，以及与故障、诊断和执行有关的信息。 您还可以创建该维修行的备注。

可以为维修过程中的每个步骤创建维修行。

## <a name="create-a-repair-line-on-a-service-order"></a>在服务订单上创建维修行

1.  转到 **服务管理** \> **服务订单** \> **服务订单**。

2.  选择具有需要维修的服务对象的服务订单。

3.  **维修** \> **维修行** 打开 **维修行** 窗体。

4.  选择 **新建** 创建新行。

5.  选择某一服务对象。 您可以选择已用该服务订单上的对象关系设置的任何服务对象。

6.  选择在维修行中相关的任何预设故障、诊断和执行值，如果需要，然后选择 **备注** 选项卡以便创建针对该维修行的备注。

7.  选择 **保存** 保存新维修行。 使用保存时间更新 **维修行** 窗体的 **常规** 选项卡的 **创建日期和时间** 字段。

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>跟踪进度和解决维修问题

您可以设置维修行的维修阶段，以便跟踪维修的进度。

在解决某一维修问题时，可以关闭该维修行。 设置维修阶段到该启用的 **已完成** 属性的阶段。 当前日期和时间在该行上作为结束时间登记。

## <a name="close-a-repair-line-for-a-resolved-issue"></a>为已解决问题关闭维修行

1.  打开 **维修行行** 窗体。 通过执行本文前面所述的过程以创建一个维修行。

2.  选择具有您要关闭的维修问题的维修行。

3.  在 **维修阶段** 字段中，选择启用了 **已完成** 属性的阶段。

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]