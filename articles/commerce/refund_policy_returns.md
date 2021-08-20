---
title: 为渠道创建和更新退货和退款政策
description: 本主题说明了如何为渠道设置退货和退款政策。
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 5c32156aea5f43d41b51f34b45b5b6dfedb5cad0f948924ecea9b3d89e6bb402
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763684"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>创建和更新渠道的退货和退款政策

[!include [banner](includes/banner.md)]

利用 Dynamics 365 Commerce 中的渠道退货政策，零售商能够就使用哪些支付方式在销售点 (POS) 设备上处理退货设置强制措施。  

本主题描述了为渠道设置退货和退款政策的步骤。

目前，该政策的范围仅限于设置可以允许渠道使用的付款方式。 “允许”列表基于用于进行购买的付款方式。 例如:

- 如果使用礼品卡进行购买，则商店政策是仅对新礼品卡处理退款或提供商店信用。 
- 如果使用现金进行销售，则退款可以使用的选项包括现金、礼品卡和客户帐户，而不是信用卡。 

## <a name="enable-return-policy"></a>启用退货政策

要在 Commerce Headquarters 中启用渠道退货政策功能，请按照下列步骤操作。

1. 转到 Dynamics 365 Commerce 中的 **功能管理** 工作区。
1. 在功能名称列表中搜索 **启用渠道退货政策** 功能。
1. 选择 **立即启用**。
1. 在 **分配计划** 页面上，运行 **1110**（全局配置）作业以分配功能更改。

## <a name="initialize-the-commerce-scheduler"></a>初始化 Commerce 计划程序

启用 **启用渠道退货政策** 功能后，您必须初始化 Commerce 计划程序以确保通过 Commerce Data Exchange (CDX) 同步添加新的功能数据库更改。 

要在 Commerce headquarters 中初始化 Commerce 计划程序，请按照下列步骤操作。

- 转到 **Retail 和 Commerce \> Headquarters 设置 \>  商业调度 \> 初始化商业调度**。 或者，您可以搜索“初始化 Commerce 计划程序”。
- 在 **初始化 Commerce 计划程序** 对话框中，确保 **删除现有配置** 选项设置为 **否**，然后选择 **确定**。

## <a name="configure-return-policy"></a>配置退货政策

请按照以下步骤配置零售商店或在线零售渠道的退货政策。

1. 转到 **Retail 和 Commerce** \>**频道设置** \> **退货** \> **渠道退货政策**。

1. 选择 **新建** 以创建新的退货政策模板。 若要使用现有模板，请在左窗格中选择模板。 对于新模板，请添加名称和描述，以帮助您将政策应用于渠道时识别该政策。

   ![添加新退货策略。](media/Return-policy-page1.png)
     
   
1. 在 **允许的退款付款方式** 部分中，定义特定于每种付款方式的 **已允许** 退货付款方式。
   ![设置每种付款类型允许的付款方式。](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - 付款方式源自为组织设置的付款方式。
    > - 为每种列出的付款方式添加允许的退货支付方式将确保可以针对允许的退货支付方式进行退货。
    
1. 将退货政策模板与其使用商店关联。 选择 **零售渠道** 选项卡中的 **添加** 选项卡并关联可用渠道。 

    - 在 **选择组织节点** 对话框中，选择应与模板关联的商店、地区和组织。
    - 只能为每个商店关联一个退货政策模板。
    - 使用箭头按钮选择商店、地区或组织。
    - 政策生效日期将是将政策应用于渠道并运行渠道作业的日期。 

    ![选择组织节点对话框。](media/Return-policy-page3.png)

1. 在 **配送计划** 页面上，运行 **1070** 作业以使渠道退货政策可用于 POS。

## <a name="preview-the-channel-return-policy-in-the-pos"></a>预览 POS 中的渠道退货政策

请按照以下任一示例中的步骤操作，以查看 POS 中允许使用的退货支付方式。

1. 以收银员或经理身份登录到 POS。
1. 在 **班次和银箱** 下面，选择 **显示日记帐**。
1. 选择属于退货的交易记录。 
1. 选择要退款的商品，然后选择付款方式。  
    - 如果所选的付款方式在允许的退货支付方式列表中，则出纳员可以完成交易。
    - 如果不允许使用所选的付款方式，则会显示错误消息。
    - 选择 **应付金额** 以显示所有允许的退货支付方式的列表。

- 或者 -

1. 以收银员或经理身份登录到 POS。
1. 选择 **退货交易**，然后通过条形码扫描或手动输入来输入收据 ID。 
1. 选择属于退货的交易记录。 
1. 选择要退款的商品，然后选择付款方式。  
    - 如果所选的付款方式在允许的退货支付方式列表中，则出纳员可以完成交易。
    - 如果不允许使用所选的付款方式，则会显示错误消息。
    - 选择 **应付金额** 以显示所有允许的退货支付方式的列表。

![不允许的退款类型。](media/Return-policy-page6.png)



![允许的退款类型。](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
