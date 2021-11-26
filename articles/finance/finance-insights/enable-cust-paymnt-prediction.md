---
title: 启用客户付款预测
description: 本主题说明如何在 Finance Insights 中开启和配置客户付款预测功能。
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 16ccd7f2e11f0b46aaa646de272e668d29ccc0c0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752920"
---
# <a name="enable-customer-payment-predictions"></a>启用客户付款预测

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题说明如何在 Finance Insights 中开启和配置客户付款预测功能。 在 **功能管理** 工作区中开启功能，然后在 **Finance insights 配置** 页中输入配置设置。 本主题还包括可以帮助您有效使用该功能的信息。

> [!NOTE]
> 在完成以下步骤之前，请确保完成[配置 Finance insights](configure-for-fin-insites.md) 主题中的先决步骤。

1. 启用客户付款预测功能：

    1. 打开 **功能管理** 工作区。
    2. 选择 **检查更新**。
    3. 在 **所有** 选项卡上，搜索 **客户付款预测**。 如果您没有找到该功能，搜索 **（预览）客户付款预测**。 
    4. 启用此功能。

    现在已打开且可以配置客户付款预测功能。

2. 配置客户付款见解功能：

    1. 转到 **信用和收款 \> 设置 \> Finance insights \> 客户付款预测**。
    2. 在 **Finance insights 配置** 页的 **客户付款预测** 选项卡上，选择 **查看预测模型中使用的数据字段** 打开 **预测模型的数据字段** 页。 在那里，您可以查看用于为客户付款预测创建人工智能 (AI) 预测模型的字段的默认列表。

        要使用默认字段列表创建预测模型，请关闭 **预测模型的数据字段** 页，然后在 **Finance insights 配置** 页面上，将 **启用功能** 选项设置为 **是**。

    3. 指定“严重逾期”交易期间以定义 **严重逾期** 预测时段对您的业务的意义。

        对于每个未结发票，系统将预测三个时段的付款概率：**按时**、**预期** 和 **严重逾期**。

        - **按时** – 此时段中包含预测在交易截止日期或之前支付的付款。
        - **逾期** – 此时段中包含预计在交易截止日期之后，但在“严重逾期”交易期间开始之前支付的付款。
        - **严重逾期** – 此时段中包含预计在“严重逾期”交易期间开始之后支付的付款。

        > [!NOTE]
        > 如果更改“严重逾期”交易期间，并在创建了客户付款的 AI 预测模型之后选择 **更改逾期阈值**，将删除现有预测模型，并创建新模型。 新预测模型将根据为了定义而输入的设置把交易记录移到“严重逾期”期间。

    4. 定义完“严重逾期”交易期间之后，选择 **创建预测模型** 创建预测模型。 **Finance insights 配置** 页中的 **预测模型** 显示预测模型的状态。

        > [!NOTE]
        > 创建预测模型期间的任何时候都可以选择 **重置模型创建** 重新开始流程。

    该功能现已配置完毕，可以使用了。

开启并配置此功能，并且预测模型已创建且正在工作之后，**Finance insights 参数** 页的 **预测模型** 部分显示模型的准确性。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
