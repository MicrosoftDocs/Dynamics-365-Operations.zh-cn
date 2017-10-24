---
title: "收据模板和打印"
description: "本文介绍如何修改窗体布局以控制如何打印收据、发票和其他单据。 Microsoft Dynamics 365 for Retail 包括您可以用于轻松创建和修改不同类型的窗体布局的窗体布局设计器。"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c95215af7004606bb3e000f68c56ea5c69bb9582
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="receipt-templates-and-printing"></a><span data-ttu-id="d39c0-104">收据模板和打印</span><span class="sxs-lookup"><span data-stu-id="d39c0-104">Receipt templates and printing</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="d39c0-105">本文介绍如何修改窗体布局以控制如何打印收据、发票和其他单据。</span><span class="sxs-lookup"><span data-stu-id="d39c0-105">This article describes how to modify form layouts to control how receipts, invoices, and other documents are printed.</span></span> <span data-ttu-id="d39c0-106">Microsoft Dynamics 365 for Retail 包括您可以用于轻松创建和修改不同类型的窗体布局的窗体布局设计器。</span><span class="sxs-lookup"><span data-stu-id="d39c0-106">Microsoft Dynamics 365 for Retail includes a form layout designer that you can use to easily create and modify various kinds of form layouts.</span></span>

<span data-ttu-id="d39c0-107">**重要信息** 必须从 Retail Modern POS 和 Cloud POS 设置窗体布局和收据模板以打印收据和其他文档。</span><span class="sxs-lookup"><span data-stu-id="d39c0-107">**Important:** You must set up form layouts and receipt profiles to print receipts and other documents from Retail Modern POS and Cloud POS.</span></span> <span data-ttu-id="d39c0-108">一个收据模板中可以包含多个窗体布局。</span><span class="sxs-lookup"><span data-stu-id="d39c0-108">You can include multiple form layouts in a receipt profile.</span></span> <span data-ttu-id="d39c0-109">然后可以通过修改硬件配置文件将收据模板分配到打印机。</span><span class="sxs-lookup"><span data-stu-id="d39c0-109">You can then assign the receipt profile to a printer by modifying a hardware profile.</span></span>

## <a name="set-up-a-receipt-format"></a><span data-ttu-id="d39c0-110">设置收据形式</span><span class="sxs-lookup"><span data-stu-id="d39c0-110">Set up a receipt format</span></span>
1.  <span data-ttu-id="d39c0-111">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS** &gt; **收据格式**。</span><span class="sxs-lookup"><span data-stu-id="d39c0-111">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Receipt formats**.</span></span>
2.  <span data-ttu-id="d39c0-112">在**收据格式**页，单击**新建**创建新窗体布局或选择现有的窗体布局。</span><span class="sxs-lookup"><span data-stu-id="d39c0-112">On the **Receipt format** page, click **New** to create a new form layout, or select an existing form layout.</span></span>
3.  <span data-ttu-id="d39c0-113">在**收据格式**字段中，输入窗体布局的标识符，然后选择此布局使用收据的类型。</span><span class="sxs-lookup"><span data-stu-id="d39c0-113">In the **Receipt format** field, enter an identifier for the form layout, and then select the type of receipt that this layout is used for.</span></span> <span data-ttu-id="d39c0-114">您还可以在**标题**字段中为收据输入描述和简短名称。</span><span class="sxs-lookup"><span data-stu-id="d39c0-114">You can also enter a description and a short name for the receipt in the **Title** field.</span></span>
4.  <span data-ttu-id="d39c0-115">在**常规**快速选项卡上，选择一个选项以定义打印行为：</span><span class="sxs-lookup"><span data-stu-id="d39c0-115">On the **General** FastTab, select an option to define the print behavior:</span></span>
    -   <span data-ttu-id="d39c0-116">**始终打印** – 收据根据需要自动打印。</span><span class="sxs-lookup"><span data-stu-id="d39c0-116">**Always print** – The receipt is printed automatically, as appropriate.</span></span>
    -   <span data-ttu-id="d39c0-117">**不打印** – 收据不打印。</span><span class="sxs-lookup"><span data-stu-id="d39c0-117">**Do not print** – The receipt isn't printed.</span></span>
    -   <span data-ttu-id="d39c0-118">**提示用户** – 提示用户打印收据。</span><span class="sxs-lookup"><span data-stu-id="d39c0-118">**Prompt user** – The user is prompted to print the receipt.</span></span>
    -   <span data-ttu-id="d39c0-119">**根据需要** – 此选项只用于礼品收据。</span><span class="sxs-lookup"><span data-stu-id="d39c0-119">**As required** – This option is used only for gift receipts.</span></span> <span data-ttu-id="d39c0-120">选中此选项后，用户可以从**更改**页打印礼品收据，如果需要礼品收据。</span><span class="sxs-lookup"><span data-stu-id="d39c0-120">When this option is selected, the user can print a gift receipt from the **Change** page, if a gift receipt is required.</span></span>

## <a name="design-a-receipt-format"></a><span data-ttu-id="d39c0-121">设计收据格式</span><span class="sxs-lookup"><span data-stu-id="d39c0-121">Design a receipt format</span></span>
<span data-ttu-id="d39c0-122">使用窗体布局设计器以图形形式创建窗体文档的布局。</span><span class="sxs-lookup"><span data-stu-id="d39c0-122">Use the form layout designer to graphically create the layout of the form document.</span></span> <span data-ttu-id="d39c0-123">**收据格式设计器**页具有三个部分：**页眉**、**行**和**页脚**。</span><span class="sxs-lookup"><span data-stu-id="d39c0-123">The **Receipt format designer** page has three sections: **Header**, **Lines**, and **Footer**.</span></span> <span data-ttu-id="d39c0-124">窗体布局从所有三个部分使用元素，而其他类型仅从一个或两个部分使用元素。</span><span class="sxs-lookup"><span data-stu-id="d39c0-124">Some types of form layouts use elements from all three sections, whereas other types use elements from only one or two sections.</span></span> <span data-ttu-id="d39c0-125">若要为每个部分查看可用的元素，请在页面左侧单击导航窗格中的相应按钮。</span><span class="sxs-lookup"><span data-stu-id="d39c0-125">To view the elements that are available for each section, click the appropriate button in the navigation pane on the left side of the page.</span></span>

1.  <span data-ttu-id="d39c0-126">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS** &gt; **收据格式**。</span><span class="sxs-lookup"><span data-stu-id="d39c0-126">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Receipt formats**.</span></span>
2.  <span data-ttu-id="d39c0-127">在**收据格式**页上，选择一个窗体布局，然后单击**设计器**。</span><span class="sxs-lookup"><span data-stu-id="d39c0-127">On the **Receipt format** page, select a form layout, and then click **Designer**.</span></span>
3.  <span data-ttu-id="d39c0-128">单击**运行**开始安装 Retail 设计器主机。</span><span class="sxs-lookup"><span data-stu-id="d39c0-128">Click **Run** to start to install the Retail designer host.</span></span>
4.  <span data-ttu-id="d39c0-129">在出现在 Internet Explorer 窗口底部的通知栏上，单击**打开**开始安装一键式设计器。</span><span class="sxs-lookup"><span data-stu-id="d39c0-129">On the Notification bar that appears at the bottom of the Internet Explorer window, click **Open** to start to install the one-click designer.</span></span> <span data-ttu-id="d39c0-130">（通知栏可能在其他浏览器的不同位置显示。）进度指示器显示安装过程的进度。</span><span class="sxs-lookup"><span data-stu-id="d39c0-130">(The Notification bar might appear in a different location in other browsers.) The progress indicator shows the progress of the installation process.</span></span>
5.  <span data-ttu-id="d39c0-131">在安装完成后，输入您的 Dynamics 365 for Retail 用户名和密码，然后单击**登录**启动设计器。</span><span class="sxs-lookup"><span data-stu-id="d39c0-131">After the installation is completed, enter your Dynamics 365 for Retail user name and password, and then click **Sign in** to start the designer.</span></span>
6.  <span data-ttu-id="d39c0-132">在您的凭据验证和设计器启动后，可以开始设计收据格式或修改现有的格式。</span><span class="sxs-lookup"><span data-stu-id="d39c0-132">After your credentials are validated and the designer starts, you can start to design the receipt format or modify an existing format.</span></span>
7.  <span data-ttu-id="d39c0-133">若要创建窗体的元素，选择**页眉**、**行**或**页脚**部分，然后将元素从该部分拖到工作区。</span><span class="sxs-lookup"><span data-stu-id="d39c0-133">To create the elements of the form, select the **Header**, **Lines**, or **Footer** section, and then drag an element from that section to the workspace.</span></span> <span data-ttu-id="d39c0-134">大多数元素包含变量，其从数据库自动填充数据。</span><span class="sxs-lookup"><span data-stu-id="d39c0-134">Most elements contain variables that are automatically populated with data from the database.</span></span> <span data-ttu-id="d39c0-135">其他元素，例如“**文本**”，可以在收据上打印自定义文本。</span><span class="sxs-lookup"><span data-stu-id="d39c0-135">Other elements, such as **Text**, let you print custom text on the receipt.</span></span> <span data-ttu-id="d39c0-136">**注意：**通过调整该部分的右下角中的数字，可以指定每个部分跨多少行。</span><span class="sxs-lookup"><span data-stu-id="d39c0-136">**Note:** You can specify how many lines each section spans by adjusting the number in the lower-right corner of that section.</span></span> <span data-ttu-id="d39c0-137">要想使一个部分更便于修改，请通过拖动该部分底部的大小调整栏来增加该部分的高度。</span><span class="sxs-lookup"><span data-stu-id="d39c0-137">To make it easier to modify a section, increase its height by dragging the sizing bar at the bottom of the section.</span></span> <span data-ttu-id="d39c0-138">在工作区的部分的高度不会影响实际收据上的行数。</span><span class="sxs-lookup"><span data-stu-id="d39c0-138">The height of the section on the workspace doesn't affect the number of lines on the actual receipt.</span></span>
8.  <span data-ttu-id="d39c0-139">在您将元素拖到工作区后，在页面的底部的**对象信息**窗格中修改部分属性。</span><span class="sxs-lookup"><span data-stu-id="d39c0-139">After you drag an element to the workspace, set the properties for the part in the **Object information** pane at the bottom of the page.</span></span> <span data-ttu-id="d39c0-140">输入以下一项或多项设置：</span><span class="sxs-lookup"><span data-stu-id="d39c0-140">Enter one or more of the following settings:</span></span>
    -   <span data-ttu-id="d39c0-141">“**对齐**”– 将字段的对齐方式设置为“**左**”或“**右**”。</span><span class="sxs-lookup"><span data-stu-id="d39c0-141">**Align** – Set the alignment of the field to either **Left** or **Right**.</span></span>
    -   <span data-ttu-id="d39c0-142">**填充字符** – 指定空格字符。</span><span class="sxs-lookup"><span data-stu-id="d39c0-142">**Fill char** – Specify the white space character.</span></span> <span data-ttu-id="d39c0-143">默认情况下，使用空白间距，不过，您可以输入任意字符。</span><span class="sxs-lookup"><span data-stu-id="d39c0-143">By default, an empty space is used, but you can enter any character.</span></span>
    -   <span data-ttu-id="d39c0-144">**前缀** – 输入要显示在所选字段开头的值。</span><span class="sxs-lookup"><span data-stu-id="d39c0-144">**Prefix** – Enter the value that appears at the beginning of the field.</span></span> <span data-ttu-id="d39c0-145">此设置仅适用于布局的**行**部分。</span><span class="sxs-lookup"><span data-stu-id="d39c0-145">This setting applies only to the **Lines** section of the layout.</span></span>
    -   <span data-ttu-id="d39c0-146">**字符** – 指定如果元素包含变量，字段可包含的最大字符数。</span><span class="sxs-lookup"><span data-stu-id="d39c0-146">**Characters** – Specify the maximum number of characters that the field can contain if the element contains a variable.</span></span> <span data-ttu-id="d39c0-147">如果该字段中的文本长于您指定最长的编号，该文本被截断以适合该字段。</span><span class="sxs-lookup"><span data-stu-id="d39c0-147">If the text in the field is longer than the number of character that you specify, the text is truncated to fit the field.</span></span>
    -   <span data-ttu-id="d39c0-148">**变量** – 如果该元素包含变量且无法自定义，则会自动选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="d39c0-148">**Variable** – This check box is selected automatically if the element contains a variable and can't be customized.</span></span>
    -   <span data-ttu-id="d39c0-149">**字体类型** – 设置字体为**常规**或**粗体**。</span><span class="sxs-lookup"><span data-stu-id="d39c0-149">**Font type** – Set the font style to either **Regular** or **Bold**.</span></span> <span data-ttu-id="d39c0-150">粗体字母使用的空间是常规字母的两倍。</span><span class="sxs-lookup"><span data-stu-id="d39c0-150">Bold letters use two times as much space as regular letters.</span></span> <span data-ttu-id="d39c0-151">因此，一些字符可能被截断。</span><span class="sxs-lookup"><span data-stu-id="d39c0-151">Therefore, some characters might be truncated.</span></span>
    -   <span data-ttu-id="d39c0-152">**字体大小** – 将字体大小设置为**常规**或**大号**。</span><span class="sxs-lookup"><span data-stu-id="d39c0-152">**Font size** – Set the font size to either **Regular** or **Large**.</span></span> <span data-ttu-id="d39c0-153">大号字母是常规字母的两倍。</span><span class="sxs-lookup"><span data-stu-id="d39c0-153">Large letters are two times higher than regular letters.</span></span> <span data-ttu-id="d39c0-154">因此，使用大号字母可能导致在收据中产生重叠文本。</span><span class="sxs-lookup"><span data-stu-id="d39c0-154">Therefore, using large letters may lead to overlapping text in the receipt.</span></span>
    -   <span data-ttu-id="d39c0-155">**删除** – 单击此按钮可从窗体布局中删除所选的组成部分。</span><span class="sxs-lookup"><span data-stu-id="d39c0-155">**Delete** – Click this button to remove the selected part from the form layout.</span></span>

## <a name="assign-receipt-profiles"></a><span data-ttu-id="d39c0-156">分配收据模板</span><span class="sxs-lookup"><span data-stu-id="d39c0-156">Assign receipt profiles</span></span>
<span data-ttu-id="d39c0-157">收据模板通过硬件配置文件直接分配到打印机。</span><span class="sxs-lookup"><span data-stu-id="d39c0-157">Receipt profiles are assigned directly to printers through the hardware profile.</span></span>

1.  <span data-ttu-id="d39c0-158">通过单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **硬件配置文件**打开硬件配置文件。</span><span class="sxs-lookup"><span data-stu-id="d39c0-158">Open the hardware profile by clicking **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profile**.</span></span>
2.  <span data-ttu-id="d39c0-159">选择打印机，然后在**收据模板**字段中，分配要在登记簿中使用的收据模板。</span><span class="sxs-lookup"><span data-stu-id="d39c0-159">Select the printer, and then, in the **Receipt profile** field, assign the receipt profile to use on the register.</span></span>

<span data-ttu-id="d39c0-160">**注意：**如果使用两台打印机，一台打印机可用于打印标准的 40 列热敏收据。</span><span class="sxs-lookup"><span data-stu-id="d39c0-160">**Note:** If two printers are used, one printer can be used to print standard 40-column thermal receipts.</span></span> <span data-ttu-id="d39c0-161">第二台打印机通常用于打印需要更多信息的全页收据类型。</span><span class="sxs-lookup"><span data-stu-id="d39c0-161">The second printer is typically used to print full-page receipt types that require more information.</span></span> <span data-ttu-id="d39c0-162">这些收据类型包括客户订单收据和客户发票。</span><span class="sxs-lookup"><span data-stu-id="d39c0-162">These receipt types include customer order receipts and customer invoices.</span></span>



