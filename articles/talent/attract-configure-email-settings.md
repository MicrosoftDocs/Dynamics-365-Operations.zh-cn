---
title: 在 Attract 中配置电子邮件设置
description: 本主题介绍如何为 Microsoft Dynamcis 365 Talent - Attract 发送的电子邮件配置设置。
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c1ebfaeb2e9bc2836bb70e87afa93484c829b6cb
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833107"
---
# <a name="configure-email-settings-in-attract"></a>在 Attract 中配置电子邮件设置

[!include [banner](includes/banner.md)]

甚至在应聘者申请您的职位之前，您的品牌就已经树立了信誉，并可以帮助您建立与应聘者之间的关系。 品牌正面形象会吸引最优秀的人才，并且会提高现有员工的忠诚。 Microsoft Dynamics 365 Talent: Attract 允许您配置电子邮件，使其体现贵公司的品牌。 因此，可以为工作应聘者在经历申请流程时提供一致的体验。

可使用 Attract 执行以下操作：

- 配置电子邮件设置，以便使用贵公司的 Microsoft Exchange 电子邮件服务帐户。 这样，应聘者就会知道电子邮件来自贵公司。 例如，可配置您的设置，使应聘者收到的电子邮件就会来自 `recruiting@contoso.com`，而不是来自 `contoso@microsoft.com`。
- 通过为电子邮件模板设置全局页眉和页脚，为所有电子邮件通信创建一致的品牌。 

> [!NOTE]
> 要将 Attract 配置为使用贵公司的电子邮件服务帐户发送电子邮件，需要综合招聘加载项。

## <a name="connect-an-email-service-account"></a>连接电子邮件服务帐户

通过连接贵公司的电子邮件服务帐户，可为工作应聘者创建品牌化电子邮件体验。 如果不连接贵公司帐户，Attract 将使用基于 Microsoft 的默认电子邮件服务帐户。

1. 选择**设置**（右上角的齿轮符号），然后选择**管理中心**。
2. 在**发送电子邮件设置**选项卡上**电子邮件服务帐户**下，选择**连接公司帐户**。

    ![在 Attract 中连接贵公司的电子邮件服务帐户](./media/attract-admin-email-service-accounts.png)

    有关如何创建共享电子邮件帐户的详细信息，请参阅[Exchange Online 中的共享邮箱](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes)。

3. 在 Microsoft 登录窗口中，使用您的企业凭证登录。
4. 如果尚未设置电子邮件服务帐户，或者如果要添加新的，请选择**添加新的服务帐户**，然后输入您的电子邮件信息。 如果您已设置了要使用的电子邮件帐户，请选择该帐户。

成功配置电子邮件服务帐户之后，会发现**电子邮件服务帐户**下列出了该帐户。

## <a name="disconnect-an-email-service-account"></a>断开电子邮件服务帐户

如果要通过 Attract 停止电子邮件通信中使用贵公司的域，可断开电子邮件服务帐户。

1. 选择**设置**（右上角的齿轮符号），然后选择**管理中心**。
2. 在**电子邮件设置**选项卡上**电子邮件服务帐户**下，选择要断开的电子邮件服务帐户旁边的**更多**按钮（具有三个直点）。
3. 选择**断开电子邮件帐户**。

    ![断开贵公司的电子邮件服务帐户](./media/attract-admin-disconnect-email-account.png)

4. 提示确认操作时，选择**断开**。

    ![确认断开贵公司的电子邮件服务帐户](./media/attract-admin-email-confirm-disconnect.png)

如果不连接其他电子邮件服务帐户，则从 Attract 发送的电子邮件将使用 Microsoft 品牌的默认电子邮件服务帐户。

## <a name="configure-email-template-settings"></a>配置电子邮件模板设置

可将贵公司的徽标图像和其他信息作为带品牌的电子邮件页眉发送。 也可以在电子邮件页脚中提供您的隐私政策和使用条款的连接。

> [!NOTE]
> 您必须遵守您的国家或地区及管辖电子邮件收件人的国家或地区的所有适用法律。 这些法律包括反垃圾邮件法规。

1. 选择**设置**（右上角的齿轮符号），然后选择**管理中心**。
2. 在**电子邮件设置**选项卡上**电子邮件模板设置**下，将要用作电子邮件页眉的图像拖到图像框，或在图像框中单击以浏览文件。 若要替换现有图像，必须首先选择其旁边的**移除**。 此图像必须是 JPEG、JPG、PNG 或 SVG 文件。 建议的图像大小为宽度为 25 与 800 像素之间，高度为 25 与 150 像素之间。 页眉的最大文件大小为 1 兆字节 (MB)。

    ![添加贵公司电子邮件页眉的图像](./media/attract-admin-email-header.png)

3. 在**你的通信隐私政策**下，提供贵公司隐私政策的链接。 在**你的通信条款和条件**下，提供贵公司使用条款的链接。

    ![为电子邮件页眉添加贵公司隐私政策和使用条款的链接](./media/attract-admin-email-footer.png)

4. 选择**保存**保存您的电子邮件模板设置。
