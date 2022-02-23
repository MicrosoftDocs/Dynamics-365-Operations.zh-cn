---
title: 启用客户付款预测(预览)
description: 本主题说明如何在 Finance Insights 中开启和配置客户付款预测功能。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e10aa9342ec9f089ef8ecec5e1221a31c580fc87
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644985"
---
# <a name="enable-customer-payment-predictions-preview"></a>启用客户付款预测(预览)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题说明如何在 Finance Insights 中开启和配置客户付款预测功能。 在 **功能管理** 工作区中开启功能，然后在 **Financial insights 参数** 页中输入配置设置。 本主题还包括可以帮助您有效使用该功能的信息。

> [!NOTE]
> 在完成以下步骤之前，请确保完成[配置 Finance insights](configure-for-fin-insites.md) 主题中的先决步骤。

1. 按照 Microsoft Dynamics Lifecycle Services (LCS) 中环境页面内的信息连接到该环境的 Azure SQL 主实例。 运行以下 Transact-SQL (T-SQL) 命令为沙盒环境开启外部测试版。 （可能必须先在 LCS 中为 IP 地址开启访问权限，才能远程连接到应用程序对象服务器 \[AOS\]。）

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > 如果您的 Microsoft Dynamics 365 Finance 部署是 Service Fabric 部署，则可跳过此步骤。 Finance Insights 团队应该已经为您开启了外部测试版。 如果在 **功能管理** 工作区中看不到此功能，或者如果尝试打开该功能时遇到此问题，请联系 <fiap@microsoft.com>。

2. 开启客户付款见解功能：

    1. 转到 **系统管理 \> 工作区 \> 功能管理**。
    2. 找到名称为 **客户付款见解（预览）** 的功能。
    3. 选择 **立即启用**。

    现在已打开且可以配置客户付款见解功能。

3. 配置客户付款见解功能：

    1. 转到 **信用和收款 \> 设置 \> Finance insights \> Finance insights 参数**。

        [![配置此功能之前的“Financial insights 参数”页](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. 在 **Financial insights 参数** 页的 **客户付款见解** 选项卡上，选择 **查看预测模型中使用的数据字段** 链接打开 **预测模型的数据字段** 页。 在那里，您可以查看用于为客户付款预测创建人工智能 (AI) 预测模型的字段的默认列表。

        要使用默认字段列表创建预测模型，请关闭 **预测模型的数据字段** 页，然后在 **Financial insights 参数** 页面上，将 **启用功能** 选项设置为 **是**。

    3. 指定“严重逾期”交易期间以定义 **严重逾期** 预测时段对您的业务的意义。

        对于每个未结发票，系统将预测三个时段的付款概率：**按时**、**预期** 和 **严重逾期**。

        - **按时** – 此时段中包含预测在交易截止日期或之前支付的付款。
        - **逾期** – 此时段中包含预计在交易截止日期之后，但在“严重逾期”交易期间开始之前支付的付款。
        - **严重逾期** – 此时段中包含预计在“严重逾期”交易期间开始之后支付的付款。

        > [!NOTE]
        > 如果更改“严重逾期”交易期间，并在创建了客户付款的 AI 预测模型之后选择 **更改逾期阈值**，将删除现有预测模型，并创建新模型。 新预测模型将根据为了定义而输入的设置把交易记录移到“严重逾期”期间。

    4. 定义完“严重逾期”交易期间之后，选择 **创建预测模型** 创建预测模型。 **Financial insights 参数** 页中的 **预测模型** 显示预测模型的状态。

        > [!NOTE]
        > 创建预测模型期间的任何时候都可以选择 **重置模型创建** 重新开始流程。

    该功能现已配置完毕，可以使用了。

开启并配置此功能，并且预测模型已创建且正在工作之后，**Financial insights 参数** 页的 **预测模型** 部分显示模型的准确性，如下图中所示。

[![“Financial insights 参数”页的预测模型的准确性](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>发布详细信息

Finance insights 公开预览版可用于美国、欧洲和英国的试用部署。 Microsoft 将逐渐增加对更多地区的支持。

可以并且应该仅在第 2 层沙盒环境中启用公开预览版功能。 在沙盒环境中创建的设置和 AI 模型不能迁移到生产环境。 有关详细信息，请参阅 [Microsoft Dynamics 365 Previews 补充使用条款](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms)。

## <a name="privacy-notice"></a>隐私声明

预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。
