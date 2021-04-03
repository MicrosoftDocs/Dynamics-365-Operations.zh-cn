---
title: 开始使用适用于巴西的电子开票附加产品
description: 本主题提供的信息将帮助您开始使用 Finance 和 Supply Chain Management 中适用于巴西的电子开票附加产品。
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: eaf9433ad2d9ccf3d3c5632d0f2d4fe772ff8bde
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592662"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="9f668-103">开始使用适用于巴西的电子开票附加产品</span><span class="sxs-lookup"><span data-stu-id="9f668-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f668-104">本主题说明如何开始使用适用于巴西的电子开票附加产品。</span><span class="sxs-lookup"><span data-stu-id="9f668-104">This topic explains how to get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="9f668-105">本主题中的过程将指导您完成 Regulatory Configuration Services (RCS) 中与国家/地区有关的配置步骤，并补充本[开始使用电子发票附加产品](e-invoicing-get-started.md)主题中描述的步骤。</span><span class="sxs-lookup"><span data-stu-id="9f668-105">The procedures in this topic guide you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS), and complement the steps described in the topic, [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a><span data-ttu-id="9f668-106">巴西 NF-e (BR) 电子开票功能的国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="9f668-106">Country-specific configuration for Brazilian NF-e (BR) Electronic invoicing feature</span></span>

<span data-ttu-id="9f668-107">配置巴西 NF-e (BR) 电子开票功能需要完成特定步骤。</span><span class="sxs-lookup"><span data-stu-id="9f668-107">Configuring the Brazilian NF-e (BR) Electronic invoicing feature requires that specific steps be completed.</span></span> <span data-ttu-id="9f668-108">所发布的配置中的某些参数采用了默认值，因此必须对其进行检查和更新以更好地适合您的业务操作。</span><span class="sxs-lookup"><span data-stu-id="9f668-108">Some of the parameters from the configurations are published with default values, so they must be reviewed and updated to better fit your business operation.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9f668-109">先决条件</span><span class="sxs-lookup"><span data-stu-id="9f668-109">Prerequisites</span></span>

<span data-ttu-id="9f668-110">在完成本节中的步骤之前，请为您的组织创建巴西 NF-e (BR) 电子开票功能，如 [开始使用电子开票附加产品](e-invoicing-get-started.md)主题内的 **在您的组织提供者下创建电子开票功能** 部分中所述。</span><span class="sxs-lookup"><span data-stu-id="9f668-110">Before you complete the procedure in this section, create a Brazilian NF-e (BR) Electronic invoicing feature for your organization, as described in the **Create an Electronic invoicing feature under your organization provider** section of the topic, [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="9f668-111">在 RCS 内 **全球化功能** 工作区的 **功能** 部分，选择 **电子开票附加产品** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="9f668-111">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing add-on** tile.</span></span>
2. <span data-ttu-id="9f668-112">在 **电子开票附加产品功能** 页上，验证是否选择了您创建的 **巴西 NF-e (BR)** 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="9f668-112">On the **Electronic invoicing add-on Features** page, verify that the **Brazilian NF-e (BR)** Electronic invoicing feature you created is selected.</span></span>
3. <span data-ttu-id="9f668-113">在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。</span><span class="sxs-lookup"><span data-stu-id="9f668-113">On the **Versions** tab, verify that the **Draft** version is selected.</span></span>
4. <span data-ttu-id="9f668-114">在 **设置** 选项卡上的网格中，选择 **提交**，然后选择 **编辑。**</span><span class="sxs-lookup"><span data-stu-id="9f668-114">On the **Setups** tab, in the grid, select **Submit** and then select **Edit.**</span></span>
5. <span data-ttu-id="9f668-115">在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）签署 xml 文档** 操作。</span><span class="sxs-lookup"><span data-stu-id="9f668-115">On the **Actions** tab, in the **Actions** field group, select **(Preview) Sign xml document** action.</span></span>
6. <span data-ttu-id="9f668-116">在 **参数** 字段组中，选择 **证书名称**，并在 **值** 字段中，输入与您的密钥保管库参数关联的证书名称。</span><span class="sxs-lookup"><span data-stu-id="9f668-116">In the **Parameters** field group, select **Certificate name**, and in the **Value** field, enter the name of certificate associated to your Key vault parameter.</span></span>
7. <span data-ttu-id="9f668-117">在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）调用巴西 SEFAZ 服务** 操作。</span><span class="sxs-lookup"><span data-stu-id="9f668-117">On the **Actions** tab, in the **Actions** field group, select **(Preview) Call Brazilian SEFAZ service** action.</span></span>
8. <span data-ttu-id="9f668-118">在 **参数** 字段组中，选择 **URL 地址** 参数。</span><span class="sxs-lookup"><span data-stu-id="9f668-118">In the **Parameters** field group, select **URL address** parameter.</span></span>
9. <span data-ttu-id="9f668-119">在 **值** 字段中，如有必要，请查看并更新您所在州的 SEFAZ 文档所发布的 Web 服务的 URL，然后选择 **保存。**</span><span class="sxs-lookup"><span data-stu-id="9f668-119">In the **Value** field, if necessary, review and update the URL of the web services published by the SEFAZ documentation for your state and then select **Save.**</span></span>
10. <span data-ttu-id="9f668-120">在 **适用性规则** 选项卡上的 **适用性规则设置** 字段组中，查看 **洲** 字段，并根据需要针对与 Web 服务 URL 所引用的相同洲对其进行更新。</span><span class="sxs-lookup"><span data-stu-id="9f668-120">On the **Applicability rules** tab, in the **Setup of applicability rule** field group, review and update the **State** field criteria as necessary for the same state which the URL of the web services is referred to.</span></span>
11. <span data-ttu-id="9f668-121">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="9f668-121">Select **Save** and close the page.</span></span>
12. <span data-ttu-id="9f668-122">要配置应用程序设置，请参阅[开始使用电子开票附加产品](e-invoicing-get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="9f668-122">To configure the application setup, see [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a><span data-ttu-id="9f668-123">巴西 NF-e (BR) 电子开票功能的应用程序设置的国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="9f668-123">Country-specific configuration of application setup for Brazilian NF-e (BR) Electronic invoicing feature</span></span>

<span data-ttu-id="9f668-124">配置巴西 NF-e (BR) 电子开票功能的应用程序设置需要完成特定步骤。</span><span class="sxs-lookup"><span data-stu-id="9f668-124">Configuring the Application setup for Brazilian NF-e (BR) Electronic invoicing feature requires that specific steps be completed.</span></span> <span data-ttu-id="9f668-125">在将电子开票功能部署到电子开票附加产品服务环境之前，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9f668-125">Complete these steps before you deploy your Electronic invoicing feature to your Electronic invoicing add-on service environment.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9f668-126">先决条件</span><span class="sxs-lookup"><span data-stu-id="9f668-126">Prerequisites</span></span>

<span data-ttu-id="9f668-127">在完成本节中的步骤之前，创建并启动巴西 NF-e (BR) 电子开票功能的应用程序配置，如 [开始使用电子开票附加产品](e-invoicing-get-started.md)主题内的 **配置应用程序设置** 部分中所述。</span><span class="sxs-lookup"><span data-stu-id="9f668-127">Before you complete the procedure in this section, create and initiate the application configuration of the Brazilian NF-e (BR) Electronic invoicing feature as described in the **Configure the application setup** section in the topic, [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="9f668-128">在 RCS 内 **全球化功能** 工作区的 **功能** 部分，选择 **电子开票附加产品** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="9f668-128">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing add-on** tile.</span></span>
2. <span data-ttu-id="9f668-129">在 **电子开票附加产品功能** 页上，验证是否选择了 **巴西 NF-e (BR)** 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="9f668-129">On the **Electronic invoicing add-on Features** page, verify that the **Brazilian NF-e (BR)** Electronic invoicing feature is selected.</span></span>
3. <span data-ttu-id="9f668-130">在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。</span><span class="sxs-lookup"><span data-stu-id="9f668-130">On the **Versions** tab, verify that the **Draft** version is selected.</span></span>
4. <span data-ttu-id="9f668-131">在 **设置** 选项卡上，选择 **应用程序设置**，并在 **相连应用程序** 字段中，选择要部署到的应用程序。</span><span class="sxs-lookup"><span data-stu-id="9f668-131">On the **Setups** tab, select **Application setup** and in the **Connected application** field, select the application to where you want to deploy.</span></span>
5. <span data-ttu-id="9f668-132">在 **表名称** 字段中，验证是否选择了 **会计单据标题**。</span><span class="sxs-lookup"><span data-stu-id="9f668-132">In the **Table name** field, verify if **Fiscal document header** is selected.</span></span>
6. <span data-ttu-id="9f668-133">选择 **响应类型**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9f668-133">Select **Response types**, and then select **New**.</span></span>
7. <span data-ttu-id="9f668-134">在 **响应类型** 字段中，输入“响应”作为固定值，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="9f668-134">In the **Response type** field, enter "Response" as a fixed value, and in the **Description** field, enter "Description".</span></span>
8. <span data-ttu-id="9f668-135">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="9f668-135">In the **Submission status** field, select **Pending**.</span></span>
9. <span data-ttu-id="9f668-136">在 **模型映射** 字段中，选择具有 **（预览）响应消息导入格式** 的 **来自响应消息的模型映射**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9f668-136">In the **Model mapping** field, select **Model mapping from response  message** with **(Preview) Response message import format**, and then select **Save**.</span></span>
10. <span data-ttu-id="9f668-137">选择 **新建**，在 **响应类型** 字段中，输入“响应数据”作为固定值，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="9f668-137">Select **New** and in the **Response type** field, enter "ResponseData" as a fixed value and in the **Description** field, enter "Description".</span></span>
11. <span data-ttu-id="9f668-138">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="9f668-138">In the **Submission status** field, select **Pending**.</span></span>
12. <span data-ttu-id="9f668-139">在 **模型映射** 字段中，选择具有 **（预览）NF-e 响应数据导入格式 (BR)** 的 **响应数据导入**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9f668-139">In the **Model mapping** field, select **Response data import** with **(Preview) NF-e response data import format (BR)**, and then select **Save**.</span></span>
13. <span data-ttu-id="9f668-140">要部署电子开票功能，请参阅[开始使用电子开票附加产品](e-invoicing-get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="9f668-140">To deploy the Electronic invoicing feature, see [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a><span data-ttu-id="9f668-141">巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能的国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="9f668-141">Country-specific configuration for Brazilian NFS-e ABRASF Curitiba (BR) Electronic invoicing feature</span></span>

<span data-ttu-id="9f668-142">配置巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能需要完成特定步骤。</span><span class="sxs-lookup"><span data-stu-id="9f668-142">Configuring the Brazilian NFS-e ABRASF Curitiba (BR) Electronic invoicing feature requires that specific steps be completed.</span></span> <span data-ttu-id="9f668-143">所发布的配置中的某些参数采用了默认值，因此必须对其进行检查和更新以更好地适合您的业务操作。</span><span class="sxs-lookup"><span data-stu-id="9f668-143">Some of the parameters from the configurations are published with default values, so they must be reviewed and updated to better fit your business operation.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9f668-144">先决条件</span><span class="sxs-lookup"><span data-stu-id="9f668-144">Prerequisites</span></span>

<span data-ttu-id="9f668-145">在完成本节中的过程之前，请在组织中创建巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="9f668-145">Before you complete the procedure in this section, create a Brazilian NFS-e ABRASF Curitiba (BR) Electronic invoicing feature in your organization.</span></span> <span data-ttu-id="9f668-146">[开始使用电子开票附加产品](e-invoicing-get-started.md)主题中的 **配置电子开票功能** 部分对此进行了说明。</span><span class="sxs-lookup"><span data-stu-id="9f668-146">This is described in the **Configure Electronic invoicing feature** section in the topic, [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="9f668-147">在 RCS 内 **全球化功能** 工作区的 **功能** 部分，选择 **电子开票附加产品** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="9f668-147">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing add-on** tile.</span></span>
2. <span data-ttu-id="9f668-148">在 **电子开票附加产品功能** 页上，验证是否选择了您创建的 **巴西 NFS-e ABRASF 库里蒂巴 (BR)** 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="9f668-148">On the **Electronic invoicing add-on Features** page, verify that the **Brazilian NFS-e ABRASF Curitiba (BR)** Electronic invoicing feature you created is selected.</span></span>
3. <span data-ttu-id="9f668-149">在 **版本** 选项卡上，验证是否选择了 **草稿** 版本，然后在 **设置** 选项卡上的网格中，选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="9f668-149">On the **Versions** tab, verify the **Draft** version is selected, and on the **Setups** tab, in the grid, select **Submit**.</span></span>
4. <span data-ttu-id="9f668-150">选择 **编辑**，在 **操作** 选项卡上的 **操作** 字段组中，选择第一个出现的 **（预览）签署 xml 文档**。</span><span class="sxs-lookup"><span data-stu-id="9f668-150">Select **Edit** and on the **Actions** tab, in the **Actions** field group, select the first occurrence of **(Preview) Sign xml document**.</span></span>
5. <span data-ttu-id="9f668-151">在 **参数** 字段组中，选择 **证书名称**。</span><span class="sxs-lookup"><span data-stu-id="9f668-151">In the **Parameters** field group, select **Certificate name**.</span></span>
6. <span data-ttu-id="9f668-152">在 **值** 字段中，输入与您的密钥保管库参数关联的证书名称。</span><span class="sxs-lookup"><span data-stu-id="9f668-152">In the **Value** field, enter the name of certificate associated to your Key vault parameter.</span></span>
7. <span data-ttu-id="9f668-153">在 **操作** 字段组中，选择第二个出现的 **（预览）签署 xml 文档**。</span><span class="sxs-lookup"><span data-stu-id="9f668-153">In the **Actions** field group, select the second occurrence of **(Preview) Signxml document**.</span></span>
8. <span data-ttu-id="9f668-154">在 **参数** 字段组中，选择 **证书名称**。</span><span class="sxs-lookup"><span data-stu-id="9f668-154">In the **Parameters** field group, select **Certificate name**.</span></span>
9. <span data-ttu-id="9f668-155">在 **值** 字段中，输入与您的密钥保管库参数关联的证书名称。</span><span class="sxs-lookup"><span data-stu-id="9f668-155">In the **Value** field, enter the name of certificate associated to your Key vault parameter.</span></span>
10. <span data-ttu-id="9f668-156">在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）调用巴西 SEFAZ 服务** 操作。</span><span class="sxs-lookup"><span data-stu-id="9f668-156">On the **Actions** tab, in the **Actions** field group, select **(Preview) Call Brazilian SEFAZ service** action.</span></span>
11. <span data-ttu-id="9f668-157">在 **参数** 字段组中，选择 **URL 地址** 参数。</span><span class="sxs-lookup"><span data-stu-id="9f668-157">In the **Parameters** field group, select **URL address** parameter.</span></span>
12. <span data-ttu-id="9f668-158">在 **值** 字段中，如有必要，请查看并更新库里蒂巴市税务部门所发布的 Web 服务的 URL，然后选择 **保存。**</span><span class="sxs-lookup"><span data-stu-id="9f668-158">In the **Value** field, if necessary, review and update the URL of the web services published by the tax department for the city of Curitiba and then select **Save.**</span></span>
13. <span data-ttu-id="9f668-159">在 **设置** 选项卡上的网格中，选择 **查询**，然后选择 **编辑。**</span><span class="sxs-lookup"><span data-stu-id="9f668-159">On the **Setups** tab, in the grid, select **Inquire** and then select **Edit.**</span></span>
14. <span data-ttu-id="9f668-160">在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）调用巴西 SEFAZ 服务** 操作。</span><span class="sxs-lookup"><span data-stu-id="9f668-160">On the **Actions** tab, in the **Actions** field group, select **(Preview) Call Brazilian SEFAZ service** action.</span></span>
15. <span data-ttu-id="9f668-161">在 **参数** 字段组中，选择 **URL 地址** 参数。</span><span class="sxs-lookup"><span data-stu-id="9f668-161">In the **Parameters** field group, select **URL address** parameter.</span></span>
16. <span data-ttu-id="9f668-162">在 **值** 字段中，如有必要，请查看并更新库里蒂巴市税务部门所发布的 Web 服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="9f668-162">In the **Value** field, if necessary, review and update the URL of the web services published by the tax department for the city of Curitiba.</span></span>
17. <span data-ttu-id="9f668-163">选择 **保存**，然后关闭此页面。</span><span class="sxs-lookup"><span data-stu-id="9f668-163">Select **Save** and then close the page.</span></span>
18. <span data-ttu-id="9f668-164">要配置应用程序设置，请参阅[开始使用电子开票附加产品](e-invoicing-get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="9f668-164">To configure the application setup, see [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a><span data-ttu-id="9f668-165">巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能的应用程序设置的国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="9f668-165">Country-specific configuration of application setup for Brazilian NFS-e ABRASF Curitiba (BR) Electronic invoicing feature</span></span>

<span data-ttu-id="9f668-166">配置巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能的应用程序设置需要完成特定步骤，然后再将电子开票功能部署到电子开票附加产品服务环境。</span><span class="sxs-lookup"><span data-stu-id="9f668-166">Configuring the application setup for Brazilian NFS-e ABRASF Curitiba (BR) Electronic invoicing feature requires that specific steps be completed before you deploy your Electronic invoicing feature to your Electronic invoicing add-on service environment.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="9f668-167">先决条件</span><span class="sxs-lookup"><span data-stu-id="9f668-167">Prerequisites</span></span>

<span data-ttu-id="9f668-168">在完成本节中的步骤之前，创建并启动巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能，如 [开始使用电子开票附加产品](e-invoicing-get-started.md)主题内的 **配置应用程序设置** 部分中所述。</span><span class="sxs-lookup"><span data-stu-id="9f668-168">Before you complete the procedure in this section, create and initiate a Brazilian NFS-e ABRASF Curitiba (BR) Electronic invoicing feature as described in the section **Configure the application setup** in the topic, [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="9f668-169">在 RCS 内 **全球化功能** 工作区的 **功能** 部分，选择 **电子开票附加产品** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="9f668-169">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing add-on** tile.</span></span>
2. <span data-ttu-id="9f668-170">在 **电子开票附加产品功能** 页上，验证是否选择了 **巴西 NFS-e ABRASF 库里蒂巴 (BR)** 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="9f668-170">On the **Electronic invoicing add-on Features** page, verify that the **Brazilian NFS-e ABRASF Curitiba (BR)** Electronic invoicing feature is selected.</span></span>
3. <span data-ttu-id="9f668-171">在 **版本** 选项卡上，验证是否选择了 **草稿** 版本，然后在 **设置** 选项卡上，选择 **应用程序设置**。</span><span class="sxs-lookup"><span data-stu-id="9f668-171">On the **Versions** tab, verify that the **Draft** version is selected, and on the **Setups** tab, select **Application setup**.</span></span>
4. <span data-ttu-id="9f668-172">在 **相连应用程序** 字段中，选择要部署的应用程序。</span><span class="sxs-lookup"><span data-stu-id="9f668-172">In the **Connected application** field, select the application where you want to deploy.</span></span>
5. <span data-ttu-id="9f668-173">在 **表名称** 字段上，验证是否选择了会计单据标题。</span><span class="sxs-lookup"><span data-stu-id="9f668-173">On **Table name** field, verify that the fiscal document header is selected.</span></span>
6. <span data-ttu-id="9f668-174">选择 **响应类型**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9f668-174">Select **Response types** and select **New**.</span></span>
7. <span data-ttu-id="9f668-175">在 **响应类型** 字段中，输入“ABRASFCuritibaSubmitResponse”作为固定值，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="9f668-175">In the **Response type** field, enter "ABRASFCuritibaSubmitResponse" as a fixed value, and in the **Description** field, enter "Description".</span></span>
8. <span data-ttu-id="9f668-176">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="9f668-176">In the **Submission status** field, select **Pending**.</span></span>
9. <span data-ttu-id="9f668-177">在 **模型映射** 字段中，选择 **响应消息导入** 以及 **（预览）NFS-e ABRASF 库里蒂巴响应消息导入 (BR)**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9f668-177">In the **Model mapping** field, select **Response message import**, with **(Preview) NFS-e ABRASF Curitiba response message import (BR)** and then select **Save**.</span></span>
10. <span data-ttu-id="9f668-178">选择 **新建**，在 **响应类型** 字段中，输入“ABRASFCuritibaSubmitResponseData”，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="9f668-178">Select **New**, and in the **Response type** field, enter "ABRASFCuritibaSubmitResponseData", and in the **Description** field, enter "Description".</span></span>
11. <span data-ttu-id="9f668-179">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="9f668-179">In the **Submission status** field, select **Pending**.</span></span>
12. <span data-ttu-id="9f668-180">在 **模型映射** 字段中，选择具有 **（预览）NFS-e ABRASF 响应数据导入格式 (BR)** 的 **响应数据导入**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9f668-180">In the **Model mapping** field, select **Response data import**, with **(Preview) NFS-e ABRASF response data import format (BR)** and then select **Save**.</span></span>
13. <span data-ttu-id="9f668-181">选择 **新建**，在 **响应类型** 字段中，输入“ABRASFCuritibaInquireResponse”，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="9f668-181">Select **New**, and in the **Response type** field, enter "ABRASFCuritibaInquireResponse", and in the **Description** field, enter "Description".</span></span>
14. <span data-ttu-id="9f668-182">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="9f668-182">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="9f668-183">在 **模型映射** 字段中，选择 **响应消息导入** 以及 **（预览）NFS-e ABRASF 库里蒂巴响应消息导入 (BR)**。</span><span class="sxs-lookup"><span data-stu-id="9f668-183">In the **Model mapping** field, select **Response message import**, with **(Preview) NFS-e ABRASF Curitiba response message import (BR).**</span></span>
16. <span data-ttu-id="9f668-184">选择 **保存**，然后返回到[开始使用电子开票附加产品](e-invoicing-get-started.md)主题，以部署电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="9f668-184">Select **Save** and then return to the topic, [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md) to deploy the Electronic invoicing feature.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="9f668-185">隐私声明</span><span class="sxs-lookup"><span data-stu-id="9f668-185">Privacy notice</span></span>
<span data-ttu-id="9f668-186">启用 **NF-e 联邦 - 巴西电子发票 (BR)** 和 **NFS-e - 巴西服务（城市）电子发票** 功能可能需要发送有限的数据，包括组织税务注册 ID。</span><span class="sxs-lookup"><span data-stu-id="9f668-186">Enabling the **NF-e Federal - Brazilian electronic invoice (BR)** and the **NFS-e - Brazilian service (city) electronic invoice** features may require sending limited data, including the organization tax registration ID.</span></span> <span data-ttu-id="9f668-187">此数据会传输到税务机构授权的第三方机构，以便以与政府的 Web 服务集成所需的预定义格式向该税务机构发送电子发票。</span><span class="sxs-lookup"><span data-stu-id="9f668-187">This data is transmitted to third-party agencies authorized by the tax authority for the purpose of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="9f668-188">作为管理员，您可以启用或关闭 **NF-e 联邦 - 巴西电子发票 (BR)** 和 **NFS-e - 巴西服务（城市）电子发票** 功能。</span><span class="sxs-lookup"><span data-stu-id="9f668-188">As an administrator, you can enable or turn off the **NF-e Federal - Brazilian electronic invoice (BR)** and the **NFS-e - Brazilian service (city) electronic invoice** features.</span></span> <span data-ttu-id="9f668-189">以下步骤表明了如何执行此操作：</span><span class="sxs-lookup"><span data-stu-id="9f668-189">The following steps show how to do this:</span></span> 

1. <span data-ttu-id="9f668-190">转到 **组织管理** > **设置** > **电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="9f668-190">Go to **Organization administration** > **Setup** > **Electronic document parameters**.</span></span> 
2. <span data-ttu-id="9f668-191">在 **功能** 选项卡上，选择包含 **NF-e 联邦 - 巴西电子发票 (BR)** 或 **NFS-e - 巴西服务（城市）电子发票** 功能的行，然后选择相应的功能。</span><span class="sxs-lookup"><span data-stu-id="9f668-191">On the **Features** tab, select the row that contains the **NF-e Federal - Brazilian electronic invoice (BR)** or the **NFS-e - Brazilian service (city) electronic invoice** feature, and select the feature.</span></span> <span data-ttu-id="9f668-192">从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。</span><span class="sxs-lookup"><span data-stu-id="9f668-192">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="9f668-193">有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。</span><span class="sxs-lookup"><span data-stu-id="9f668-193">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9f668-194">其他资源</span><span class="sxs-lookup"><span data-stu-id="9f668-194">Additional resources</span></span>

- [<span data-ttu-id="9f668-195">电子开票加载项概览</span><span class="sxs-lookup"><span data-stu-id="9f668-195">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="9f668-196">开始使用电子开票加载项服务管理</span><span class="sxs-lookup"><span data-stu-id="9f668-196">Get started with Electronic invoicing add-on service administration</span></span>](e-invoicing-get-started-service-administration.md)
- [<span data-ttu-id="9f668-197">开始使用电子开票加载项</span><span class="sxs-lookup"><span data-stu-id="9f668-197">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
