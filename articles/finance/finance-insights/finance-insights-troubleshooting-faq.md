---
title: 解决 Finance Insights 设置问题
description: 本主题列出了您使用 Finance Insights 功能时可能会出现的问题。 它还介绍了如何解决这些问题。
author: panolte
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: f3cac30a66ff3a74a7f67c11dd9fa14af79d10af
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752609"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>解决 Finance Insights 设置问题

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题列出了您使用 Finance Insights 功能时可能会出现的问题。 它还介绍了如何解决这些问题。

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>症状：为什么我无法映射客户付款见解数据集成模板目标列？

### <a name="resolution"></a>解决方法

您可能正在使用早期版本的模板。 在 10.0.17 版本发布之前，预览版客户使用 **付款预测结果（预览版）** 实体配置了 **客户付款见解结果（CDS 到 Fin and Ops）** 数据集成 (DI) 模板。 升级到 10.0.17 及更高版本后，您应该使用 **客户付款见解结果（CDS 到 Fin and Ops 10.0.17 及更高版本）** DI 模板来完成映射。 在刷新数据管理实体列表并且其中出现 **付款预测结果** 实体之前，您可能无法映射 DI 模板目标列。 若要刷新实体列表并显示付款预测结果，您将在 Microsoft Dynamics 365 Finance和 Dataverse（以前称为 Common Data Service\[CDS \] 管理员门户）中完成相关步骤。

### <a name="in-finance"></a>在 Finance 中

升级后在 Finance 中执行以下步骤。

1. 转到 **系统管理 \> 工作区 \> 数据管理**。
2. 在 **数据管理** 工作区中，选择 **框架参数** 磁贴。
3. 在 **数据导入/导出框架参数** 页面上，选择 **实体设置**，然后选择 **刷新实体列表**。
4. 关闭 **数据导入/导出框架参数** 页。
5. 在 **数据管理** 工作区中，选择 **数据实体** 磁贴。
6. 搜索“付款预测结果”。 验证 **付款预测结果** 实体是否不是预览版。 预览版本的名称以“（预览版）”结尾。 如果您只看到实体的预览版本，请与 Microsoft 支持人员联系。

### <a name="in-dataverse"></a>在 Dataverse 中

在 [Power Platform 管理中心](https://admin.powerplatform.microsoft.com/environments)中执行这些步骤，以更新您的数据集成项目。

1. 如果您使用的是 Finance Insights 预览版，请删除与 **客户付款见解结果（CDS 到 Fin and Ops）** 模板关联的 DI 项目。
2. 按照[创建数据集成器项目](create-data-integrate-project.md)中的步骤操作。 使用 **客户付款见解结果（CDS 到 Fin and Ops 10.0.17 及更高版本）** 模板。

## <a name="symptom-when-i-try-to-open-ai-builder-by-using-the-links-on-the-customer-payment-predictions-setup-page-why-do-i-receive-the-following-error-message-sorry-theres-been-a-disconnect"></a>问题：当我尝试使用客户付款预测设置页面上的链接打开 AI Builder 时，为什么会收到以下错误消息：“抱歉，已断开连接”？

### <a name="resolution"></a>解决方法

Dynamics 365 Finance 用户必须具有环境的 Microsoft Power Apps 用户帐户，并且该用户帐户必须具有系统定制员角色。 Microsoft Power Apps 系统管理员可以创建此用户帐户并分配角色。 然后，您可以转到 <https://make.preview.powerapps.com/>，使用该用户帐户登录，然后再次尝试链接。

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>症状：为什么“现金流预测”工作区中的“现金预测”选项卡未显示任何数据？

### <a name="resolution"></a>解决方法

必须设置并启用“现金和银行管理”中的现金流预测功能以及 Finance Insights 中的现金流预测功能，才能在 **现金流预测** 工作区中正确显示数据。

首先，设置并启用现金流预测和流动性帐户。 有关详细信息，请参阅[现金流预测](../cash-bank-management/cash-flow-forecasting.md)。 如果此设置已完成，但您看不到所期望的结果，请参阅[现金流预测设置疑难解答](../cash-bank-management/cash-flow-forecasting-tsg.md)，以了解详细信息。

接下来，确认已启用 Finance Insights（**现金和银行管理设置 \> 设置 \> Finance Insights \> 现金流预测**）中的现金流预测功能，并且已完成 AI 模型训练。 如果尚未完成训练，请选择 **立即预测** 以启动模型训练流程。
