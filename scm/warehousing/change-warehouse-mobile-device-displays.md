---
title: "仓库移动设备的显示设置"
description: "此文章介绍如何设置移动设备显示的外观，以及如何将键盘快捷键映射到控件（例如按钮）。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 721b293d1f8c76458ca510732f9bb94f003ac6e3
ms.lasthandoff: 03/31/2017


---

# <a name="warehouse-mobile-device-display-settings"></a>仓库移动设备的显示设置

此文章介绍如何设置移动设备显示的外观，以及如何将键盘快捷键映射到控件（例如按钮）。 

本文适用于仓库管理中的“高级仓储”功能。 移动设备可用于仓库工作人员执行的很多任务。

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>指定样式和映射键盘快捷方式
作为移动设备配置的一部分，您可以为移动设备定义不同的布局。 为此，您必须知道级联样式表 (CSS) 文件和 Active Server Page Extension (ASPX) 文件的名称。 默认文件作为仓库移动设备门户安装的一部分进行安装。 如果不知道文件名，请联系系统管理员。 您可以在**“移动设备显示设置”**页上定义新样式：

-    在**“CSS 文件”**字段中，输入 CSS 文件的名称。 包含 .css 文件扩展名。
-   在**“移动设备显示设置视图”**字段中，指定 ASPX 文件。 **不**要包含 .aspx 文件扩展名。

CSS 和 ASPX 文件必须位于特定目录中，以便 Internet Information Services (IIS) 应用程序可以加载它们。 如果您在不同的浏览器中或在需要不同的布局控件的不同类型的硬件上运行移动设备功能，那么定义不同的 CSS 文件可能很有用。 简单设置（如背景色、文本的字体和字号以及按钮的宽度和行为）可以通过以不同的方式使用 CSS 文件来轻松控制。 用于在服务器端 ASP.NET 应用程序上显示移动站点的 ASPX 文件。 文件控制 HTML 的总体结构的布局方式。 建议仅当您的 HTML 和 JavaScript 遇到严重的结构问题，并且必须为特定设备更改此代码才自定义此功能。 要将移动设备页上的 HTML 控件映射到键盘快捷方式，请在**“移动设备显示设置”**页上的**键盘快捷方式**字段中分配键的数字代码。 您可使用移动设备上的**“查看键盘快捷方式的代码”**菜单查找数字字符代码。 请注意，根据所使用的硬件，映射可能不同。 必须使用以下句法创建映射：

&lt;控制=key&lt;关键字&gt;名称&gt;(&lt;名称) 代码&gt;;

下面是该语法的各个部分的说明：

-   **&lt;控制**名称&gt;–在 HTML 呈现控制 (，例如按钮) 的名称。
-   **关键字&gt;(&lt;名称) **键的键盘名称–您创建快捷方式。
-   **&lt;关键&gt;字码** –参数的字符代码可以用作快捷键。

下面是一个示例：

Cancel(Esc)=27; Full(F2)=113

在包含**“取消”**按钮的所有页面上，该按钮将具有以下文本：

**(Esc) 取消**

按键盘上的 ESC 键将启用**“取消”**按钮。 要将样式和键盘快捷方式应用于与特定设备，则必须在**“条件”**字段中创建映射。 您必须使用 .NET 正则表达式创建映射，并且该表达式必须包含由竖线 (|) 分隔的三个部分，如下所示：

Request.UserHostAddress=user&lt;主机地址&gt;_=_HostName=user&lt;主机名&gt;_=_Request.UserAgent=user&lt;代理&gt;

下面是该表达式的各个部分的说明：

-   **&lt;用户主机地址&gt;** –符合请求者 IP 地址的 .NET 正则表达式。
-   **&lt;用户主机名&gt;** –符合请求者的网络名称的 .NET 正则表达式。
-   **&lt;代理&gt;**用户–符合该查看器的标识符请求者的 .NET 正则表达式。

以下示例允许使用 Internet Explorer 8：

Request.UserHostAddress=.\*_=_HostName=。\*_=_Request.UserAgent=MSIE\\s8\\\\

您可使用移动设备上的**“查看显示设置的服务器配置”**菜单查找有关该设置的信息。

## <a name="define-text-colors-for-messages"></a>定义消息的文本颜色
您可**“移动设备文本颜色”**页控制在系统生成的消息（如错误消息）中使用的各种颜色。 例如，文本颜色可以指示消息的用途或严重性。 将显示以下类型的消息。

| 消息类型 | 描述                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 默认值      | 默认消息对所有消息使用默认颜色设置（由仓库移动设备门户的 CSS 文件定义）。                                                   |
| 错误        | 错误消息指示用户为继续操作而必须解决的问题。                                                                                             |
| 成功      | 成功消息确认操作均已成功。                                                                                                                                |
| 警告      | 警告消息告知工作人员已出现问题，或指示工作人员继续如此便可能出现问题。 但是，工作人员不必解决问题也能继续。 |

要选择颜色，请在**“选择颜色”**页上单击调色板或键入十六进制颜色代码。

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>定义移动设备上使用的日期格式
您可以扩展每个安装的可接受日期格式清单。 例如，如果您希望提供便于工作人员在移动设备上输入日期的格式，此功能可能很有用。 默认格式由用户的默认语言决定，该语言在**“用户选项”**页上的**“语言”**字段中指定。 (同一页还用于将员工与特定仓库工作。**注释用户): **仓库移动设备门户不使用**日期-时间和数字格式**字段的区域和语言设置**首选项**的页面。 要更改日期格式，您必须熟悉 Microsoft .NET Framework 的正则表达式。 有关详细信息，请参阅 [.NET Framework 正则表达式](http://go.microsoft.com/fwlink/?LinkId=391260)。 若要定义日期格式，请编辑内容位于的\\在仓库移动设备门户服务器上的\\Dates.ini 的 Dates.ini 文件。 此文件使用 .NET 正则表达式指定日期格式。 正则表达式必须包含用于创建日、月和年 (DDMMYY) 的命名组的子表达式，如下例所示：

^ (?&lt;天数&gt;\\d {0}\\(?)。&lt;月&gt;\\d {0}\\(?)。&lt;年度&gt;\\d {0} $\\。)

每个子表达式需要表示日和月的一到二位数，并需要表示年的一到四位数。 例如，以下子表达式定义了年的命名组，需要最少两位数或最多四位数：

(?&lt;年度&gt;\\d {0}\\。)

您可在同一个文件中指定多个表达式。 每个表达式必须位于单独的行上。 匹配的第一个表达式用于分析日期。

<a name="see-also"></a>请参阅
--------

[Configuration of mobile devices for warehouse work](configure-mobile-devices-warehouse.md)


