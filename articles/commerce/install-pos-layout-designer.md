---
title: 安装 POS 布局设计器
description: 您可以使用一键式设计器在横向或纵向模式下为商店、收银机、出纳和经理设计不同的 Modern POS (MPOS) 和 Cloud POS 布局。
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.industry: Retail
ms.search.form: RetailTillLayout
ms.openlocfilehash: a610dbb9db63236ae7d182692f45f21c56982c69
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274251"
---
# <a name="install-the-pos-layout-designer"></a>安装 POS 布局设计器

[!include [banner](includes/banner.md)]

您可以使用一键式设计器在横向或纵向模式下为商店、收银机、出纳和经理设计不同的 Modern POS (MPOS) 和 Cloud POS 布局。

MPOS 或 Cloud POS 的图形设计界面由钱柜布局控制。 格式控制各种对象的位置。 示例包括总体布局、物料网格布局、客户版式、付款版式和各种菜单按钮格式。 布局还包括销售界面显示给销售人员的整体外观。

## <a name="install-the-one-click-designer"></a>安装一键式设计器。

1. 在 Commerce 中，使用左上角的菜单导航到 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS** &gt; **屏幕布局**。
2. 选择应用程序类型为 **适用于 Windows 的 Modern POS** 或 **云 POS** 的任何布局，然后单击 **布局设计器**。
3. 在出现在 Internet Explorer 窗口底部的通知栏上，单击 **打开** 开始安装一键式设计器。 （通知栏可能在其他浏览器的不同位置显示。）
4. 在显示的 **应用程序运行 - 安全警告** 消息框中，单击 **运行** 以安装 Retail 设计器主机。 进度指示器显示安装进度。
5. 在安装完成后，在 **登录** 页面输入您的 Commerce 用户名和密码，然后单击 **登录** 启动设计器。
6. 在您的凭据验证和设计器启动后，可以开始设计自己的布局或修订现有布局。

    [![一键式设计器中的布局。](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>布局设计器安装疑难解答

- 单击 **设计器** 时，不显示下载（或运行）安装程序的提示，或者您当前的安全设置不允许您下载文件。 

    **解决方案：**

    - 在 Internet Explorer 中，确保对此站点禁用弹出窗口阻止程序。 单击 **设置** &gt; **选项** &gt; **隐私** &gt; **查找弹出窗口阻止程序**，必要时更改设置。
    - 在 Internet Explorer 中，将 Commerce URL 添加到受信任的站点中。 单击 **设置** &gt; **选项** &gt; **安全** &gt; **受信任的站点** &gt; **站点** &gt; **添加**。

- 程序不开始，并且指示您联系供应商。

    **解决方案：** 在 Internet Explorer 中，将 Commerce URL 添加到受信任的站点中。 单击 **设置** &gt; **选项** &gt; **安全** &gt; **受信任的站点** &gt; **站点** &gt; **添加**。

**已知问题：** 设计器在 Google Chrome 和 Mozilla Firefox 浏览器中无法正常运行。 我们正在努力修复此问题。

## <a name="additional-resources"></a>其他资源

[配置、安装和激活 Retail Modern POS (MPOS)](retail-modern-pos-device-activation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
