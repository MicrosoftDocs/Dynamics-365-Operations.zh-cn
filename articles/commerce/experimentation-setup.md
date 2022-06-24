---
title: 设置试验
description: 本文介绍了如何在第三方服务中设置试验。
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946158"
---
# <a name="set-up-an-experiment"></a>设置试验

在[定义假设并确定您要使用哪些成功指标](experimentation-identify.md)后，您需要在第三方服务中设置试验。 下图显示了在 Dynamics 365 Commerce 中的电子商务网站上设置和运行试验所涉及的所有步骤。 其他步骤在单独的文章中介绍。

[![试验用户旅程 - 设置。](./media/experimentation_setup.svg)](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>在第三方服务中设置试验
到目前为止，您应该已经选择了第三方服务来运行和监视您的试验，并设置了试验连接器。 这些先决条件在 [Dynamics 365 Commerce 中的试验](experimentation-overview.md)中列出。

请按照在第三方服务中创建试验所需的步骤进行操作。 如果连接器配置正确，则您在第三方服务中设置的试验的完整列表将在大约 5 分钟内显示在 Commerce 站点构建器中。

## <a name="set-up-your-success-metrics"></a>设置您的成功指标
每个试验都需要指标来度量变体的影响和验证假设。 请按照以下步骤使用 Dynamics 365 Commerce 中的实时遥测事件来在第三方服务中启用指标计算。

要为现成模块设置成功指标，请按照这些步骤操作。

1. 在 Commerce 站点构建器中，选择左侧导航窗格中的 **页面**，然后选择要为其收集指标的页面。 
1. 转到您要跟踪的页面或模块的右侧属性窗格中的 **要跟踪的事件 ID** 部分。
1. 选择 **查看**。 将显示所有点击事件 ID 的列表。 复制您要跟踪的事件，然后将事件密钥粘贴到第三方服务中的指定位置。 如果您需要多个事件，则一次复制一个密钥。 
1. 对于页面视图，请在追加了 `.PageView` 的站点构建器中使用页面名称的 SHA-256 哈希值。 例如，`Homepage.PageView` 的事件 ID 将为 `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`。
1. 根据第三方服务的要求，采取任何其他步骤来跟踪指标。

对于自定义模块点击，请按照这些步骤来检测点击事件：

1. 使用下面的函数为模块准备 **TelemetryContent** 对象。 此函数将页面名称、模块名称和 SDK 提供的默认遥测对象作为输入。

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    下面是一个示例： 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. 创建包含有关需要捕获的内容的信息的有效负载数据。 对于按钮和其他静态控件，您可以包括 **电子文本**，如“立即购买”或“搜索”。 对于具有点击（如点击产品卡）的组件，您可以发送 **recid**，即产品的记录 ID 或产品 ID。

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    一个静态控件的示例：传递如下所示的按钮文本字符串：

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    一个产品点击的示例：传递如下所示的产品 recordId：

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. 调用 **OnClick** 函数注册事件。

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    下面是一个示例：

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>上一步
[标识假设并确定试验指标](experimentation-identify.md) 


## <a name="next-step"></a>后续步骤
[连接和编辑试验](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
