---
title: 将 Customer Voice 集成到电子商务站点页面中
description: 本文介绍如何将 Microsoft Dynamics 365 Customer Voice 集成到 Dynamics 365 Commerce 电子商务站点页面。
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: c8c67ecf4950c92fc91c8d119e06e5e8afff0ddf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850322"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>将 Customer Voice 集成到电子商务站点页面中

[!include [banner](../includes/banner.md)]

本文介绍如何将 Microsoft Dynamics 365 Customer Voice 集成到 Dynamics 365 Commerce 电子商务站点页面。

您可以将 [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) 集成到电子商务站点中，以收集、分析和跟踪实时客户反馈。 要开始集成，您必须创建一个帐户并为您要收集的反馈类型选择一个 Customer Voice 项目模板。

## <a name="integrate-the-customer-voice-service"></a>集成 Customer Voice 服务

若要创建 Customer Voice 帐户，请转到 [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) 并按照提示操作。

创建 Customer Voice 帐户并登录后，下一步是为您要收集的反馈类型选择项目模板。

若要选择 Customer Voice 项目模板，请按照以下步骤操作。

1. 转到 [Customer Voice 项目模板页面](https://customervoice.microsoft.com/Pages/ProjectPage.aspx)。
1. 选择 **开始使用**。
1. 选择您要收集的反馈类型的项目模板，然后选择 **下一步**。
1. 在 **发送** 选项卡上的 **选择嵌入格式** 下面，选择嵌入格式。 **嵌入式代码** 字段显示必须在 Commerce 站点生成器中嵌入的代码。

本文中的示例使用 **定期客户调查** 项目模板和 **按钮** 嵌入格式。

以下示例图显示了 **定期客户调查** 项目模板页面，其中选择了 **按钮** 嵌入格式的选项，并且该选项的嵌入代码显示在 **嵌入代码** 字段中。 如以下部分所述，将提供的代码嵌入您的站点页面需要执行三项单独的操作。

![已选择“按钮”选项的 Customer Voice 定期客户调查页面。](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>嵌入外部脚本 URL

在应该有 Customer Voice 调查的所有站点页面上，您必须嵌入 Customer Voice 在嵌入代码中提供的外部脚本 URL。 将脚本嵌入多个站点页面的最佳方法是在站点构建器中创建一个包含外部脚本 URL 的片段，然后将该片段添加到相应的页面模板中。 发布更新的模板后，嵌入的外部脚本代码将类似于受影响站点页面上的以下示例。

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

有关片段的信息，请参阅[使用片段](work-with-fragments.md)。

> [!NOTE]
> 您只须将 URL 添加到片段中。 外部脚本模块将添加其他脚本代码。

若要将外部脚本 URL 嵌入到片段中，请按照以下步骤操作。

1. 在站点生成器中，创建一个基于[外部脚本模块](script-module.md)的片段。
1. 在新片段中，选择 **默认外部脚本** 插槽。
1. 在 **默认外部脚本** 属性窗格中，在 **脚本来源** 字段中输入外部脚本 URL，如以下示例图中所示。

    ![新片段的脚本来源字段中的外部脚本 URL。](media/customer-voice-integration-2.png)

1. 选择 **保存**，然后选择 **完成编辑**。
1. 选择 **发布** 发布此片段。

包含嵌入式外部脚本块的新片段现已准备就绪，可以添加到适当的页面模板中。

### <a name="embed-the-external-style-sheet-code"></a>嵌入外部样式表代码

接下来，在应该有 Customer Voice 调查的所有站点页面上，您必须嵌入 Customer Voice 在嵌入代码中提供的外部样式表代码。 与上一节一样，将外部样式表代码嵌入多个站点页面的最佳方法是在站点构建器中创建一个包含样式表代码的片段，然后将该片段添加到适当的页面模板中。 嵌入式外部样式表代码将类似于以下示例代码。

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

若要将外部样式表代码嵌入到片段中，请按照以下步骤操作。

1. 在站点生成器中，创建一个基于[元标记模块](metatags-module.md)的片段。
1. 在片段中，选择 **默认元标记** 插槽。
1. 在 **默认元标记** 属性窗格中，在 **元标记** 字段中输入样式表代码，如以下示例图中所示。

    ![新片段的元标记字段中的外部样式表代码。](media/customer-voice-integration-3.png)

1. 选择 **保存**，然后选择 **完成编辑**。
1. 选择 **发布** 发布此片段。

包含嵌入式外部样式表代码的新片段现已准备就绪，可以添加到适当的页面模板中。

### <a name="embed-the-inline-script-code"></a>嵌入内联脚本代码 

接下来，在应该有 Customer Voice 调查的所有站点页面上，您必须嵌入 Customer Voice 在嵌入代码中提供的内联脚本代码。 与前面的节一样，将内联脚本代码嵌入多个站点页面的最佳方法是在站点构建器中创建一个包含内联脚本代码的片段，然后将该片段添加到适当的页面模板中。

在内联脚本代码的以下示例中，**SURVEY\_KEY** 是占位符。 **SURVEY\_KEY** 的值应与 Customer Voice 在嵌入代码中提供的实际调查键匹配。 最后一行会调用代码，以在一秒钟后呈现调查按钮，从而确保脚本有足够的时间加载。 根据您选择的调查，您可能还必须添加或更新其他元数据，例如公司名称。

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

若要将内联脚本代码嵌入到片段中，请按照以下步骤操作。

1. 在站点生成器中，创建一个基于[内联脚本模块](script-module.md)的片段。
1. 在此片段中，选择 **默认内联脚本** 插槽。
1. 在 **默认内联脚本** 属性窗格中，在 **内联脚本** 字段中输入内联脚本代码，如以下示例图中所示。

    ![新片段的内联脚本字段中的内联脚本代码。](media/customer-voice-integration-4.png)

1. 选择 **保存**，然后选择 **完成编辑**。
1. 选择 **发布** 发布此片段。

包含嵌入式内联脚本代码的新片段现已准备就绪，可以添加到适当的页面模板中。

## <a name="add-fragments-to-a-template"></a>将片段添加到模板中

创建完包含 Customer Voice 嵌入代码的片段后，您必须将它们添加到与要使用它们的站点页面相关联的页面模板中。 在以下示例图中，已将三个示例片段添加到产品详细信息页 (PDP) 模板中。

![添加到 PDP 模板的片段的示例。](media/customer-voice-integration-5.png)

发布更新后的模板后，Customer Voice 调查将显示在由模板控制的所有页面上。

有关模板的信息，请参阅[使用模板](work-with-templates.md)。

## <a name="configure-content-security-policy"></a>配置内容安全策略

默认情况下，除非完成额外配置，否则内容安全策略 (CSP) 不允许调用其他服务。 因此，发布更新后的模板后，可能无法在相关站点页面上加载调查。 要查看与 CSP 相关的错误，请打开 Web 浏览器的开发人员工具 (F12)，然后转到包含调查的页面。 与 CSP 相关的错误将显示在控制台输出中。

要在站点构建器中配置 CSP 以修复错误，请按照以下步骤操作。

1. 转到 **站点设置 \> 扩展**。
1. 在 **内容安全策略** 选项卡上，将 `https://customervoice.microsoft.com/` 添加到 **child-src** 指令。
1. 将 `https://customervoice.microsoft.com/` 添加到 **frame-src** 指令。
1. 将 `https://mfpembedcdnmsit.azureedge.net` 和 **.azureedge.net** 添加到 **img-src** 指令。

有关详细信息，请参阅[内容安全策略](manage-csp.md)。

## <a name="additional-resources"></a>其他资源

[外部脚本模块](script-module.md)

[元标记模块](metatags-module.md)

[内联脚本模块](script-module.md)

[内容安全策略](manage-csp.md)

[使用片段](work-with-fragments.md)

[使用模板](work-with-templates.md)
