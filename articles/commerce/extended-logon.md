---
title: 设置和使用扩展登录
description: 本文介绍如何设置和使用 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序的扩展登录功能。
author: boycezhu
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.industry: Retail
ms.search.form: RetailFunctionalityProfile
ms.openlocfilehash: e2fc39b1b7fb34f49c061dcc324c28cf5a89277c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283687"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>设置和使用扩展登录

[!include [banner](includes/banner.md)]

本文介绍如何设置和使用 Microsoft Dynamics 365 Commerce 销售点 (POS) 应用程序的扩展登录功能。

Cloud POS (CPOS) 和 Modern POS (MPOS) 提供扩展的登录功能，允许零售商店工作人员通过使用磁条阅读器 (MSR) 扫描条码或刷卡来登录 POS 应用程序。

## <a name="set-up-extended-logon"></a>设置扩展登录

要在零售商店中为 POS 收银机设置扩展登录，请按照以下步骤操作。

1. 在 Commerce headquarters 中，转到 **Retail 和 Commerce \> 渠道设置 \> POS 设置 \> POS 配置文件 \> 功能配置文件**。 
2. 在左侧导航窗格中，选择与零售商店关联的功能配置文件。
3. 在 **功能** 快速选项卡上的 **其他登录身份验证选项** 下，根据需要将以下选项设置为 **是** 或 **否**：

    - **职员条码登录** – 如果您希望工作人员通过扫描条码登录 POS，请将此选项设置为 **是**。 
    - **职员条码登录需要密码** – 如果您希望工作人员在通过扫描条码登录 POS 时输入密码，请将此选项设置为 **是**。
    - **职员卡登录** – 如果您希望工作人员通过刷卡登录 POS，请将此选项设置为 **是**。
    - **职员卡登录需要密码** – 如果您希望工作人员在通过刷卡登录 POS 时输入密码，请将此选项设置为 **是**。

条码或卡与可分配给工作人员的凭据关联。 凭据必须至少有六个字符。 包含前五个字符的字符串必须是唯一的，将被视为用于查找工作人员的 *凭据 ID*。 其余字符用于安全验证。 例如，您有两张卡，其中一张的凭据为 12345DGYDEYTDW，另一张的凭据为 12345EWUTBDAJH。 由于这两张卡具有相同的凭据 ID，即 12345，因此无法将这两张卡同时成功分配给工作人员。

## <a name="assign-extended-logon"></a>分配扩展登录

默认情况下，只有经理可以将扩展登录分配给工作人员。 要分配扩展登录，转到 POS 中的 **扩展登录**。 然后通过在搜索字段中输入工作人员的操作员 ID 搜索工作人员。 选择工作人员，然后单击 **分配**。 在下一个页面，刷卡或扫描扩展登录以分配给工作人员。 如果成功读取刷卡或扫描，**确定** 按钮将可用。 单击 **确定** 为该工作人员保存扩展登录。

## <a name="delete-extended-logon"></a>删除扩展登录

若要删除分配给工作人员的扩展登录，使用 **扩展登录** 操作搜索工作人员。 选择工作人员，然后单击 **取消分配**。 与该工作人员关联的所有扩展登录凭据将被删除。

## <a name="use-extended-logon"></a>使用扩展登录

配置扩展登录并向工作人员分配条码或磁条后，在 POS 登录页显示时，工作人员必须刷或扫描他们的卡。 如果还需要密码才能继续登录，系统将提示工作人员输入他们的密码。

## <a name="extend-extended-logon"></a>扩展扩展登录

扩展登录功能的现成实现需要凭据的最小长度达到 6 个字符，并且前五个字符（凭据 ID）是唯一的。 它最初的用途是作为一个示例，开发人员可以进行自定义来满足特定实现的要求。 （例如，可以自定义来支持更多字符或使用不同的安全验证规则。）有关如何为扩展登录构建扩展的详细信息，请参阅[扩展 MPOS 和 Cloud POS 的扩展登录功能](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/)。

登录服务还可进行扩展来支持其他扩展登录设备，例如掌上扫描仪。 有关详细信息，请参阅 [POS 可扩展性文档](dev-itpro/pos-extension/pos-extension-overview.md)。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
