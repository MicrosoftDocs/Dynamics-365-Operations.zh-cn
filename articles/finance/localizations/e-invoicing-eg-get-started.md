---
title: 开始使用适用于埃及的电子开票
description: 本主题提供的信息将帮助您开始使用 Finance 和 Supply Chain Management 中适用于埃及的电子开票。
author: gionoder
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: abae35db7e37e65950c05c8e21b8e8555edbf3be
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920773"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a><span data-ttu-id="0826b-103">开始使用适用于埃及的电子开票</span><span class="sxs-lookup"><span data-stu-id="0826b-103">Get started with Electronic invoicing for Egypt</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0826b-104">本主题提供的信息将帮助您开始使用适用于埃及的电子开票。</span><span class="sxs-lookup"><span data-stu-id="0826b-104">This topic provides information that will help you get started with Electronic invoicing for Egypt.</span></span> <span data-ttu-id="0826b-105">本主题将指导您完成 Regulatory Configuration Services (RCS) 中与国家/地区有关的配置步骤，并补充[开始使用电子开票](e-invoicing-get-started.md)中描述的步骤。</span><span class="sxs-lookup"><span data-stu-id="0826b-105">The topic guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS), and complement the steps described in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a><span data-ttu-id="0826b-106">埃及电子发票 (EG) 电子开票功能的国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="0826b-106">Country-specific configuration for Egyptian electronic invoice (EG) Electronic invoicing feature</span></span>

<span data-ttu-id="0826b-107">**埃及电子发票 (EG) 电子开票功能** 的一些参数使用默认值发布。</span><span class="sxs-lookup"><span data-stu-id="0826b-107">Some of the parameters from the **Egyptian electronic invoice (EG) Electronic invoicing feature** are published with default values.</span></span> <span data-ttu-id="0826b-108">在将电子开票功能部署到服务环境之前，查看并（如有必要）更新这些值以更好地反映您的业务操作。</span><span class="sxs-lookup"><span data-stu-id="0826b-108">Review the values and if necessary, update the values to better reflect your business operation before you deploy the Electronic invoicing feature to the Service environment.</span></span>

<span data-ttu-id="0826b-109">此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **电子开票功能的国家/地区特定配置** 部分。</span><span class="sxs-lookup"><span data-stu-id="0826b-109">This section complements the **Country-specific configuration for Electronic invoicing feature** section in the topic [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0826b-110">先决条件</span><span class="sxs-lookup"><span data-stu-id="0826b-110">Prerequisites</span></span>

<span data-ttu-id="0826b-111">在完成本节中的过程之前，您必须：</span><span class="sxs-lookup"><span data-stu-id="0826b-111">Before you complete the procedure in this section, you must:</span></span>

- <span data-ttu-id="0826b-112">创建数字证书机密，如 [开始使用电子开票服务管理](e-invoicing-get-started-service-administration.md)内 **创建数字证书机密** 部分中所述。</span><span class="sxs-lookup"><span data-stu-id="0826b-112">Create a digital certificate secret, as described in the **Create digital certificate secret** section in [Get started with Electronic invoicing service administration](e-invoicing-get-started-service-administration.md).</span></span> <span data-ttu-id="0826b-113">出于测试目的，埃及税务机关提供了特定的测试数字证书，这些证书只能在测试和解决方案验证阶段才可以使用。</span><span class="sxs-lookup"><span data-stu-id="0826b-113">For testing purposes, the Egyptian tax authority provides specific test digital certificates that must be used only during testing and solution validation phases.</span></span> <span data-ttu-id="0826b-114">有关详细信息，请使用[埃及电子开票 SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/) 中提供的链接访问埃及税务局网站。</span><span class="sxs-lookup"><span data-stu-id="0826b-114">For more information, consult the Egyptian tax authority website using the link provided in the [Egyptian e-invoicing SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).</span></span>

1. <span data-ttu-id="0826b-115">在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="0826b-115">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing** tile.</span></span>
2. <span data-ttu-id="0826b-116">在 **电子开票功能** 页面上，验证是否选择了您创建的 **埃及电子发票 (EG)** 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="0826b-116">On the **Electronic invoicing Features** page, verify that the **Egyptian electronic invoice (EG)** Electronic invoicing feature you created is selected.</span></span>
3. <span data-ttu-id="0826b-117">在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。</span><span class="sxs-lookup"><span data-stu-id="0826b-117">On the **Versions** tab, verify the **Draft** version is selected.</span></span>
4. <span data-ttu-id="0826b-118">在 **设置** 选项卡上的网格中，选择 **销售发票** 功能设置。</span><span class="sxs-lookup"><span data-stu-id="0826b-118">On the **Setups** tab, in the grid, select **Sales invoice** feature setup.</span></span>
5. <span data-ttu-id="0826b-119">选择 **编辑**，在 **操作** 选项卡上的 **操作** 字段组中，选择 **对埃及税务主管机构的 json 文档签名**。</span><span class="sxs-lookup"><span data-stu-id="0826b-119">Select **Edit**, and on the **Actions** tab in the **Actions** field group, select **Sign json document for Egyptian Tax Authority**.</span></span>
6. <span data-ttu-id="0826b-120">在 **参数** 字段组中，选择 **证书名称** 参数，并选择所创建的要与电子开票功能配合使用的数字证书名称。</span><span class="sxs-lookup"><span data-stu-id="0826b-120">In the **Parameters** field group, select the parameter, **Certificate name** and select the name of the digital certificate created to use with the Electronic invoicing feature.</span></span>
7. <span data-ttu-id="0826b-121">在 **操作** 字段组中，选择 **与埃及 ETA 服务集成**。</span><span class="sxs-lookup"><span data-stu-id="0826b-121">In the **Actions** field group, select **Integrate with Egyptian ETA service**.</span></span> <span data-ttu-id="0826b-122">对于两次发生的此操作，请重复此步骤。</span><span class="sxs-lookup"><span data-stu-id="0826b-122">Repeat this step for the two occurrences of this action.</span></span>
8. <span data-ttu-id="0826b-123">在 **参数** 字段组中，选择 **Web 服务 URL** 和 **登录服务 URL**，并在必要时查看 URL 参数。</span><span class="sxs-lookup"><span data-stu-id="0826b-123">In the **Parameters** field group, select **Web service URL** and **Login service URL** and, if necessary, review the URL parameters.</span></span> <span data-ttu-id="0826b-124">使用[埃及电子开票 SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/) 中提供的链接，访问埃及税务局网站以获取测试和生产 URL。</span><span class="sxs-lookup"><span data-stu-id="0826b-124">Consult the Egyptian tax authority website to get the Testing and Production URL, using the link provided in the [Egyptian e-invoicing SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).</span></span>
9. <span data-ttu-id="0826b-125">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="0826b-125">Select **Save** and close the page.</span></span>
10. <span data-ttu-id="0826b-126">若要将电子开票功能部署到服务环境，请参阅[开始使用电子开票](e-invoicing-get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="0826b-126">To deploy the Electronic invoicing feature to the Service environment, see [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a><span data-ttu-id="0826b-127">埃及电子发票 (EG) 电子开票功能的应用程序设置的国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="0826b-127">Country-specific configuration of the application setup for the Egyptian electronic invoice (EG) Electronic invoicing feature</span></span>

<span data-ttu-id="0826b-128">在将应用程序设置部署到 Finance 或 Supply Chain Management 连接的应用程序之前，请完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="0826b-128">Complete these steps before you deploy the Application setup to your Finance or Supply Chain Management Connected application.</span></span>

<span data-ttu-id="0826b-129">此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **应用程序设置的国家/地区特定配置** 部分。</span><span class="sxs-lookup"><span data-stu-id="0826b-129">This section complements the **Country-specific configuration of application setup** section in the topic [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="0826b-130">在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="0826b-130">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing** tile.</span></span>
2. <span data-ttu-id="0826b-131">在 **电子开票功能** 页面中，验证是否选择了 **埃及电子发票 (EG)** 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="0826b-131">In the **Electronic invoicing Features** page, verify that the **Egyptian electronic invoice (EG)** Electronic invoicing feature is selected.</span></span>
3. <span data-ttu-id="0826b-132">在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。</span><span class="sxs-lookup"><span data-stu-id="0826b-132">On the **Versions** tab, verify that the **Draft** version is selected.</span></span>
4. <span data-ttu-id="0826b-133">在 **设置** 选项卡上，选择 **应用程序设置**，并在 **相连应用程序** 字段中，选择要部署到的应用程序。</span><span class="sxs-lookup"><span data-stu-id="0826b-133">On the **Setups** tab, select **Application setup** and in the **Connected application** field, select the application where you want to deploy.</span></span>
5. <span data-ttu-id="0826b-134">在 **表名称** 字段中，验证是否选择了客户发票日记帐。</span><span class="sxs-lookup"><span data-stu-id="0826b-134">In the **Table name** field, verify that the customer invoice journal is selected.</span></span>
6. <span data-ttu-id="0826b-135">选择 **响应类型**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0826b-135">Select **Response types**, and then select **New**.</span></span>
7. <span data-ttu-id="0826b-136">在 **响应类型** 字段中，输入“响应”，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="0826b-136">In the **Response type** field, enter "Response" and in the **Description** field, enter "Description".</span></span>
8. <span data-ttu-id="0826b-137">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="0826b-137">In the **Submission status** field, select **Pending**.</span></span>
9. <span data-ttu-id="0826b-138">在 **模型映射** 字段中，选择具有 **（预览）响应消息导入格式** 的 **来自响应消息的模型映射**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0826b-138">In the **Model mapping** field, select **Model mapping from response message**, with **(Preview) Response message import format**, and then select **Save**.</span></span>
10. <span data-ttu-id="0826b-139">选择 **新建**，然后在 **响应类型** 字段中输入“ResponseData”作为固定值。</span><span class="sxs-lookup"><span data-stu-id="0826b-139">Select **New** and in the **Response type** field, enter "ResponseData" as a fixed value.</span></span> <span data-ttu-id="0826b-140">在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="0826b-140">In the **Description** field, enter "Description".</span></span>
11. <span data-ttu-id="0826b-141">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="0826b-141">In the **Submission status** field, select **Pending**.</span></span>
12. <span data-ttu-id="0826b-142">在 **数据实体名称** 字段中，选择 **销售发票抬头 V2**。</span><span class="sxs-lookup"><span data-stu-id="0826b-142">In the **Data entity name** field, select **Sales invoice headers V2**.</span></span>
13. <span data-ttu-id="0826b-143">在 **模型映射** 字段中，选择具有 **（预览）埃及响应数据导入格式** 的 **埃及响应数据导入**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="0826b-143">In the **Model mapping** field, select **Egypt response data import**, with **(Preview) Egypt response data import** and then select **Save**.</span></span>
14. <span data-ttu-id="0826b-144">若要将应用程序设置部署到 Finance 或 Supply Chain Management 连接的应用程序，请参阅[开始使用电子开票](e-invoicing-get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="0826b-144">To deploy the application setup to the Finance or Supply Chain Management connected application, see [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="0826b-145">隐私声明</span><span class="sxs-lookup"><span data-stu-id="0826b-145">Privacy notice</span></span>

<span data-ttu-id="0826b-146">启用 **埃及电子发票 (EG)** 功能可能需要发送有限的数据，包括组织税务登记 ID。</span><span class="sxs-lookup"><span data-stu-id="0826b-146">Enabling the **Egyptian electronic invoice (EG)** feature may require sending limited data, including the organization tax registration ID.</span></span> <span data-ttu-id="0826b-147">此数据将被传输到税务机构授权的第三方机构，以便以与政府的 Web 服务集成所需的预定义格式向该税务机构发送电子发票。</span><span class="sxs-lookup"><span data-stu-id="0826b-147">This data will be transmitted to third-party agencies authorized by the tax authority for the purpose of sending electronic invoices to this tax authority in the predefined format that's required for integration with the government's web service.</span></span> <span data-ttu-id="0826b-148">管理员可以通过导航到 **组织管理** > **设置** > **电子单据参数** 来启用和禁用此功能。</span><span class="sxs-lookup"><span data-stu-id="0826b-148">An administrator can enable and disable the feature by navigating to **Organization administration** > **Setup** > **Electronic document parameters**.</span></span> <span data-ttu-id="0826b-149">在 **功能** 选项卡上，选择包含 **埃及电子发票 (EG)** 功能的行，然后进行适当的选择。</span><span class="sxs-lookup"><span data-stu-id="0826b-149">On the **Features** tab, select the row that contains the **Egyptian electronic invoice (EG)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="0826b-150">从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。</span><span class="sxs-lookup"><span data-stu-id="0826b-150">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="0826b-151">有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。</span><span class="sxs-lookup"><span data-stu-id="0826b-151">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0826b-152">其他资源</span><span class="sxs-lookup"><span data-stu-id="0826b-152">Additional resources</span></span>

- [<span data-ttu-id="0826b-153">电子开票概览</span><span class="sxs-lookup"><span data-stu-id="0826b-153">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="0826b-154">开始使用电子开票服务管理</span><span class="sxs-lookup"><span data-stu-id="0826b-154">Get started with Electronic invoicing service administration</span></span>](e-invoicing-get-started-service-administration.md)
- [<span data-ttu-id="0826b-155">开始使用电子开票</span><span class="sxs-lookup"><span data-stu-id="0826b-155">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="0826b-156">埃及的客户电子发票</span><span class="sxs-lookup"><span data-stu-id="0826b-156">Customer electronic invoices in Egypt</span></span>](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
