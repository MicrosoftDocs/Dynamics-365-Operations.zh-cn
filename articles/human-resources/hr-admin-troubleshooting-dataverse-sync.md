---
title: 重置 Dataverse 同步
description: 本主题介绍如何解决 Microsoft Dynamics 365 Human Resources 与 Microsoft Dataverse 中人力资本管理 (HCM) 公共解决方案之间无法正确同步的记录问题。
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 8bfcd51b023c02590919155abbb836326408d298
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696226"
---
# <a name="reset-dataverse-synchronization"></a>重置 Dataverse 同步


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>问题

在 Microsoft Dynamics 365 Human Resources 与 Microsoft Dataverse 内人力资本管理 (HCM) 公共解决方案中的实体之间未同步记录。 有关同步的详细信息，请转到[配置 Dataverse 集成](hr-admin-integration-common-data-service.md)。 当 **Dataverse 集成重试** 或 **Dataverse 集成缺少请求同步** 批处理作业卡在 **正在执行** 状态时，可能会出现无法正确同步的情况。

## <a name="resolution"></a>解决方法

当 **Dataverse 集成重试** 或 **Dataverse 集成错过的请求同步** 批处理作业卡在 **正在执行** 或 **正在取消** 状态时，您可以重置状态。 通过在[重置卡住的批处理作业](hr-admin-troubleshooting-batch-execution.md)中遵循指导来取消批处理作业，可以完成此操作。 取消批处理作业后，可以通过将批处理作业设置为 **正在等待** 状态来重置它。 然后，批处理作业将在下一个计划的运行时间期间内运行。

1. 如果您尚未执行此操作，请在 **功能管理** 中启用 **增强型批处理中止** 功能。
   1. 转到 **功能管理** 页面（**系统管理** > **摘要** > **功能管理**）。
   2. 选择 **全部** 选项卡。
   3. 选择 **功能名称** 列并按 **增强型批处理中止** 进行筛选。
   4. 如果 **启用** 操作尚未启用，请选择它。

2. 关闭 Dataverse 集成。
   1. 转到 **Microsoft Dataverse 集成** 页面（从 **系统管理** 转到 **链接** > **集成** > **Dataverse 配置**）。
   2. 将 **启用 Dataverse 集成** 设置为 **否**。

3. 取消 **Dataverse 集成重试** 批处理作业。
   1. 转到 **批处理作业** 页面（从 **系统管理** 转到 **链接** > **批处理作业** > **批处理作业**）。
   2. 按 **集成** 筛选 **作业描述** 列。
   3. 取消 **Dataverse 集成重试** 批处理作业。
   4. 在操作功能区上，选择 **批处理作业**、**强制取消**，然后选择 **是** 以确认。

   > [!NOTE]
   > 根据首次启用集成的时间，批处理作业可能具有 **Common Data Service 集成重试** 说明。 如果列出了此批处理作业，则选择此批处理作业，而不是 **Dataverse 集成重试** 批处理作业。

4. 删除所有 Dataverse 集成批处理作业。
   1. 在 **批处理作业** 页面上，选择 **Dataverse 集成错过的请求同步**、**Dataverse 集成重试** 和 **Dataverse 集成初始同步** 批处理作业。
   2. 在操作功能区上，选择 **更改状态** 操作。 
   3. 选择 **预扣**，然后选择 **确定**。
   4. 在操作功能区上，选择 **删除** 操作，然后选择 **是** 以确认此操作。

5. 启用 Dataverse 集成批处理作业。
   1. 转到 **Microsoft Dataverse 集成** 页面（**系统管理** > **链接** > **集成** > **Dataverse 配置**）。
   2. 将 **启用 Dataverse 集成** 设置为 **是**。

6. 转到 **批处理作业** 页面，并确认已创建 **Dataverse 集成重试** 和 **Dataverse 集成错过的请求同步** 批处理作业。

重新创建批处理作业后，您现在可以监视 **Dataverse 集成重试** 批处理作业，以查看执行该作业所需的时间。 然后，您可以验证记录是否会正确同步到 Microsoft Dataverse 中的 HCM 通用解决方案。

## <a name="see-also"></a>请参阅

[配置 Dataverse 集成](hr-admin-integration-common-data-service.md)<br>
[重置卡住的批处理作业](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
