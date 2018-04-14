---
title: "设置信用和收款"
description: "本文介绍如何设置收款功能。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e5c96f16a2c6a4bc5213293e0dbaac3918a6e9c5
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-credit-and-collections"></a><span data-ttu-id="bd249-103">设置信用和收款</span><span class="sxs-lookup"><span data-stu-id="bd249-103">Set up Credit and collections</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bd249-104">本文介绍如何设置收款功能。</span><span class="sxs-lookup"><span data-stu-id="bd249-104">This article explains how to set up the collections functionality.</span></span>

<a name="set-up-aging-period-definitions"></a><span data-ttu-id="bd249-105">设置帐龄期间定义</span><span class="sxs-lookup"><span data-stu-id="bd249-105">Set up aging period definitions</span></span>
-------------------------------

<span data-ttu-id="bd249-106">设置帐龄期间定义。</span><span class="sxs-lookup"><span data-stu-id="bd249-106">Set up an aging period definition.</span></span> <span data-ttu-id="bd249-107">帐龄期间定义用于定义在**“帐龄余额”**、**“收款活动”**和**“收款案例”**列表页上显示的列。</span><span class="sxs-lookup"><span data-stu-id="bd249-107">An aging period definition defines the columns that appear on the **Aged balances**, **Collections activities**, and **Collections cases** list pages.</span></span> <span data-ttu-id="bd249-108">它还定义在**“收款”**页上显示的期间。</span><span class="sxs-lookup"><span data-stu-id="bd249-108">It also defines the periods that appear on the **Collections** page.</span></span> <span data-ttu-id="bd249-109">如果设置客户池，使用池的帐龄期间定义。</span><span class="sxs-lookup"><span data-stu-id="bd249-109">If a customer pool is set up, the aging period definition for the pool is used.</span></span> <span data-ttu-id="bd249-110">如果未设置池，则使用在**“应收账款参数”**页中指定的默认帐龄期间定义。</span><span class="sxs-lookup"><span data-stu-id="bd249-110">If no pools are set up, the default aging period definition that is specified on the **Accounts receivable parameters** page is used.</span></span> <span data-ttu-id="bd249-111">如果默认帐龄期间定义未指定，则在**“帐龄期间定义”**页中使用第一个帐龄期间定义。</span><span class="sxs-lookup"><span data-stu-id="bd249-111">If no default aging period definition is specified, the first aging period definition on the **Aging period definitions** page is used.</span></span>

## <a name="create-an-aging-snapshot"></a><span data-ttu-id="bd249-112">创建一个帐龄快照</span><span class="sxs-lookup"><span data-stu-id="bd249-112">Create an aging snapshot</span></span>
<span data-ttu-id="bd249-113">为所有客户或在客户池的客户创建帐龄快照记录。</span><span class="sxs-lookup"><span data-stu-id="bd249-113">Create aging snapshot records for all customers or for the customers in a customer pool.</span></span> <span data-ttu-id="bd249-114">帐龄快照信息将显示在**“帐龄余额”**列表页和**“收款”**页上。</span><span class="sxs-lookup"><span data-stu-id="bd249-114">Aging snapshot information appears on the **Aged balances** list page and on the **Collections** page.</span></span> <span data-ttu-id="bd249-115">您必须创建一个帐龄快照，然后才能使用列表页。</span><span class="sxs-lookup"><span data-stu-id="bd249-115">You must create an aging snapshot before you can use the list page.</span></span> <span data-ttu-id="bd249-116">列表页只为已经创建帐龄快照的客户显示信息。</span><span class="sxs-lookup"><span data-stu-id="bd249-116">The list page shows information only for customers that an aging snapshot has been created for.</span></span>

## <a name="optional-set-up-customer-pools"></a><span data-ttu-id="bd249-117">可选：设置客户池</span><span class="sxs-lookup"><span data-stu-id="bd249-117">Optional: Set up customer pools</span></span>
<span data-ttu-id="bd249-118">您可以设置客户池表示客户组。</span><span class="sxs-lookup"><span data-stu-id="bd249-118">You can set up customer pools to represent groups of customers.</span></span> <span data-ttu-id="bd249-119">您可以使用客户池用作筛选器用于显示在**“收款”**列表页上、**“收款”**页上的客户信息，或者，当您创建帐龄快照时。</span><span class="sxs-lookup"><span data-stu-id="bd249-119">You can use customer pools as filters for the customer information that appears on **Collections** list pages, on the **Collections** page, or when you create aging snapshots.</span></span>

## <a name="optional-create-a-collections-team"></a><span data-ttu-id="bd249-120">可选：创建集合团队</span><span class="sxs-lookup"><span data-stu-id="bd249-120">Optional: Create a collections team</span></span>
<span data-ttu-id="bd249-121">如果您的组织的多个人员执行收款工作，您可以设置收款团队。</span><span class="sxs-lookup"><span data-stu-id="bd249-121">If multiple people in your organization do collections work, you can set up a collections team.</span></span> <span data-ttu-id="bd249-122">您可以在**“应收账款参数”**页上选择团队。</span><span class="sxs-lookup"><span data-stu-id="bd249-122">You can select the team on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="bd249-123">如果没有创建收款团队，则当您在**“收款代理”**页上设置收款代理时将自动创建一个团队。</span><span class="sxs-lookup"><span data-stu-id="bd249-123">If you don't create a collections team, a team is created automatically when you set up collections agents on the **Collections agent** page.</span></span>

## <a name="set-up-a-collections-case-category"></a><span data-ttu-id="bd249-124">设置集合案例类别</span><span class="sxs-lookup"><span data-stu-id="bd249-124">Set up a collections case category</span></span>
<span data-ttu-id="bd249-125">如果您使用案例组织您的收款工作，请设置具有**“收款”**类别类型的案例类别。</span><span class="sxs-lookup"><span data-stu-id="bd249-125">If you will use cases to organize your collections work, set up a case category that has the **Collections** category type.</span></span> <span data-ttu-id="bd249-126">只有当您要在**“收款”**页上使用案例功能时，此设置才是必需的。</span><span class="sxs-lookup"><span data-stu-id="bd249-126">This setup is required only if you want to use the case functionality on the **Collections** page.</span></span>

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a><span data-ttu-id="bd249-127">设置日志名称（结算、冲销和资金不足）</span><span class="sxs-lookup"><span data-stu-id="bd249-127">Set up journal names (settlement, writeoff, and NSF)</span></span>
<span data-ttu-id="bd249-128">设置当您在**“收款”**页上处理交易记录时使用的日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="bd249-128">Set up the journal names that are used when transactions are processed on the **Collections** page.</span></span> <span data-ttu-id="bd249-129">此处理包括结算交易记录，冲销交易记录和处理资金不足 (NSF) 付款。</span><span class="sxs-lookup"><span data-stu-id="bd249-129">This processing includes settlement of a transaction, write-off of a transaction, and processing of a not sufficient funds (NSF) payment.</span></span>

| <span data-ttu-id="bd249-130">描述</span><span class="sxs-lookup"><span data-stu-id="bd249-130">Description</span></span> | <span data-ttu-id="bd249-131">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="bd249-131">Journal type</span></span>     |
|-------------|------------------|
| <span data-ttu-id="bd249-132">结算</span><span class="sxs-lookup"><span data-stu-id="bd249-132">Settlement</span></span>  | <span data-ttu-id="bd249-133">客户 - 付款</span><span class="sxs-lookup"><span data-stu-id="bd249-133">Customer payment</span></span> |
| <span data-ttu-id="bd249-134">销帐</span><span class="sxs-lookup"><span data-stu-id="bd249-134">Write-off</span></span>   | <span data-ttu-id="bd249-135">日常</span><span class="sxs-lookup"><span data-stu-id="bd249-135">Daily</span></span>            |
| <span data-ttu-id="bd249-136">资金不足</span><span class="sxs-lookup"><span data-stu-id="bd249-136">NSF</span></span>         | <span data-ttu-id="bd249-137">客户 - 付款</span><span class="sxs-lookup"><span data-stu-id="bd249-137">Customer payment</span></span> |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a><span data-ttu-id="bd249-138">设置冲销交易记录的原因代码</span><span class="sxs-lookup"><span data-stu-id="bd249-138">Set up a reason code for writeoff transactions</span></span>
<span data-ttu-id="bd249-139">在**“收款”**页上设置在勾销交易记录时使用的默认值原因代码。</span><span class="sxs-lookup"><span data-stu-id="bd249-139">Set up the default reason code that is used when transactions are written off on the **Collections** page.</span></span> <span data-ttu-id="bd249-140">您可以在勾销流程中更改该代码。</span><span class="sxs-lookup"><span data-stu-id="bd249-140">You can change the code during the write-off process.</span></span>

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a><span data-ttu-id="bd249-141">设置电子邮件附件的文件夹和创建电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="bd249-141">Set up a folder for email attachments and create email templates</span></span>
<span data-ttu-id="bd249-142">如果您从**“收款”**页发送具有 Microsoft Excel 附件的电子邮件，您可以为这些消息创建可选电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="bd249-142">If you will send email messages from the **Collections** page that have Microsoft Excel attachments, you can create optional email templates for those messages.</span></span>

## <a name="set-up-accounts-receivable-parameters-for-collections"></a><span data-ttu-id="bd249-143">设置集合的应收账款参数。</span><span class="sxs-lookup"><span data-stu-id="bd249-143">Set up accounts receivable parameters for collections</span></span>
<span data-ttu-id="bd249-144">设置在**“收款”**选项卡上显示的应收账款参数。</span><span class="sxs-lookup"><span data-stu-id="bd249-144">Set up the accounts receivable parameters that appear on the **Collections** tab.</span></span>

## <a name="optional-set-up-collections-agents"></a><span data-ttu-id="bd249-145">可选：设置收款代理</span><span class="sxs-lookup"><span data-stu-id="bd249-145">Optional: Set up collections agents</span></span>
<span data-ttu-id="bd249-146">如果您的组织的多个人员执行收款工作，您可以设置收款代理。</span><span class="sxs-lookup"><span data-stu-id="bd249-146">If multiple people in your organization do collections work, you can set up collections agents.</span></span> <span data-ttu-id="bd249-147">收款代理是设置为**“用户关系”**页上的用户的工作人员。</span><span class="sxs-lookup"><span data-stu-id="bd249-147">A collections agent is a worker who is set up as a user on the **User relations** page.</span></span> <span data-ttu-id="bd249-148">您可以分配客户池（客户查询）到代收人员以帮助代理组织它们的工作。</span><span class="sxs-lookup"><span data-stu-id="bd249-148">You can assign customer pools (customer queries) to collections agents to help the agents organize their work.</span></span> <span data-ttu-id="bd249-149">收款代理添加到**“应收账款参数”**页上选择的团队。</span><span class="sxs-lookup"><span data-stu-id="bd249-149">The collections agents are added to the team that is selected on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="bd249-150">如果在此窗体中未选择团队，则会自动创建名为**“收款”**的新团队，并且收款代理添加到该团队。</span><span class="sxs-lookup"><span data-stu-id="bd249-150">If a team isn't selected on that page, a new team that is named **Collections** is automatically created, and the collections agents are added to that team.</span></span>

## <a name="set-up-a-writeoff-account"></a><span data-ttu-id="bd249-151">设置冲销帐户</span><span class="sxs-lookup"><span data-stu-id="bd249-151">Set up a writeoff account</span></span>
<span data-ttu-id="bd249-152">交易记录已注销时，设置用于总帐冲销条目的销帐帐户。</span><span class="sxs-lookup"><span data-stu-id="bd249-152">Set up the write-off account that is used for the general ledger write-off entry when a transaction is written off.</span></span> <span data-ttu-id="bd249-153">此帐户存储在客户过帐模板中。</span><span class="sxs-lookup"><span data-stu-id="bd249-153">This account is stored on the customer posting profile.</span></span>

## <a name="set-up-nsf-information-for-bank-accounts"></a><span data-ttu-id="bd249-154">为银行帐户设置资金不足信息</span><span class="sxs-lookup"><span data-stu-id="bd249-154">Set up NSF information for bank accounts</span></span>
<span data-ttu-id="bd249-155">更新银行帐户，以便当在**“收款”**页上标识 NSF 支付时，这些帐户具有正确的日记帐。</span><span class="sxs-lookup"><span data-stu-id="bd249-155">Update bank accounts so that they have the correct journal when NSF payments are identified on the **Collections** page.</span></span> <span data-ttu-id="bd249-156">在**“币种管理”**选项卡上，在**“NSF 支付日记帐”**字段中，选择一个支付日记帐。</span><span class="sxs-lookup"><span data-stu-id="bd249-156">On the **Currency management** tab,  in the **NSF payment journal** field, select a payment journal.</span></span>

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a><span data-ttu-id="bd249-157">为“收款”页的用户设置 Outlook 设置</span><span class="sxs-lookup"><span data-stu-id="bd249-157">Set up Outlook settings for users of the Collections page</span></span>
<span data-ttu-id="bd249-158">在工作人员可以通过使用**“收款”**页创建活动或发送电子邮件消息前，您必须验证选择了**“Microsoft Outlook 同步”**配置键，并且为这些工作人员设置了 Outlook 同步。</span><span class="sxs-lookup"><span data-stu-id="bd249-158">Before workers can create activities or send email messages by using the **Collections** page, you must verify that the **Microsoft Outlook synchronization** configuration key is selected, and that Outlook synchronization is set up for those workers.</span></span>

## <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a><span data-ttu-id="bd249-159">设置收款客户联系人的电子邮件和地址设置</span><span class="sxs-lookup"><span data-stu-id="bd249-159">Set up email and address settings for collections customer contacts</span></span>
<span data-ttu-id="bd249-160">如果要将电子邮件发送给来自**“收款”**页的那些联系人，设置客户联系人的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="bd249-160">Set up email addresses for customer contacts if you want to send email messages to those contacts from the **Collections** page.</span></span> <span data-ttu-id="bd249-161">收款联系人用作**“收款”**页上的默认联系人。</span><span class="sxs-lookup"><span data-stu-id="bd249-161">The collections contact is used as the default contact on the **Collections** page.</span></span> <span data-ttu-id="bd249-162">如果报表应该使用主要地址以外的地址，您可以设置客户的报表地址。</span><span class="sxs-lookup"><span data-stu-id="bd249-162">You can set up a statement address for a customer if statements should use an address other than the primary address.</span></span> 

<span data-ttu-id="bd249-163">在客户的**“信用和收款”**快速选项卡上，在**“收款联系人”**字段中，选择客户组织中与您的收款代理合作的人员。</span><span class="sxs-lookup"><span data-stu-id="bd249-163">On the **Credit and Collections** FastTab for a customer, in the **Collections contact** field, select the person in the customer organization who works with your collections agent.</span></span> <span data-ttu-id="bd249-164">此人用作**“收款”**页上的默认联系人，并且是电子邮件发送到的人员。</span><span class="sxs-lookup"><span data-stu-id="bd249-164">This person is used as the default contact on the **Collections** page, and email messages are sent to him or her.</span></span> 

> [!NOTE] 
> <span data-ttu-id="bd249-165">如果没有为客户指定收款联系人，使用客户的主要联系人。</span><span class="sxs-lookup"><span data-stu-id="bd249-165">If a collections contact isn't specified for a customer, the primary contact for the customer is used.</span></span> <span data-ttu-id="bd249-166">如果未指定主要联系人，电子邮件将发送到**“联系人”**页上中列出的第一个地址。</span><span class="sxs-lookup"><span data-stu-id="bd249-166">If a primary contact isn't specified, email messages are sent to the first address that is listed on the **Contacts** page.</span></span>

## <a name="set-up-email-settings-for-salespeople"></a><span data-ttu-id="bd249-167">设置销售人员的电子邮件设置</span><span class="sxs-lookup"><span data-stu-id="bd249-167">Set up email settings for salespeople</span></span>
<span data-ttu-id="bd249-168">如果要将电子邮件发送给来自**“收款”**页的销售人员，为销售人员设置电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="bd249-168">Set up email addresses for salespeople if you want to send email messages to salespeople from the **Collections** page.</span></span> <span data-ttu-id="bd249-169">为每个佣金销售组中的每个销售代表设置电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="bd249-169">Set up an email address for each sales representative in each commission sales group.</span></span> <span data-ttu-id="bd249-170">其**“联系人”**选项被选中的销售代表是电子邮件发送到的默认销售人员。</span><span class="sxs-lookup"><span data-stu-id="bd249-170">The sales representative who has the **Contact** option selected is the default salesperson that email messages are sent to.</span></span> 

<span data-ttu-id="bd249-171">如果未指定销售代表，使用客户组织的主要销售人员。</span><span class="sxs-lookup"><span data-stu-id="bd249-171">If a sales representative isn't specified, the primary salesperson for the customer organization is used.</span></span> <span data-ttu-id="bd249-172">如果未指定主要销售人员，电子邮件将发送到此页上列出的第一个销售人员。</span><span class="sxs-lookup"><span data-stu-id="bd249-172">If a primary salesperson isn't specified, email messages are sent to the first salesperson who is listed on the page.</span></span>


<span data-ttu-id="bd249-173">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="bd249-173">For more information, see the following topics:</span></span>

 - [<span data-ttu-id="bd249-174">创建催款单序列</span><span class="sxs-lookup"><span data-stu-id="bd249-174">Create a collection letter sequence</span></span>](tasks/create-collection-letter-sequence.md)

 - [<span data-ttu-id="bd249-175">处理催款单</span><span class="sxs-lookup"><span data-stu-id="bd249-175">Process collection letters</span></span>](tasks/process-collection-letters.md)

 - [<span data-ttu-id="bd249-176">审核收款信息</span><span class="sxs-lookup"><span data-stu-id="bd249-176">Review collections information</span></span>](tasks/review-collections-information.md)


