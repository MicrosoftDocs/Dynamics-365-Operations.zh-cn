---
title: 仓库移动设备的显示设置
description: 此文章介绍如何设置移动设备显示的外观，以及如何将键盘快捷键映射到控件（例如按钮）。
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28d7db2e8a4d9afef9caa106c059a6f5d0e87ce6
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/19/2019
ms.locfileid: "859751"
---
# <a name="warehouse-mobile-device-display-settings"></a><span data-ttu-id="47fab-103">仓库移动设备显示设置</span><span class="sxs-lookup"><span data-stu-id="47fab-103">Warehouse mobile device display settings</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="47fab-104">已弃用此功能。</span><span class="sxs-lookup"><span data-stu-id="47fab-104">This feature has been deprecated.</span></span> <span data-ttu-id="47fab-105">有关详细信息，请参阅[已删除或弃用的功能](../../dev-itpro/migration-upgrade/deprecated-features.md#warehouse-mobile-devices-portal)。</span><span class="sxs-lookup"><span data-stu-id="47fab-105">For more information, see [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md#warehouse-mobile-devices-portal).</span></span>

<span data-ttu-id="47fab-106">此文章介绍如何设置移动设备显示的外观，以及如何将键盘快捷键映射到控件（例如按钮）。</span><span class="sxs-lookup"><span data-stu-id="47fab-106">This article describes how to set up the appearance of a mobile device display and map keyboard shortcuts to controls such as buttons.</span></span> 

<span data-ttu-id="47fab-107">本文适用于仓库管理中的“高级仓储”功能。</span><span class="sxs-lookup"><span data-stu-id="47fab-107">This article applies to "advanced warehousing" features in Warehouse management.</span></span> <span data-ttu-id="47fab-108">移动设备可用于仓库工作人员执行的很多任务。</span><span class="sxs-lookup"><span data-stu-id="47fab-108">Mobile devices can be used for many of the tasks that warehouse workers perform.</span></span>

## <a name="specify-styles-and-map-keyboard-shortcuts"></a><span data-ttu-id="47fab-109">指定样式和映射键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="47fab-109">Specify styles and map keyboard shortcuts</span></span>
<span data-ttu-id="47fab-110">作为移动设备配置的一部分，您可以为移动设备定义不同的布局。</span><span class="sxs-lookup"><span data-stu-id="47fab-110">As part of the mobile device configuration, you can define different layouts for mobile devices.</span></span> <span data-ttu-id="47fab-111">为此，您必须知道级联样式表 (CSS) 文件和 Active Server Page Extension (ASPX) 文件的名称。</span><span class="sxs-lookup"><span data-stu-id="47fab-111">To do this, you must know the name of the Cascading Style Sheets (CSS) file and the Active Server Page Extension (ASPX) file.</span></span> <span data-ttu-id="47fab-112">默认文件作为仓库移动设备门户安装的一部分进行安装。</span><span class="sxs-lookup"><span data-stu-id="47fab-112">Default files are installed as part of the Warehouse Mobile Devices Portal installation.</span></span> <span data-ttu-id="47fab-113">如果不知道文件名，请联系系统管理员。</span><span class="sxs-lookup"><span data-stu-id="47fab-113">If you don’t know the file names, ask your system administrator.</span></span> <span data-ttu-id="47fab-114">您可以在**移动设备显示设置**页上定义新样式：</span><span class="sxs-lookup"><span data-stu-id="47fab-114">You can define a new style on the **Mobile device display settings** page:</span></span>

-    <span data-ttu-id="47fab-115">在**CSS 文件**字段中，输入 CSS 文件的名称。</span><span class="sxs-lookup"><span data-stu-id="47fab-115">In the **CSS file** field, enter the name of your CSS file.</span></span> <span data-ttu-id="47fab-116">包含 .css 文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="47fab-116">Include the .css file name extension.</span></span>
-   <span data-ttu-id="47fab-117">在**移动设备显示设置视图**字段中，指定 ASPX 文件。</span><span class="sxs-lookup"><span data-stu-id="47fab-117">In the **Mobile device display settings view** field, specify the ASPX file.</span></span> <span data-ttu-id="47fab-118">**不**要包含 .aspx 文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="47fab-118">Do **not** include the .aspx file name extension.</span></span>

<span data-ttu-id="47fab-119">CSS 和 ASPX 文件必须位于特定目录中，以便 Internet Information Services (IIS) 应用程序可以加载它们。</span><span class="sxs-lookup"><span data-stu-id="47fab-119">The CSS and ASPX files must be located in a specific directory, so that the Internet Information Services (IIS) application can load them.</span></span> <span data-ttu-id="47fab-120">如果您在不同的浏览器中或在需要不同的布局控件的不同类型的硬件上运行移动设备功能，那么定义不同的 CSS 文件可能很有用。</span><span class="sxs-lookup"><span data-stu-id="47fab-120">It might be useful to define different CSS files if you're running the mobile device functionality in different browsers or on different kinds of hardware that require different layout control.</span></span> <span data-ttu-id="47fab-121">简单设置（如背景色、文本的字体和字号以及按钮的宽度和行为）可以通过以不同的方式使用 CSS 文件来轻松控制。</span><span class="sxs-lookup"><span data-stu-id="47fab-121">Simple settings such as the background color, the font and font size for text, and the width and behavior of buttons, can easily be controlled by different use of CSS files.</span></span> <span data-ttu-id="47fab-122">用于在服务器端 ASP.NET 应用程序上显示移动站点的 ASPX 文件。</span><span class="sxs-lookup"><span data-stu-id="47fab-122">The ASPX file is used to display the mobile site on the server-side ASP.NET application.</span></span> <span data-ttu-id="47fab-123">文件控制 HTML 的总体结构的布局方式。建议仅当您的 HTML 和 JavaScript 遇到严重的结构问题，并且必须为特定设备更改此代码才自定义此功能。</span><span class="sxs-lookup"><span data-stu-id="47fab-123">The file controls how the overall structure of the HTML is laid out. It's a good idea to customize this functionality only if you have serious structural issues with the HTML and JavaScript, and must change this code for your specific devices.</span></span> <span data-ttu-id="47fab-124">要将移动设备页上的 HTML 控件映射到键盘快捷方式，请在**移动设备显示设置**页上的**键盘快捷方式**字段中分配键的数字代码。</span><span class="sxs-lookup"><span data-stu-id="47fab-124">To map the HTML controls on the mobile device page to keyboard shortcuts, on the **Mobile device display settings** page, in the **Keyboard shortcut** field, assign the numeric codes for the keys.</span></span> <span data-ttu-id="47fab-125">您可使用移动设备上的**查看键盘快捷方式的代码**菜单查找数字字符代码。</span><span class="sxs-lookup"><span data-stu-id="47fab-125">You can use the **View codes for keyboard shortcuts** menu on the mobile device to find the numeric character codes.</span></span> <span data-ttu-id="47fab-126">请注意，根据所使用的硬件，映射可能不同。</span><span class="sxs-lookup"><span data-stu-id="47fab-126">Note that the mappings might differ, depending on the hardware that is used.</span></span> <span data-ttu-id="47fab-127">必须使用以下句法创建映射：</span><span class="sxs-lookup"><span data-stu-id="47fab-127">You must use the following syntax to create the mapping:</span></span>

<span data-ttu-id="47fab-128">&lt;控件名称&gt;（&lt;键名称&gt;）=&lt;键字码&gt;；</span><span class="sxs-lookup"><span data-stu-id="47fab-128">&lt;control name&gt;(&lt;key name&gt;)=&lt;key code&gt;;</span></span>

<span data-ttu-id="47fab-129">下面是该语法的各个部分的说明：</span><span class="sxs-lookup"><span data-stu-id="47fab-129">Here is an explanation of the parts of the syntax:</span></span>

-   <span data-ttu-id="47fab-130">**&lt;控制名称&gt;** –控件的名称（例如以 HTML 表示的按钮）。</span><span class="sxs-lookup"><span data-stu-id="47fab-130">**&lt;control name&gt;** – The name of the control (for example, a button) that is rendered in HTML.</span></span>
-   <span data-ttu-id="47fab-131">**(&lt;键名称&gt;)** - 为其创建快捷方式的键盘键的名称。</span><span class="sxs-lookup"><span data-stu-id="47fab-131">**(&lt;key name&gt;)** – The name of the keyboard key that you’re creating the shortcut for.</span></span>
-   <span data-ttu-id="47fab-132">**&lt;键代码&gt;** - 要用作快捷键的键的数字字符代码。</span><span class="sxs-lookup"><span data-stu-id="47fab-132">**&lt;Key code&gt;** – The numeric character code for the key to use as the shortcut key.</span></span>

<span data-ttu-id="47fab-133">下面是一个示例：</span><span class="sxs-lookup"><span data-stu-id="47fab-133">Here is an example:</span></span>

<span data-ttu-id="47fab-134">Cancel(Esc)=27; Full(F2)=113</span><span class="sxs-lookup"><span data-stu-id="47fab-134">Cancel(Esc)=27; Full(F2)=113</span></span>

<span data-ttu-id="47fab-135">在包含**取消**按钮的所有页面上，该按钮将具有以下文本：</span><span class="sxs-lookup"><span data-stu-id="47fab-135">On all pages that include a **Cancel** button, the button will have this text:</span></span>

<span data-ttu-id="47fab-136">**(Esc) 取消**</span><span class="sxs-lookup"><span data-stu-id="47fab-136">**(Esc) Cancel**</span></span>

<span data-ttu-id="47fab-137">按键盘上的 ESC 键将启用**取消**按钮。</span><span class="sxs-lookup"><span data-stu-id="47fab-137">Pressing the Esc key on the keyboard will activate the **Cancel** button.</span></span> <span data-ttu-id="47fab-138">要将样式和键盘快捷方式应用于与特定设备，则必须在**条件**字段中创建映射。</span><span class="sxs-lookup"><span data-stu-id="47fab-138">To apply the style and keyboard shortcut settings to a specific device, you must create a mapping in the **Criteria** field.</span></span> <span data-ttu-id="47fab-139">您必须使用 .NET 正则表达式创建映射，并且该表达式必须包含由竖线 (|) 分隔的三个部分，如下所示：</span><span class="sxs-lookup"><span data-stu-id="47fab-139">You must use a .NET regular expression to create the mapping, and the expression must consist of three sections that are separated by a vertical bar (|), as shown here:</span></span>

<span data-ttu-id="47fab-140">Request.UserHostAddress=&lt;用户主机地址&gt;|主机名=&lt;用户主机名&gt;|Request.UserAgent=&lt;用户代理&gt;</span><span class="sxs-lookup"><span data-stu-id="47fab-140">Request.UserHostAddress=&lt;user host address&gt;|HostName=&lt;user host name&gt;|Request.UserAgent=&lt;user agent&gt;</span></span>

<span data-ttu-id="47fab-141">下面是该表达式的各个部分的说明：</span><span class="sxs-lookup"><span data-stu-id="47fab-141">Here is an explanation of the parts of the expression:</span></span>

-   <span data-ttu-id="47fab-142">**&lt;用户主机地址&gt;** - 与申请人 IP 地址匹配的 .NET 正则表达式。</span><span class="sxs-lookup"><span data-stu-id="47fab-142">**&lt;user host address&gt;** – A .NET regular expression that matches the requestor IP address.</span></span>
-   <span data-ttu-id="47fab-143">**&lt;用户主机名&gt;** - 与申请人的网名匹配的 .NET 正则表达式。</span><span class="sxs-lookup"><span data-stu-id="47fab-143">**&lt;user host name&gt;** – A .NET regular expression that matches the network name of the requestor.</span></span>
-   <span data-ttu-id="47fab-144">**&lt;用户代理&gt;** - 与申请人使用的浏览器的标识符匹配的 .NET 正则表达式。</span><span class="sxs-lookup"><span data-stu-id="47fab-144">**&lt;user agent&gt;** – A .NET regular expression that matches the identifier of the browser that the requestor uses.</span></span>

<span data-ttu-id="47fab-145">以下示例允许使用 Internet Explorer 8：</span><span class="sxs-lookup"><span data-stu-id="47fab-145">The following example enables Internet Explorer 8 to be used:</span></span>

<span data-ttu-id="47fab-146">Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0</span><span class="sxs-lookup"><span data-stu-id="47fab-146">Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0</span></span>

<span data-ttu-id="47fab-147">您可使用移动设备上的**查看显示设置的服务器配置**菜单查找有关该设置的信息。</span><span class="sxs-lookup"><span data-stu-id="47fab-147">You can use the **View server configuration for display settings** menu on the mobile device to find the information about the setup.</span></span>

## <a name="define-text-colors-for-messages"></a><span data-ttu-id="47fab-148">定义消息的文本颜色</span><span class="sxs-lookup"><span data-stu-id="47fab-148">Define text colors for messages</span></span>
<span data-ttu-id="47fab-149">您可**移动设备文本颜色**页控制在系统生成的消息（如错误消息）中使用的各种颜色。</span><span class="sxs-lookup"><span data-stu-id="47fab-149">You can use the **Mobile device text colors** page to control the various colors that are used in system-generated messages, such as error messages.</span></span> <span data-ttu-id="47fab-150">例如，文本颜色可以指示消息的用途或严重性。</span><span class="sxs-lookup"><span data-stu-id="47fab-150">For example, the text color can indicate the purpose or severity of the message.</span></span> <span data-ttu-id="47fab-151">将显示以下类型的消息。</span><span class="sxs-lookup"><span data-stu-id="47fab-151">The following types of messages are shown.</span></span>

| <span data-ttu-id="47fab-152">消息类型</span><span class="sxs-lookup"><span data-stu-id="47fab-152">Message type</span></span> | <span data-ttu-id="47fab-153">描述</span><span class="sxs-lookup"><span data-stu-id="47fab-153">Description</span></span>                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47fab-154">默认值</span><span class="sxs-lookup"><span data-stu-id="47fab-154">Default</span></span>      | <span data-ttu-id="47fab-155">默认消息对所有消息使用默认颜色设置（由仓库移动设备门户的 CSS 文件定义）。</span><span class="sxs-lookup"><span data-stu-id="47fab-155">Default messages use the default color settings for all messages, as defined by the CSS file for the Warehouse Mobile Device Portal.</span></span>                                                   |
| <span data-ttu-id="47fab-156">错误</span><span class="sxs-lookup"><span data-stu-id="47fab-156">Error</span></span>        | <span data-ttu-id="47fab-157">错误消息指示用户为继续操作而必须解决的问题。</span><span class="sxs-lookup"><span data-stu-id="47fab-157">Error messages indicate an issue that the user must resolve before he or she can continue.</span></span>                                                                                             |
| <span data-ttu-id="47fab-158">成功</span><span class="sxs-lookup"><span data-stu-id="47fab-158">Success</span></span>      | <span data-ttu-id="47fab-159">成功消息确认操作均已成功。</span><span class="sxs-lookup"><span data-stu-id="47fab-159">Success messages confirm that an action was successful.</span></span>                                                                                                                                |
| <span data-ttu-id="47fab-160">警告</span><span class="sxs-lookup"><span data-stu-id="47fab-160">Warning</span></span>      | <span data-ttu-id="47fab-161">警告消息告知工作人员已出现问题，或指示工作人员继续如此便可能出现问题。</span><span class="sxs-lookup"><span data-stu-id="47fab-161">Warning messages inform the worker that there is an issue, or that there could be an issue if the worker continues.</span></span> <span data-ttu-id="47fab-162">但是，工作人员不必解决问题也能继续。</span><span class="sxs-lookup"><span data-stu-id="47fab-162">However, the worker doesn't have to resolve the issue to continue.</span></span> |

<span data-ttu-id="47fab-163">要选择颜色，请在**选择颜色**页上单击调色板或键入十六进制颜色代码。</span><span class="sxs-lookup"><span data-stu-id="47fab-163">To select the color, on the **Select color** page, click in the palette or type a hexadecimal color code.</span></span>

## <a name="define-the-date-format-to-use-on-mobile-devices"></a><span data-ttu-id="47fab-164">定义移动设备上使用的日期格式</span><span class="sxs-lookup"><span data-stu-id="47fab-164">Define the date format to use on mobile devices</span></span>
<span data-ttu-id="47fab-165">您可以扩展每个安装的可接受日期格式清单。</span><span class="sxs-lookup"><span data-stu-id="47fab-165">You can extend the list of accepted date formats for each installation.</span></span> <span data-ttu-id="47fab-166">例如，如果您希望提供便于工作人员在移动设备上输入日期的格式，此功能可能很有用。</span><span class="sxs-lookup"><span data-stu-id="47fab-166">This capability can be useful if, for example, you want to provide a format that makes it easier for a worker to enter dates on a mobile device.</span></span> <span data-ttu-id="47fab-167">默认格式由用户的默认语言决定，该语言在**用户选项**页上的**语言**字段中指定。</span><span class="sxs-lookup"><span data-stu-id="47fab-167">The default format is determined by the user's default language, which is specified in the **Language** field on the **User options** page.</span></span> <span data-ttu-id="47fab-168">（同一页面还用于将员工与特定仓库工作用户关联。)**注意**：仓库移动设备门户不使用**言和地区首选项**页上的**日期时间和数字格式**字段的设置。</span><span class="sxs-lookup"><span data-stu-id="47fab-168">(The same page is also used to associate an employee with a specific warehouse work user.) **Note:** The Warehouse Mobile Devices Portal doesn't use the setting of the **Date time and number format** field on the **Language and region preferences** page.</span></span> <span data-ttu-id="47fab-169">若要更改日期格式，您必须熟悉 Microsoft .NET Framework 的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="47fab-169">To change a date format, you must be familiar with regular expressions in the Microsoft .NET Framework.</span></span> <span data-ttu-id="47fab-170">有关详细信息，请参阅 [.NET Framework 正则表达式](http://go.microsoft.com/fwlink/?LinkId=391260)。</span><span class="sxs-lookup"><span data-stu-id="47fab-170">For more information, see [.NET Framework Regular Expressions](http://go.microsoft.com/fwlink/?LinkId=391260).</span></span> <span data-ttu-id="47fab-171">要定义日期格式，请编辑位于仓库移动设备门户服务器上的 Content\\Settings\\Dates.ini 目录下的 Dates.ini 文件。</span><span class="sxs-lookup"><span data-stu-id="47fab-171">To define date formats, edit the Dates.ini file that is located at Content\\Settings\\Dates.ini on the Warehouse Mobile Devices Portal server.</span></span> <span data-ttu-id="47fab-172">此文件使用 .NET 正则表达式指定日期格式。</span><span class="sxs-lookup"><span data-stu-id="47fab-172">This file uses .NET regular expressions to specify the date format.</span></span> <span data-ttu-id="47fab-173">正则表达式必须包含用于创建日、月和年 (DDMMYY) 的命名组的子表达式，如下例所示：</span><span class="sxs-lookup"><span data-stu-id="47fab-173">The regular expression must contain subexpressions that create named groups for day, month, and year (DDMMYY), as shown in the following example:</span></span>

<span data-ttu-id="47fab-174">^(?&lt;day&gt;\\d{2})(?&lt;month&gt;\\d{2})(?&lt;year&gt;\\d{2})$</span><span class="sxs-lookup"><span data-stu-id="47fab-174">^(?&lt;day&gt;\\d{2})(?&lt;month&gt;\\d{2})(?&lt;year&gt;\\d{2})$</span></span>

<span data-ttu-id="47fab-175">每个子表达式需要表示日和月的一到二位数，并需要表示年的一到四位数。</span><span class="sxs-lookup"><span data-stu-id="47fab-175">Each subexpression requires one to two digits for the day and month, and one to four digits for the year.</span></span> <span data-ttu-id="47fab-176">例如，以下子表达式定义了年的命名组，需要最少两位数或最多四位数：</span><span class="sxs-lookup"><span data-stu-id="47fab-176">For example, the following subexpression defines a named group for a year, and requires a minimum of two digits or a maximum of four digits:</span></span>

<span data-ttu-id="47fab-177">(?&lt;year&gt;\\d{2,4})</span><span class="sxs-lookup"><span data-stu-id="47fab-177">(?&lt;year&gt;\\d{2,4})</span></span>

<span data-ttu-id="47fab-178">您可在同一个文件中指定多个表达式。</span><span class="sxs-lookup"><span data-stu-id="47fab-178">You can specify more than one expression in the same file.</span></span> <span data-ttu-id="47fab-179">每个表达式必须位于单独的行上。</span><span class="sxs-lookup"><span data-stu-id="47fab-179">Each expression must be on a separate line.</span></span> <span data-ttu-id="47fab-180">匹配的第一个表达式用于分析日期。</span><span class="sxs-lookup"><span data-stu-id="47fab-180">The first expression that is matched is used to parse the date.</span></span>

<a name="additional-resources"></a><span data-ttu-id="47fab-181">其他资源</span><span class="sxs-lookup"><span data-stu-id="47fab-181">Additional resources</span></span>
--------

[<span data-ttu-id="47fab-182">为仓库工作配置移动设备</span><span class="sxs-lookup"><span data-stu-id="47fab-182">Configuration of mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)



