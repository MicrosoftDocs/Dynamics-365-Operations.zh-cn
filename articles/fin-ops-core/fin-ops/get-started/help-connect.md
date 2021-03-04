---
title: 配置 Finance and Operations 应用的帮助体验
description: 此主题介绍某些 Microsoft Dynamics 365 应用的帮助系统组件。 还介绍如何连接这些应用和提供有关自定义帮助创建流程的摘要。
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0495bbc008ed1760b98c2c1ace63fc4a8b1ab5cc
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694413"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>配置 Finance and Operations 应用的帮助体验

[!include [banner](../includes/banner.md)]

在此主题中，将概述 Finance and Operations 应用（如 Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce 和 Dynamics 365 Human Resources）的帮助系统组件。 此主题还介绍如何连接这些组件和提供有关自定义帮助创建流程的摘要。

## <a name="help-architecture"></a>帮助体系结构

Finance and Operations 应用中包含已发布到 [https://docs.microsoft.com/dynamics365](/dynamics365/) 站点的概念性概述和其他主题。 然后，可从产品内的 **帮助** 窗格访问此内容。 下图显示此帮助系统的各个部分。

[![帮助体系结构](./media/help-architecture.png)](./media/help-architecture.png)

产品内帮助系统从 docs.microsoft.com 和其他相连网站提取文章。 还提取 Microsoft Dynamics Lifecycle Services (LCS) 中的业务流程建模器 (BPM) 内存储的任务指南。

## <a name="adding-task-guides"></a>添加任务指南

> [!NOTE]
> Human Resources 或 Commerce 中现在无 **任务指南** 选项卡。 <!--We are currently working to enable this functionality in a future release.--> 但是，Human Resources 中的入门中的任务指南体验可用，以涵盖基本功能。 [https://docs.microsoft.com/dynamics365](/dynamics365/) 站点中提供 Human Resources 和 Commerce 的过程帮助。

系统管理员可在 **系统参数** 页中配置对实施的相关任务指南库的访问。

> [!NOTE]
> - 若要配置帮助，必须通过使用与部署应用的租户相同的租户中的帐户登录。
> - 不能从本地虚拟硬盘 (VHD) 上正在运行的应用实例访问 LCS 库。

[![具有帮助设置的系统参数窗体](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

若要配置解决方案的任务指南，请在 **系统参数** 页中执行以下步骤。

> [!IMPORTANT]
> 首次打开 **帮助** 选项卡时，必须连接到 Lifecycle Services。 请确保选择窗体中间的链接，等待连接，关闭对话框，单后选择 **确定** 以转至 **系统参数** 页面。
>
> [![连接到 LCS](./media/connect-to-lcs-crop-1024x365.png "连接到 LCS")](./media/connect-to-lcs-crop.png)

1. 选择要连接到的 Lifecycle Services 项目。
2. 选择要从中检索任务录制的 BPM 库（在所选项目内）。
3. 选择 BPM 库的显示顺序。 此显示顺序定义库中的任务录制在 **帮助** 窗格中的显示顺序。

完成这些步骤后，您可以打开 **帮助** 窗格并选择 **任务指南** 选项卡。您现在将看到适用于您当前在 Finance and Operations 应用中所处页面的任务指南。 如果未找到任何任务指南，您可以输入关键字来调整搜索。

### <a name="showing-translated-task-guides"></a>显示翻译的任务指南

翻译的任务指南首次随 2016 年 5 月 APQC 标准库和入门库发布。 若要查看已本地化的任务指南帮助，请确保您的 Dynamics 365 解决方案已连接到 2016 年 5 月库。 用户可通过更改 **选项** &gt; **首选项** 下的语言设置，更改用于显示任务指南的语言。

> [!NOTE]
> 虽然许多任务指南已被翻译了，但是客户端现在不显示翻译的任务指南名称。 此外，在 2016 年 5 月库中仅提供在 2016 年 2 月发布的任务指南的翻译。 Microsoft 将发布包含其它翻译的更新库。
>
> - 如果已翻译任务指南，在您打开任务指南时，所有任务指南文本都将显示为您选择的语言。
> - 如果尚未翻译任务指南，在您打开任务指南时，仅部分文本（控制文本）显示为您选择的语言。

## <a name="adding-custom-help"></a>添加自定义帮助

您可以使用任务指南创建自定义帮助，也可以将自定义帮助网站连接到 **帮助** 窗格。

### <a name="create-custom-help-by-using-task-guides"></a>使用任务指南创建自定义帮助

您可以通过创建反映您的实施的任务录制并将其保存到 LCS 中的业务流程库，为支持的应用创建自定义帮助。 您无法为 Human Resources 创建自定义任务指南。

如果您是合作伙伴，并且您要将一个库提升到公司库并将其包括到解决方案中，它将可供您的客户使用。 您还可以复制 APQC Unified 库，然后打开副本中的任务录制，进行编辑，再保存所做更改。 有关详细信息，请参阅[任务录制器资源](../../dev-itpro/user-interface/task-recorder.md)。

### <a name="connect-a-custom-help-site"></a>连接自定义帮助站点

Finance and Operations 应用很少以现成格式使用。 相反，将自定义并扩展此解决方案以满足组织的需要。 还可以自定义和扩展帮助体验。 例如，可以向产品内 **帮助** 窗格添加自定义帮助。

Microsoft 提供了工具提示，以帮助您开发自定义帮助和将其连接到 **帮助** 窗格。 有关如何设置连接到 **帮助** 窗格的自定义帮助解决方案的信息，请参阅[自定义帮助概述](../../dev-itpro/help/custom-help-overview.md)。

如果要与 Microsoft 合作处理用于自定义帮助的工具和流程，请填写 [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback) 中的表单。

## <a name="see-also"></a>请参阅

[帮助系统](help-overview.md)  
[自定义帮助概述](../../dev-itpro/help/custom-help-overview.md)  
[任务录制器资源](../../dev-itpro/user-interface/task-recorder.md)  
[通过任务录制器创建文档或培训](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[自定义帮助 GitHub 知识库](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]