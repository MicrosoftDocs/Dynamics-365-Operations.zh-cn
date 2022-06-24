---
title: 重置卡住的批处理作业
description: 本文说明如何解决卡住的批处理作业的问题。
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: b56a16257a45dd093d10b7550b13d6a4a1ceb1f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896009"
---
# <a name="reset-stuck-batch-jobs"></a>重置卡住的批处理作业


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>签发

Microsoft Dynamics 365 Human Resources 可能遇到批处理作业在 **正在执行** 或 **正在取消** 状态下卡住而无法完成的问题。

## <a name="resolution"></a>解决方法

当批处理作业在 **正在执行** 或 **正在取消** 状态下卡主时，您可以通过强制取消作业来重置状态。 取消后，可以通过将批处理作业设置为 **正在等待** 状态来重置它。 然后，它将再次提取以在下一个计划的批处理运行中执行。

1. 在 **系统管理** 工作区中，选择 **链接** 页面，然后选择 **批处理作业**。

2. 在 **批处理作业** 列表页面上，选择需要重置的作业。

3. 在操作功能区上，选择 **强制取消**，然后确认操作。

   > [!NOTE]
   > **强制取消** 操作仅在所选批处理作业具有 **正在执行** 或 **正在取消** 状态，并且该作业没有运行批处理执行或取消流程时可用。

4. 在操作功能区上，选择 **更改状态**。

5. 在 **选择新状态** 页面上，选择 **正在等待**，然后选择 **确定**。

   ![选择新的批处理作业状态。](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>请参阅

[通过安排在下班后执行批处理作业而优化性能](hr-admin-troubleshooting-batch-jobs.md)<br>
[使用自动清理任务优化性能](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
