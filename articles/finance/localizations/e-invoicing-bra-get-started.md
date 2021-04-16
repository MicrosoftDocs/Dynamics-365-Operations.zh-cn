---
title: 开始使用适用于巴西的电子开票
description: 本主题提供的信息将帮助您开始使用 Finance 和 Supply Chain Management 中适用于巴西的电子开票。
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: f8caaa6417365a131da0565cbc4a9f79425d0c7e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840260"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a><span data-ttu-id="82e42-103">开始使用适用于巴西的电子开票</span><span class="sxs-lookup"><span data-stu-id="82e42-103">Get started with Electronic invoicing for Brazil</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82e42-104">本主题提供的信息将帮助您开始使用适用于巴西的电子开票。</span><span class="sxs-lookup"><span data-stu-id="82e42-104">This topic provides information that will help you get started with Electronic invoicing for Brazil.</span></span> <span data-ttu-id="82e42-105">本主题将指导您完成 Regulatory Configuration Services (RCS) 中与国家/地区有关的配置步骤，并补充[开始使用电子开票](e-invoicing-get-started.md)主题中描述的步骤。</span><span class="sxs-lookup"><span data-stu-id="82e42-105">The topic guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS), and complement the steps described in the topic, [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a><span data-ttu-id="82e42-106">巴西 NF-e (BR) 电子开票功能的国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="82e42-106">Country-specific configuration for Brazilian NF-e (BR) Electronic invoicing feature</span></span>

<span data-ttu-id="82e42-107">**巴西 NF-e (BR) 电子开票功能** 的一些参数使用默认值发布。</span><span class="sxs-lookup"><span data-stu-id="82e42-107">Some of the parameters from the **Brazilian NF-e (BR) Electronic invoicing feature** are published with default values.</span></span> <span data-ttu-id="82e42-108">在将电子开票功能部署到服务环境之前，查看并（如有必要）更新这些值以更好地反映您的业务操作。</span><span class="sxs-lookup"><span data-stu-id="82e42-108">Review the values and if necessary, update the values to better reflect your business operation before you deploy the Electronic invoicing feature to the Service environment.</span></span>

<span data-ttu-id="82e42-109">此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **电子开票功能的国家/地区特定配置** 部分。</span><span class="sxs-lookup"><span data-stu-id="82e42-109">This section complements the **Country-specific configuration for Electronic invoicing feature** section in the topic, [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="82e42-110">在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="82e42-110">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing** tile.</span></span>
2. <span data-ttu-id="82e42-111">在 **电子开票功能** 页面上，验证是否选择了您创建的 **巴西 NF-e (BR)** 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="82e42-111">On the **Electronic invoicing Features** page, verify that the **Brazilian NF-e (BR)** Electronic invoicing feature you created is selected.</span></span>
3. <span data-ttu-id="82e42-112">在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。</span><span class="sxs-lookup"><span data-stu-id="82e42-112">On the **Versions** tab, verify that the **Draft** version is selected.</span></span>
4. <span data-ttu-id="82e42-113">在 **设置** 选项卡上的网格中，选择 **提交**，然后选择 **编辑。**</span><span class="sxs-lookup"><span data-stu-id="82e42-113">On the **Setups** tab, in the grid, select **Submit** and then select **Edit.**</span></span>
5. <span data-ttu-id="82e42-114">在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）签署 xml 文档** 操作。</span><span class="sxs-lookup"><span data-stu-id="82e42-114">On the **Actions** tab, in the **Actions** field group, select **(Preview) Sign xml document** action.</span></span>
6. <span data-ttu-id="82e42-115">在 **参数** 字段组中，选择 **证书名称**，并在 **值** 字段中，输入与您的密钥保管库参数关联的证书名称。</span><span class="sxs-lookup"><span data-stu-id="82e42-115">In the **Parameters** field group, select **Certificate name**, and in the **Value** field, enter the name of certificate associated to your Key vault parameter.</span></span>
7. <span data-ttu-id="82e42-116">在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）调用巴西 SEFAZ 服务** 操作。</span><span class="sxs-lookup"><span data-stu-id="82e42-116">On the **Actions** tab, in the **Actions** field group, select **(Preview) Call Brazilian SEFAZ service** action.</span></span>
8. <span data-ttu-id="82e42-117">在 **参数** 字段组中，选择 **URL 地址** 参数。</span><span class="sxs-lookup"><span data-stu-id="82e42-117">In the **Parameters** field group, select **URL address** parameter.</span></span>
9. <span data-ttu-id="82e42-118">在 **值** 字段中，如有必要，请查看并更新您所在州的 SEFAZ 文档所发布的 Web 服务的 URL，然后选择 **保存。**</span><span class="sxs-lookup"><span data-stu-id="82e42-118">In the **Value** field, if necessary, review and update the URL of the web services published by the SEFAZ documentation for your state and then select **Save.**</span></span>
10. <span data-ttu-id="82e42-119">在 **适用性规则** 选项卡上的 **适用性规则设置** 字段组中，查看 **洲** 字段，并根据需要针对与 Web 服务 URL 所引用的相同洲对其进行更新。</span><span class="sxs-lookup"><span data-stu-id="82e42-119">On the **Applicability rules** tab, in the **Setup of applicability rule** field group, review and update the **State** field criteria as necessary for the same state, which the URL of the web services is referred to.</span></span>
11. <span data-ttu-id="82e42-120">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="82e42-120">Select **Save** and close the page.</span></span>
12. <span data-ttu-id="82e42-121">若要将电子开票功能部署到服务环境，请参阅[开始使用电子开票](e-invoicing-get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="82e42-121">To deploy the Electronic invoicing feature to the Service environment, see [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a><span data-ttu-id="82e42-122">巴西 NF-e (BR) 电子开票功能的应用程序设置的国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="82e42-122">Country-specific configuration of application setup for Brazilian NF-e (BR) Electronic invoicing feature</span></span>

<span data-ttu-id="82e42-123">在将应用程序设置部署到 Finance 或 Supply Chain Management 连接的应用程序之前，请完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="82e42-123">Complete these steps before you deploy the application setup to your Finance or Supply Chain Management connected application.</span></span>

<span data-ttu-id="82e42-124">此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **应用程序设置的国家/地区特定配置** 部分。</span><span class="sxs-lookup"><span data-stu-id="82e42-124">This section complements the **Country-specific configuration of Application setup** section in the topic, [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="82e42-125">在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择\**电子开票* 磁贴。</span><span class="sxs-lookup"><span data-stu-id="82e42-125">In RCS, in the **Features** section of the **Globalization feature** workspace, select the \**Electronic invoicing* tile.</span></span>
2. <span data-ttu-id="82e42-126">在 **电子开票功能** 页面上，验证是否选择了 **巴西 NF-e (BR)** 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="82e42-126">On the **Electronic invoicing Features** page, verify that the **Brazilian NF-e (BR)** Electronic invoicing feature is selected.</span></span>
3. <span data-ttu-id="82e42-127">在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。</span><span class="sxs-lookup"><span data-stu-id="82e42-127">On the **Versions** tab, verify that the **Draft** version is selected.</span></span>
4. <span data-ttu-id="82e42-128">在 **设置** 选项卡上，选择 **应用程序设置**，并在 **相连应用程序** 字段中，选择要部署到的应用程序。</span><span class="sxs-lookup"><span data-stu-id="82e42-128">On the **Setups** tab, select **Application setup** and in the **Connected application** field, select the application to where you want to deploy.</span></span>
5. <span data-ttu-id="82e42-129">在 **表名称** 字段中，验证是否选择了 **会计单据标题**。</span><span class="sxs-lookup"><span data-stu-id="82e42-129">In the **Table name** field, verify if **Fiscal document header** is selected.</span></span>
6. <span data-ttu-id="82e42-130">选择 **响应类型**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="82e42-130">Select **Response types**, and then select **New**.</span></span>
7. <span data-ttu-id="82e42-131">在 **响应类型** 字段中，输入“响应”作为固定值，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="82e42-131">In the **Response type** field, enter "Response" as a fixed value, and in the **Description** field, enter "Description".</span></span>
8. <span data-ttu-id="82e42-132">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="82e42-132">In the **Submission status** field, select **Pending**.</span></span>
9. <span data-ttu-id="82e42-133">在 **模型映射** 字段中，选择具有 **（预览）响应消息导入格式** 的 **来自响应消息的模型映射**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="82e42-133">In the **Model mapping** field, select **Model mapping from response  message** with **(Preview) Response message import format**, and then select **Save**.</span></span>
10. <span data-ttu-id="82e42-134">选择 **新建**，在 **响应类型** 字段中，输入“响应数据”作为固定值，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="82e42-134">Select **New** and in the **Response type** field, enter "ResponseData" as a fixed value and in the **Description** field, enter "Description".</span></span>
11. <span data-ttu-id="82e42-135">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="82e42-135">In the **Submission status** field, select **Pending**.</span></span>
12. <span data-ttu-id="82e42-136">在 **模型映射** 字段中，选择具有 **（预览）NF-e 响应数据导入格式 (BR)** 的 **响应数据导入**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="82e42-136">In the **Model mapping** field, select **Response data import** with **(Preview) NF-e response data import format (BR)**, and then select **Save**.</span></span>
13. <span data-ttu-id="82e42-137">若要将应用程序设置部署到 Finance 或 Supply Chain 连接的应用程序，请参阅[开始使用电子开票](e-invoicing-get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="82e42-137">To deploy the application setup to the Finance or Supply Chain connected application, see [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a><span data-ttu-id="82e42-138">巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能的国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="82e42-138">Country-specific configuration for Brazilian NFS-e ABRASF Curitiba (BR) Electronic invoicing feature</span></span>

<span data-ttu-id="82e42-139">**巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能** 的一些参数使用默认值发布。</span><span class="sxs-lookup"><span data-stu-id="82e42-139">Some of the parameters from the **Brazilian NFS-e ABRASF Curitiba (BR) Electronic invoicing feature** are published with default values.</span></span> <span data-ttu-id="82e42-140">在将电子开票功能部署到服务环境之前，查看并（如有必要）更新这些值以更好地满足您的业务操作需求。</span><span class="sxs-lookup"><span data-stu-id="82e42-140">Review and, if necessary, update the values to better fit your business operation needs before you deploy the Electronic invoicing feature to the Service environment.</span></span>

<span data-ttu-id="82e42-141">此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **电子开票功能的国家/地区特定配置** 部分。</span><span class="sxs-lookup"><span data-stu-id="82e42-141">This section complements the **Country-specific configuration for Electronic invoicing feature** section in the topic, [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="82e42-142">在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="82e42-142">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing** tile.</span></span>
2. <span data-ttu-id="82e42-143">在 **电子开票功能** 页面上，验证是否选择了您创建的 **巴西 NFS-e ABRASF 库里蒂巴 (BR)** 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="82e42-143">On the **Electronic invoicing Features** page, verify that the **Brazilian NFS-e ABRASF Curitiba (BR)** Electronic invoicing feature you created is selected.</span></span>
3. <span data-ttu-id="82e42-144">在 **版本** 选项卡上，验证是否选择了 **草稿** 版本，然后在 **设置** 选项卡上的网格中，选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="82e42-144">On the **Versions** tab, verify the **Draft** version is selected, and on the **Setups** tab, in the grid, select **Submit**.</span></span>
4. <span data-ttu-id="82e42-145">选择 **编辑**，在 **操作** 选项卡上的 **操作** 字段组中，选择第一个出现的 **（预览）签署 xml 文档**。</span><span class="sxs-lookup"><span data-stu-id="82e42-145">Select **Edit** and on the **Actions** tab, in the **Actions** field group, select the first occurrence of **(Preview) Sign xml document**.</span></span>
5. <span data-ttu-id="82e42-146">在 **参数** 字段组中，选择 **证书名称**。</span><span class="sxs-lookup"><span data-stu-id="82e42-146">In the **Parameters** field group, select **Certificate name**.</span></span>
6. <span data-ttu-id="82e42-147">在 **值** 字段中，输入与您的密钥保管库参数关联的证书名称。</span><span class="sxs-lookup"><span data-stu-id="82e42-147">In the **Value** field, enter the name of certificate associated to your Key vault parameter.</span></span>
7. <span data-ttu-id="82e42-148">在 **操作** 字段组中，选择第二个出现的 **（预览）签署 xml 文档**。</span><span class="sxs-lookup"><span data-stu-id="82e42-148">In the **Actions** field group, select the second occurrence of **(Preview) Signxml document**.</span></span>
8. <span data-ttu-id="82e42-149">在 **参数** 字段组中，选择 **证书名称**。</span><span class="sxs-lookup"><span data-stu-id="82e42-149">In the **Parameters** field group, select **Certificate name**.</span></span>
9. <span data-ttu-id="82e42-150">在 **值** 字段中，输入与您的密钥保管库参数关联的证书名称。</span><span class="sxs-lookup"><span data-stu-id="82e42-150">In the **Value** field, enter the name of certificate associated to your Key vault parameter.</span></span>
10. <span data-ttu-id="82e42-151">在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）调用巴西 SEFAZ 服务** 操作。</span><span class="sxs-lookup"><span data-stu-id="82e42-151">On the **Actions** tab, in the **Actions** field group, select **(Preview) Call Brazilian SEFAZ service** action.</span></span>
11. <span data-ttu-id="82e42-152">在 **参数** 字段组中，选择 **URL 地址** 参数。</span><span class="sxs-lookup"><span data-stu-id="82e42-152">In the **Parameters** field group, select **URL address** parameter.</span></span>
12. <span data-ttu-id="82e42-153">在 **值** 字段中，如有必要，请查看并更新库里蒂巴市税务部门所发布的 Web 服务的 URL，然后选择 **保存。**</span><span class="sxs-lookup"><span data-stu-id="82e42-153">In the **Value** field, if necessary, review and update the URL of the web services published by the tax department for the city of Curitiba and then select **Save.**</span></span>
13. <span data-ttu-id="82e42-154">在 **设置** 选项卡上的网格中，选择 **查询**，然后选择 **编辑。**</span><span class="sxs-lookup"><span data-stu-id="82e42-154">On the **Setups** tab, in the grid, select **Inquire** and then select **Edit.**</span></span>
14. <span data-ttu-id="82e42-155">在 **操作** 选项卡上的 **操作** 字段组中，选择 **（预览）调用巴西 SEFAZ 服务** 操作。</span><span class="sxs-lookup"><span data-stu-id="82e42-155">On the **Actions** tab, in the **Actions** field group, select **(Preview) Call Brazilian SEFAZ service** action.</span></span>
15. <span data-ttu-id="82e42-156">在 **参数** 字段组中，选择 **URL 地址** 参数。</span><span class="sxs-lookup"><span data-stu-id="82e42-156">In the **Parameters** field group, select **URL address** parameter.</span></span>
16. <span data-ttu-id="82e42-157">在 **值** 字段中，如有必要，请查看并更新库里蒂巴市税务部门所发布的 Web 服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="82e42-157">In the **Value** field, if necessary, review and update the URL of the web services published by the tax department for the city of Curitiba.</span></span>
17. <span data-ttu-id="82e42-158">选择 **保存**，然后关闭此页面。</span><span class="sxs-lookup"><span data-stu-id="82e42-158">Select **Save** and then close the page.</span></span>
18. <span data-ttu-id="82e42-159">若要将电子开票功能部署到服务环境，请参阅[开始使用电子开票](e-invoicing-get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="82e42-159">To deploy the Electronic invoicing feature to the Service environment, see [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a><span data-ttu-id="82e42-160">巴西 NFS-e ABRASF 库里蒂巴 (BR) 电子开票功能的应用程序设置的国家/地区特定配置</span><span class="sxs-lookup"><span data-stu-id="82e42-160">Country-specific configuration of application setup for Brazilian NFS-e ABRASF Curitiba (BR) Electronic invoicing feature</span></span>

<span data-ttu-id="82e42-161">在将应用程序设置部署到 Finance 或 Supply Chain Management 连接的应用程序之前，请完成这些步骤。</span><span class="sxs-lookup"><span data-stu-id="82e42-161">Complete these steps before you deploy the application setup to your Finance or Supply Chain Management connected application.</span></span>

<span data-ttu-id="82e42-162">此部分补充 [开始使用电子开票](e-invoicing-get-started.md)主题中的 **应用程序设置的国家/地区特定配置** 部分。</span><span class="sxs-lookup"><span data-stu-id="82e42-162">This section complements the **Country-specific configuration of application setup** section in the topic, [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="82e42-163">在 RCS 中的 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="82e42-163">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing** tile.</span></span>
2. <span data-ttu-id="82e42-164">在 **电子开票功能** 页面上，验证是否选择了 **巴西 NFS-e ABRASF 库里蒂巴 (BR)** 电子开票功能。</span><span class="sxs-lookup"><span data-stu-id="82e42-164">On the **Electronic invoicing Features** page, verify that the **Brazilian NFS-e ABRASF Curitiba (BR)** Electronic invoicing feature is selected.</span></span>
3. <span data-ttu-id="82e42-165">在 **版本** 选项卡上，验证是否选择了 **草稿** 版本，然后在 **设置** 选项卡上，选择 **应用程序设置**。</span><span class="sxs-lookup"><span data-stu-id="82e42-165">On the **Versions** tab, verify that the **Draft** version is selected, and on the **Setups** tab, select **Application setup**.</span></span>
4. <span data-ttu-id="82e42-166">在 **相连应用程序** 字段中，选择要部署的应用程序。</span><span class="sxs-lookup"><span data-stu-id="82e42-166">In the **Connected application** field, select the application where you want to deploy.</span></span>
5. <span data-ttu-id="82e42-167">在 **表名称** 字段上，验证是否选择了会计单据标题。</span><span class="sxs-lookup"><span data-stu-id="82e42-167">On **Table name** field, verify that the fiscal document header is selected.</span></span>
6. <span data-ttu-id="82e42-168">选择 **响应类型**，然后选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="82e42-168">Select **Response types** and select **New**.</span></span>
7. <span data-ttu-id="82e42-169">在 **响应类型** 字段中，输入“ABRASFCuritibaSubmitResponse”作为固定值，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="82e42-169">In the **Response type** field, enter "ABRASFCuritibaSubmitResponse" as a fixed value, and in the **Description** field, enter "Description".</span></span>
8. <span data-ttu-id="82e42-170">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="82e42-170">In the **Submission status** field, select **Pending**.</span></span>
9. <span data-ttu-id="82e42-171">在 **模型映射** 字段中，选择 **响应消息导入** 以及 **（预览）NFS-e ABRASF 库里蒂巴响应消息导入 (BR)**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="82e42-171">In the **Model mapping** field, select **Response message import**, with **(Preview) NFS-e ABRASF Curitiba response message import (BR)** and then select **Save**.</span></span>
10. <span data-ttu-id="82e42-172">选择 **新建**，在 **响应类型** 字段中，输入“ABRASFCuritibaSubmitResponseData”，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="82e42-172">Select **New**, and in the **Response type** field, enter "ABRASFCuritibaSubmitResponseData", and in the **Description** field, enter "Description".</span></span>
11. <span data-ttu-id="82e42-173">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="82e42-173">In the **Submission status** field, select **Pending**.</span></span>
12. <span data-ttu-id="82e42-174">在 **模型映射** 字段中，选择具有 **（预览）NFS-e ABRASF 响应数据导入格式 (BR)** 的 **响应数据导入**，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="82e42-174">In the **Model mapping** field, select **Response data import**, with **(Preview) NFS-e ABRASF response data import format (BR)** and then select **Save**.</span></span>
13. <span data-ttu-id="82e42-175">选择 **新建**，在 **响应类型** 字段中，输入“ABRASFCuritibaInquireResponse”，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="82e42-175">Select **New**, and in the **Response type** field, enter "ABRASFCuritibaInquireResponse", and in the **Description** field, enter "Description".</span></span>
14. <span data-ttu-id="82e42-176">在 **提交状态** 字段中，选择 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="82e42-176">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="82e42-177">在 **模型映射** 字段中，选择 **响应消息导入** 以及 **（预览）NFS-e ABRASF 库里蒂巴响应消息导入 (BR)**。</span><span class="sxs-lookup"><span data-stu-id="82e42-177">In the **Model mapping** field, select **Response message import**, with **(Preview) NFS-e ABRASF Curitiba response message import (BR).**</span></span>
16. <span data-ttu-id="82e42-178">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="82e42-178">Select **Save** and close the page.</span></span>
17. <span data-ttu-id="82e42-179">若要将应用程序设置部署到 Finance 或 Supply Chain 连接的应用程序，请参阅[开始使用电子开票](e-invoicing-get-started.md)。</span><span class="sxs-lookup"><span data-stu-id="82e42-179">To deploy the application setup to the Finance or Supply Chain connected application, see [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="82e42-180">隐私声明</span><span class="sxs-lookup"><span data-stu-id="82e42-180">Privacy notice</span></span>
<span data-ttu-id="82e42-181">启用 **NF-e 联邦 - 巴西电子发票 (BR)** 和 **NFS-e - 巴西服务（城市）电子发票** 功能可能需要发送有限的数据，包括组织税务注册 ID。</span><span class="sxs-lookup"><span data-stu-id="82e42-181">Enabling the **NF-e Federal - Brazilian electronic invoice (BR)** and the **NFS-e - Brazilian service (city) electronic invoice** features may require sending limited data, including the organization tax registration ID.</span></span> <span data-ttu-id="82e42-182">此数据会传输到税务机构授权的第三方机构，以便以与政府的 Web 服务集成所需的预定义格式向该税务机构发送电子发票。</span><span class="sxs-lookup"><span data-stu-id="82e42-182">This data is transmitted to third-party agencies authorized by the tax authority for the purpose of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="82e42-183">作为管理员，您可以启用或关闭 **NF-e 联邦 - 巴西电子发票 (BR)** 和 **NFS-e - 巴西服务（城市）电子发票** 功能。</span><span class="sxs-lookup"><span data-stu-id="82e42-183">As an administrator, you can enable or turn off the **NF-e Federal - Brazilian electronic invoice (BR)** and the **NFS-e - Brazilian service (city) electronic invoice** features.</span></span> <span data-ttu-id="82e42-184">以下步骤表明了如何执行此操作：</span><span class="sxs-lookup"><span data-stu-id="82e42-184">The following steps show how to do this:</span></span> 

1. <span data-ttu-id="82e42-185">转到 **组织管理** > **设置** > **电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="82e42-185">Go to **Organization administration** > **Setup** > **Electronic document parameters**.</span></span> 
2. <span data-ttu-id="82e42-186">在 **功能** 选项卡上，选择包含 **NF-e 联邦 - 巴西电子发票 (BR)** 或 **NFS-e - 巴西服务（城市）电子发票** 功能的行，然后选择相应的功能。</span><span class="sxs-lookup"><span data-stu-id="82e42-186">On the **Features** tab, select the row that contains the **NF-e Federal - Brazilian electronic invoice (BR)** or the **NFS-e - Brazilian service (city) electronic invoice** feature, and select the feature.</span></span> <span data-ttu-id="82e42-187">从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。</span><span class="sxs-lookup"><span data-stu-id="82e42-187">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="82e42-188">有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。</span><span class="sxs-lookup"><span data-stu-id="82e42-188">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82e42-189">其他资源</span><span class="sxs-lookup"><span data-stu-id="82e42-189">Additional resources</span></span>

- [<span data-ttu-id="82e42-190">电子开票概览</span><span class="sxs-lookup"><span data-stu-id="82e42-190">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="82e42-191">开始使用电子开票服务管理</span><span class="sxs-lookup"><span data-stu-id="82e42-191">Get started with Electronic invoicing service administration</span></span>](e-invoicing-get-started-service-administration.md)
- [<span data-ttu-id="82e42-192">开始使用电子开票</span><span class="sxs-lookup"><span data-stu-id="82e42-192">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
