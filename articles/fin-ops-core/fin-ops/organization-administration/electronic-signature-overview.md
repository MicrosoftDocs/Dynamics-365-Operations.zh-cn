---
title: 电子签名概览
description: 本文提供电子签名的概览并说明如何使用它们。
author: maertenm
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df7f842477ddfb88662f37ae311215f08c6b0173
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693176"
---
# <a name="electronic-signatures-overview"></a><span data-ttu-id="6585b-103">电子签名概览</span><span class="sxs-lookup"><span data-stu-id="6585b-103">Electronic signatures overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6585b-104">本文提供电子签名的概览并说明如何使用它们。</span><span class="sxs-lookup"><span data-stu-id="6585b-104">This article provides an overview of electronic signatures and describes how they can be used.</span></span>

## <a name="what-is-an-electronic-signature"></a><span data-ttu-id="6585b-105">什么是电子签名？</span><span class="sxs-lookup"><span data-stu-id="6585b-105">What is an electronic signature?</span></span>

<span data-ttu-id="6585b-106">电子签名确认要启动或审核计算流程的人员的身份。</span><span class="sxs-lookup"><span data-stu-id="6585b-106">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="6585b-107">在一些行业中，电子签名与手写签名在法律上具有相同效力。</span><span class="sxs-lookup"><span data-stu-id="6585b-107">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span>

<span data-ttu-id="6585b-108">电子签名是一些受管制行业（如制药业、食品和饮料业以及航空和国防）的法规遵从性要求。</span><span class="sxs-lookup"><span data-stu-id="6585b-108">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span> <span data-ttu-id="6585b-109">它们也是遵循 21 CFR 第 11 部分（由美国食品和药品管理局颁发）中的法规所必需的。</span><span class="sxs-lookup"><span data-stu-id="6585b-109">They are also required for compliance with regulations in 21 CFR Part 11 that was issued by the Food and Drug Administration (FDA) in the United States.</span></span>

> [!NOTE]
> <span data-ttu-id="6585b-110">电子签名本身与数字签名不同。</span><span class="sxs-lookup"><span data-stu-id="6585b-110">An electronic signature by itself isn't the same as a digital signature.</span></span> <span data-ttu-id="6585b-111">电子签名只是手写签名的替代品，而数字签名还提供其他安全措施。</span><span class="sxs-lookup"><span data-stu-id="6585b-111">An electronic signature is just a substitute for a handwritten signature, whereas a digital signature provides additional security measures.</span></span> <span data-ttu-id="6585b-112">数字签名可以帮助标识其他用户或进程是否篡改了数据。</span><span class="sxs-lookup"><span data-stu-id="6585b-112">A digital signature can help identify whether another user or process has tampered with the data.</span></span> <span data-ttu-id="6585b-113">还可以验证数字签名，并且用于对数据签名的证书所有者不能驳倒此验证。</span><span class="sxs-lookup"><span data-stu-id="6585b-113">A digital signature can also be verified, and this verification can't be refuted by the owner of the certificate that was used to sign the data.</span></span> <span data-ttu-id="6585b-114">如下所述，电子签名具有内置数字签名功能。</span><span class="sxs-lookup"><span data-stu-id="6585b-114">As described below, electronic signatures have built-in digital signature functionality.</span></span>

## <a name="electronic-signatures"></a><span data-ttu-id="6585b-115">电子签名</span><span class="sxs-lookup"><span data-stu-id="6585b-115">Electronic signatures</span></span>

<span data-ttu-id="6585b-116">可以对关键业务流程使用电子签名。</span><span class="sxs-lookup"><span data-stu-id="6585b-116">You can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="6585b-117">一些流程具有内置电子签名功能。</span><span class="sxs-lookup"><span data-stu-id="6585b-117">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="6585b-118">还可以为任意数据库表和字段创建自定义签名要求。</span><span class="sxs-lookup"><span data-stu-id="6585b-118">You can also create custom signature requirements for any database table and field.</span></span>

<span data-ttu-id="6585b-119">电子签名具有内置数字签名功能。</span><span class="sxs-lookup"><span data-stu-id="6585b-119">Electronic signatures have built-in digital signature functionality.</span></span> <span data-ttu-id="6585b-120">对文档签名的每个用户必须获取有效的加密证书。</span><span class="sxs-lookup"><span data-stu-id="6585b-120">Every user who signs documents must obtain a valid cryptographic certificate.</span></span> <span data-ttu-id="6585b-121">对文档签名时，与此证书相关的私钥进行验证。</span><span class="sxs-lookup"><span data-stu-id="6585b-121">When a document is signed, the private key that is associated with that certificate is validated.</span></span> <span data-ttu-id="6585b-122">电子签名信息记录在日志中以提供审计线索。</span><span class="sxs-lookup"><span data-stu-id="6585b-122">Electronic signature information is recorded in a log to provide an audit trail.</span></span> <span data-ttu-id="6585b-123">若要设置电子签名，请参阅[设置电子签名](tasks/set-up-electronic-signatures.md)。</span><span class="sxs-lookup"><span data-stu-id="6585b-123">To set up electronic signatures, see [Set up electronic signatures](tasks/set-up-electronic-signatures.md).</span></span>

## <a name="users-who-require-access-to-electronic-signatures"></a><span data-ttu-id="6585b-124">需要访问电子签名的用户</span><span class="sxs-lookup"><span data-stu-id="6585b-124">Users who require access to electronic signatures</span></span>

<span data-ttu-id="6585b-125">以下三类用户通常要求电子签名的安全访问权限：电子签名管理员、签名人和电子签名审计员。</span><span class="sxs-lookup"><span data-stu-id="6585b-125">Three kinds of users typically require security access to electronic signatures: electronic signature administrators, signers, and electronic signature auditors.</span></span>

### <a name="electronic-signature-administrator"></a><span data-ttu-id="6585b-126">电子签名管理员</span><span class="sxs-lookup"><span data-stu-id="6585b-126">Electronic signature administrator</span></span>

<span data-ttu-id="6585b-127">电子签名管理员设置签名要求、一般参数和审核人，并在无法验证签名时接收预警。</span><span class="sxs-lookup"><span data-stu-id="6585b-127">The electronic signature administrator sets up signature requirements, general parameters, and approvers, and receives alerts when signatures can't be verified.</span></span> <span data-ttu-id="6585b-128">默认情况下，属于 **信息技术经理** 安全角色的用户有权管理电子签名。</span><span class="sxs-lookup"><span data-stu-id="6585b-128">By default, a user who belongs to the **Information technology manager** security role has permission to administer electronic signatures.</span></span>

### <a name="signer"></a><span data-ttu-id="6585b-129">签名人</span><span class="sxs-lookup"><span data-stu-id="6585b-129">Signer</span></span>

<span data-ttu-id="6585b-130">签名人为需要签名的文档和流程提供电子签名。</span><span class="sxs-lookup"><span data-stu-id="6585b-130">A signer provides electronic signatures for documents and processes that require signatures.</span></span> <span data-ttu-id="6585b-131">默认情况下，属于 **系统用户** 安全角色的用户有权对文档进行电子签名。</span><span class="sxs-lookup"><span data-stu-id="6585b-131">By default, a user who belongs to the **System user** security role has permission to sign documents electronically.</span></span>

> [!NOTE]
> <span data-ttu-id="6585b-132">签名人可能需要其他权限才能被授权访问与将要签名的文档或流程有关的数据。</span><span class="sxs-lookup"><span data-stu-id="6585b-132">The signer might require additional permissions before access is granted to data that is related to the document or process that is being signed.</span></span> <span data-ttu-id="6585b-133">更改数据后必须为这些更改签名的用户必须具有更改数据的权限。</span><span class="sxs-lookup"><span data-stu-id="6585b-133">A user who changes data and must then sign for those changes must have permission to change the data.</span></span> <span data-ttu-id="6585b-134">代表其他用户签名的用户可能不需要访问数据。</span><span class="sxs-lookup"><span data-stu-id="6585b-134">A user who signs on behalf of another user might not require access to the data.</span></span> <span data-ttu-id="6585b-135">此类型的用户示例是为员工的更改签名的主管。</span><span class="sxs-lookup"><span data-stu-id="6585b-135">An example of this kind of user is a supervisor who signs for an employee's changes.</span></span>

### <a name="electronic-signature-auditor"></a><span data-ttu-id="6585b-136">电子签名审计员</span><span class="sxs-lookup"><span data-stu-id="6585b-136">Electronic signature auditor</span></span>

<span data-ttu-id="6585b-137">电子签名审计员查看数据库日志和可从数据库日志得到的查看签名日志。</span><span class="sxs-lookup"><span data-stu-id="6585b-137">The electronic signature auditor reviews the database log and the signature review log that is available from the database log.</span></span> <span data-ttu-id="6585b-138">默认情况下，属于 **信息技术经理** 安全角色的用户有权审核电子签名。</span><span class="sxs-lookup"><span data-stu-id="6585b-138">By default, a user who belongs to the **Information technology manager** security role has permission to audit electronic signatures.</span></span>

<span data-ttu-id="6585b-139">如果您使用一个角色，而不使用 **信息技术经理**，请确保为该角色分配以下特权：</span><span class="sxs-lookup"><span data-stu-id="6585b-139">If you use a role other than **Information technology manager**, make sure that the role is assigned the following privileges:</span></span>

- <span data-ttu-id="6585b-140">查看电子签名故障</span><span class="sxs-lookup"><span data-stu-id="6585b-140">View electronic signature failures</span></span>
- <span data-ttu-id="6585b-141">查看数据库日志</span><span class="sxs-lookup"><span data-stu-id="6585b-141">View database log</span></span>

## <a name="signing-documents-electronically"></a><span data-ttu-id="6585b-142">对文档进行电子签名</span><span class="sxs-lookup"><span data-stu-id="6585b-142">Signing documents electronically</span></span>

### <a name="get-a-certificate"></a><span data-ttu-id="6585b-143">获取证书</span><span class="sxs-lookup"><span data-stu-id="6585b-143">Get a certificate</span></span>

<span data-ttu-id="6585b-144">在对文档进行电子签名前，每个签名人必须申请证书。</span><span class="sxs-lookup"><span data-stu-id="6585b-144">Before you sign documents electronically, you must request a certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="6585b-145">Microsoft SQL Server 功能用于创建证书并启用电子签名。</span><span class="sxs-lookup"><span data-stu-id="6585b-145">Microsoft SQL Server features are used to create certificates and enable electronic signing.</span></span> <span data-ttu-id="6585b-146">不需要其他证书或公钥基础结构 (PKI)。</span><span class="sxs-lookup"><span data-stu-id="6585b-146">No additional certificate or public key infrastructure (PKI) is required.</span></span>

<span data-ttu-id="6585b-147">申请证书时，会为您创建一个公钥和一个私钥。</span><span class="sxs-lookup"><span data-stu-id="6585b-147">When you request a certificate, a public key and a private key are created for you.</span></span> <span data-ttu-id="6585b-148">私钥是通过使用只有您知道的密码进行加密。</span><span class="sxs-lookup"><span data-stu-id="6585b-148">The private key is encrypted by using a password that is known only to you.</span></span> <span data-ttu-id="6585b-149">当对文档进行电子签名时，通过输入密码来验证您的身份。</span><span class="sxs-lookup"><span data-stu-id="6585b-149">When you sign a document electronically, your identity is verified when you enter the password.</span></span>

<span data-ttu-id="6585b-150">要请求证书，在 **选项** 页，在 **帐户** 选项卡上，单击 **获取证书**。</span><span class="sxs-lookup"><span data-stu-id="6585b-150">To request a certificate, on the **Options** page, on the **Accounts** tab, click **Get certificate**.</span></span>

<span data-ttu-id="6585b-151">您必须输入并确认您将用于签名的密码。</span><span class="sxs-lookup"><span data-stu-id="6585b-151">You must enter and confirm the password that you will use for signing.</span></span> <span data-ttu-id="6585b-152">使用该密码来保护您的私钥并授权使用您的证书。</span><span class="sxs-lookup"><span data-stu-id="6585b-152">The password is used to protect your private key and authorize the use of your certificate.</span></span> <span data-ttu-id="6585b-153">该密码不存储在数据库中，对于任何其他人（甚至管理员）都不可用。</span><span class="sxs-lookup"><span data-stu-id="6585b-153">This password isn't stored in the database, and it isn't available to anyone else, not even to the administrator.</span></span>

<span data-ttu-id="6585b-154">如果您忘记与证书连接的密码，证书必须重置。</span><span class="sxs-lookup"><span data-stu-id="6585b-154">If you forget the password that is connected with your certificate, that certificate must be reset.</span></span> <span data-ttu-id="6585b-155">如果重置证书，您不会影响使用旧证书签名的文档。</span><span class="sxs-lookup"><span data-stu-id="6585b-155">If you reset the certificate, you don't affect documents that you signed by using the previous certificate.</span></span> <span data-ttu-id="6585b-156">若要重置证书，在 **选项** 页上，单击 **重置证书**。</span><span class="sxs-lookup"><span data-stu-id="6585b-156">To reset the certificate, on the **Options** page, click **Reset certificate**.</span></span>

### <a name="sign-a-document-electronically"></a><span data-ttu-id="6585b-157">对文档进行电子签名</span><span class="sxs-lookup"><span data-stu-id="6585b-157">Sign a document electronically</span></span>

<span data-ttu-id="6585b-158">执行需要电子签名的更改时，将显示 **对文档签名** 页。</span><span class="sxs-lookup"><span data-stu-id="6585b-158">The **Sign document** page is displayed when you make a change that requires an electronic signature.</span></span>

1. <span data-ttu-id="6585b-159">在 **对文档签名** 页，单击 **文档** 选项卡查看对文档的更改。</span><span class="sxs-lookup"><span data-stu-id="6585b-159">On the **Sign document** page, click the **Document** tab to review the changes to the document.</span></span>
2. <span data-ttu-id="6585b-160">在 **签名** 选项卡上，选择一个原因代码。</span><span class="sxs-lookup"><span data-stu-id="6585b-160">On the **Signature** tab, select a reason code.</span></span>
3. <span data-ttu-id="6585b-161">输入注释，如果注释是必需的。</span><span class="sxs-lookup"><span data-stu-id="6585b-161">Enter a comment, if a comment is required.</span></span>
4. <span data-ttu-id="6585b-162">如果您的用户 ID 未显示在 **签名人** 字段中，请在列表中选择它。</span><span class="sxs-lookup"><span data-stu-id="6585b-162">If your user ID doesn't appear in the **Signer** field, select it in the list.</span></span>
5. <span data-ttu-id="6585b-163">输入您所在的位置，如果此信息是必需的。</span><span class="sxs-lookup"><span data-stu-id="6585b-163">Enter your location, if this information is required.</span></span>
6. <span data-ttu-id="6585b-164">单击 **OK**。</span><span class="sxs-lookup"><span data-stu-id="6585b-164">Click **OK**.</span></span>

### <a name="sign-for-another-users-changes"></a><span data-ttu-id="6585b-165">为其他用户的更改签名</span><span class="sxs-lookup"><span data-stu-id="6585b-165">Sign for another user's changes</span></span>

<span data-ttu-id="6585b-166">有时您可能需要用户为其他用户的更改签名。</span><span class="sxs-lookup"><span data-stu-id="6585b-166">Occasionally, you might want a user to sign for another user's changes.</span></span> <span data-ttu-id="6585b-167">例如，可能要求主管为员工所做的物料清单 (BOM) 更改签名。</span><span class="sxs-lookup"><span data-stu-id="6585b-167">For example, a supervisor might be required to sign for changes that an employee makes to a bill of materials (BOM).</span></span> <span data-ttu-id="6585b-168">使用此过程可以将用户指定为其他用户的签名人。</span><span class="sxs-lookup"><span data-stu-id="6585b-168">Use this procedure to designate a user as a signer for another user.</span></span>

> [!NOTE]
> <span data-ttu-id="6585b-169">一个用户为其他用户的更改签名时，必须在执行更改的用户的工作站提供签名。</span><span class="sxs-lookup"><span data-stu-id="6585b-169">When one user signs for another user's change, the signature must be provided at the workstation of the user who made the change.</span></span> <span data-ttu-id="6585b-170">只有提供签名后，该用户才能保存更改。</span><span class="sxs-lookup"><span data-stu-id="6585b-170">The user can't save the change until the signature has been provided.</span></span>

<span data-ttu-id="6585b-171">若要指定审核人，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6585b-171">To designate approvers, follow these steps.</span></span>

1. <span data-ttu-id="6585b-172">在 **选项** 页，在 **帐户** 选项卡上，单击 **指定审核人**。</span><span class="sxs-lookup"><span data-stu-id="6585b-172">On the **Options** page, on the **Accounts** tab, click **Designate approver**.</span></span>
2. <span data-ttu-id="6585b-173">在 **审核人用户 ID** 字段中，选择必须为其他用户的更改签名的用户的 ID。</span><span class="sxs-lookup"><span data-stu-id="6585b-173">In the **Approver user ID** field, select the ID of the user who must sign for another user's changes.</span></span>
3. <span data-ttu-id="6585b-174">在 **为其签名的用户 ID** 字段中，选择必须为其更改签名的用户的 ID。</span><span class="sxs-lookup"><span data-stu-id="6585b-174">In the **Sign for user ID** field, select the ID of the user whose changes must be signed for.</span></span>
