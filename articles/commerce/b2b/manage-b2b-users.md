---
title: 在 B2B 电子商务网站上管理业务合作伙伴用户
description: 本主题介绍管理员如何在企业到企业 (B2B) 电子商务网站上添加、编辑和删除业务合作伙伴用户。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7c1bd8d9cb494cef78fa7c14f6c391821d48749a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799845"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a><span data-ttu-id="281e4-103">在 B2B 电子商务网站上管理业务合作伙伴用户</span><span class="sxs-lookup"><span data-stu-id="281e4-103">Manage business partner users on B2B e-commerce websites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="281e4-104">本主题介绍管理员如何在企业到企业 (B2B) 电子商务网站上添加、编辑和删除业务合作伙伴用户。</span><span class="sxs-lookup"><span data-stu-id="281e4-104">This topic describes how administrators can add, edit, and delete business partner users on business-to-business (B2B) e-commerce websites.</span></span>

<span data-ttu-id="281e4-105">B2B 电子商务网站需要组织进行注册才能成为业务合作伙伴。</span><span class="sxs-lookup"><span data-stu-id="281e4-105">B2B e-commerce websites require that organizations register to become business partners.</span></span> <span data-ttu-id="281e4-106">组织将注册详细信息提交到 B2B 电子商务网站后，将通过资格认证流程。</span><span class="sxs-lookup"><span data-stu-id="281e4-106">After an organization submits registration details to a B2B e-commerce website, it goes through a qualification process.</span></span> <span data-ttu-id="281e4-107">如果组织成功取得资格，将作为业务合作伙伴加入。</span><span class="sxs-lookup"><span data-stu-id="281e4-107">If the organization is successfully qualified, it's onboarded as a business partner.</span></span>

<span data-ttu-id="281e4-108">组织作为业务合作伙伴加入后，发起请求成为业务合作伙伴的组织用户将被识别为管理员用户，并被授予将其他授权用户加入该 B2B 电子商务网站的特权。</span><span class="sxs-lookup"><span data-stu-id="281e4-108">After an organization is onboarded as a business partner, the organization user who initiated the request to become a business partner is identified as the administrator user and is granted privileges to onboard additional authorized users of the B2B e-commerce website.</span></span> <span data-ttu-id="281e4-109">这些授权用户然后可以代表业务合作伙伴下订单。</span><span class="sxs-lookup"><span data-stu-id="281e4-109">These authorized users can then place orders on behalf of the business partner.</span></span>

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a><span data-ttu-id="281e4-110">在 Commerce headquarters 中启用 B2B 电子商务功能</span><span class="sxs-lookup"><span data-stu-id="281e4-110">Turn on the B2B e-commerce capabilities feature in Commerce headquarters</span></span>

<span data-ttu-id="281e4-111">Commerce headquarters 中的 B2B 电子商务功能让组织可以加入业务合作伙伴和定义管理员用户。</span><span class="sxs-lookup"><span data-stu-id="281e4-111">The B2B e-commerce capabilities feature in Commerce headquarters enables organizations to onboard business partners and define administrator users.</span></span> <span data-ttu-id="281e4-112">此功能还让管理员能够创建和管理业务合作伙伴用户和团队，并为其分配特定角色。</span><span class="sxs-lookup"><span data-stu-id="281e4-112">This feature also enables administrators to create and manage business partner users and teams, and to assign specific roles to them.</span></span> <span data-ttu-id="281e4-113">最后，它让业务合作伙伴用户可以创建订单模板，然后使用现有订单重新订购产品。</span><span class="sxs-lookup"><span data-stu-id="281e4-113">Finally, it enables business partner users to create order templates and use existing orders to reorder products.</span></span>

<span data-ttu-id="281e4-114">要在 Commerce headquarters 中启用 B2B 电子商务功能，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="281e4-114">To turn on the B2B e-commerce capabilities feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="281e4-115">转到 **工作区 \> 功能管理**。</span><span class="sxs-lookup"><span data-stu-id="281e4-115">Go to **Workspaces \> Feature Management**.</span></span>
1. <span data-ttu-id="281e4-116">在 **所有** 选项卡上，使用术语 **零售和商业** 对 **模块** 字段进行筛选。</span><span class="sxs-lookup"><span data-stu-id="281e4-116">On the **All** tab, filter on the **Module** field by using the term **Retail and commerce**.</span></span>
1. <span data-ttu-id="281e4-117">查找并选择名为 **启用 B2B 电子商务功能** 的功能，然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="281e4-117">Find and select the feature that is named **Enable the use of B2B eCommerce capabilities**, and then select **Enable now**.</span></span>

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a><span data-ttu-id="281e4-118">创建编号规则并将其添加到 Commerce 共享参数</span><span class="sxs-lookup"><span data-stu-id="281e4-118">Create a number sequence and add it to Commerce shared parameters</span></span>

<span data-ttu-id="281e4-119">编号规则用于为需要标识符的主数据记录和交易记录生成可读的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="281e4-119">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="281e4-120">有关编号规则的详细信息，请参阅[编号规则概览](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview)。</span><span class="sxs-lookup"><span data-stu-id="281e4-120">For more information about number sequences, see [Number sequences overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).</span></span>

<span data-ttu-id="281e4-121">若要创建编号规则并将其添加到 Commerce headquarters 中的 Commerce 共享参数，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="281e4-121">To create a number sequence and add it to Commerce shared parameters in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="281e4-122">转到 **Retail 和 Commerce \> Headquarters 设置 \> 编号规则 \> 编号规则**，创建一个编号规则。</span><span class="sxs-lookup"><span data-stu-id="281e4-122">Go to **Retail and Commerce \> Headquarters setup \> Number sequences \> Number sequences**, and create a number sequence.</span></span>
1. <span data-ttu-id="281e4-123">转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 共享参数**，将新编号规则添加到 **客户层次结构 ID** 引用中。</span><span class="sxs-lookup"><span data-stu-id="281e4-123">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce shared parameters**, and add the new number sequence to the **Customer hierarchy ID** reference.</span></span>

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a><span data-ttu-id="281e4-124">为新业务合作伙伴设置管理员用户</span><span class="sxs-lookup"><span data-stu-id="281e4-124">Set up the administrator user for a new business partner</span></span>

<span data-ttu-id="281e4-125">潜在的业务合作伙伴可以通过站点上的链接提交加入请求，来启动 B2B 电子商务网站的加入流程。</span><span class="sxs-lookup"><span data-stu-id="281e4-125">Potential business partners can initiate the onboarding process to a B2B e-commerce website by submitting an onboarding request via a link on the site.</span></span> <span data-ttu-id="281e4-126">潜在的业务合作伙伴用户选择链接后，可以提供加入和注册所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="281e4-126">After a potential business partner user selects the link, they can provide the details that are required for onboarding and sign-up.</span></span> <span data-ttu-id="281e4-127">提交请求后，将显示一个提交确认页面。</span><span class="sxs-lookup"><span data-stu-id="281e4-127">After the request is submitted, a submission confirmation page appears.</span></span> <span data-ttu-id="281e4-128">如果提交被批准，请求者（即发起加入请求的用户）将成为业务合作伙伴管理员用户。</span><span class="sxs-lookup"><span data-stu-id="281e4-128">If the submission is approved, the requestor (that is, the user who initiated the onboarding request) becomes the business partner administrator user.</span></span>

<span data-ttu-id="281e4-129">要在 Commerce headquarters 中审核和设置业务合作伙伴管理员用户，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="281e4-129">To approve and set up a business partner administrator user in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="281e4-130">转到 **Retail 和 Commerce IT \> 配送计划**。</span><span class="sxs-lookup"><span data-stu-id="281e4-130">Go to **Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="281e4-131">运行 **P-0001** 作业，将所有业务合作伙伴的加入请求拉入 Commerce headquarters。</span><span class="sxs-lookup"><span data-stu-id="281e4-131">Run the **P-0001** job to pull all business partner onboarding requests into Commerce headquarters.</span></span>
1. <span data-ttu-id="281e4-132">**P-0001** 作业成功运行后，转到 **Retail 和 Commerce IT \> 客户**，运行 **从异步模式同步客户和业务合作伙伴** 作业。</span><span class="sxs-lookup"><span data-stu-id="281e4-132">After the **P-0001** job has successfully run, go to **Retail and Commerce IT \> Customer**, and run the **Synchronize customers and business partners from async mode** job.</span></span> <span data-ttu-id="281e4-133">此作业成功运行后，加入请求将作为 Commerce headquarters 中的目标客户记录创建。</span><span class="sxs-lookup"><span data-stu-id="281e4-133">After this job has successfully run, the onboarding requests are created as prospects records in Commerce headquarters.</span></span> <span data-ttu-id="281e4-134">这些记录的 **类型 ID** 字段将设置为 **B2B 目标客户**。</span><span class="sxs-lookup"><span data-stu-id="281e4-134">The **Type ID** field of these records is set to **B2B prospect**.</span></span>
1. <span data-ttu-id="281e4-135">转到 **客户 \> 所有目标客户**，打开目标客户页面。</span><span class="sxs-lookup"><span data-stu-id="281e4-135">Go to **Customers \> All prospects**, and open the prospects page.</span></span>
1. <span data-ttu-id="281e4-136">选择新业务合作伙伴的目标客户记录打开目标客户详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="281e4-136">Select the prospect record for the new business partner to open the prospect details page.</span></span>
1. <span data-ttu-id="281e4-137">在 **常规** 选项卡上，选择 **转换 \> 批准/拒绝** 批准或拒绝加入请求。</span><span class="sxs-lookup"><span data-stu-id="281e4-137">On the **General** tab, select **Convert \> Approve/Reject** to approve or reject the onboarding request.</span></span> <span data-ttu-id="281e4-138">当出现确认消息时，请确认您要继续流程，然后批准请求。</span><span class="sxs-lookup"><span data-stu-id="281e4-138">When a confirmation message appears, confirm that you want to continue with the process, and approve the request.</span></span> <span data-ttu-id="281e4-139">然后，一封电子邮件将发送到请求者的电子邮件地址，确认其组织已被批准为业务合作伙伴。</span><span class="sxs-lookup"><span data-stu-id="281e4-139">An email is then sent to the requestor's email address to confirm that their organization has been approved as a business partner.</span></span>

    <span data-ttu-id="281e4-140">批准请求后，目标客户记录的 **状态** 字段将设置为 **已审批**。</span><span class="sxs-lookup"><span data-stu-id="281e4-140">After you approve the request, the **Status** field of the prospect record is set to **Approved**.</span></span> <span data-ttu-id="281e4-141">此外，系统中还创建了两个新的客户记录：业务合作伙伴组织的 **组织类型** 客户记录和请求者的 **个人类型** 客户记录。</span><span class="sxs-lookup"><span data-stu-id="281e4-141">Additionally, two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor.</span></span> <span data-ttu-id="281e4-142">还将为业务合作伙伴创建客户层次结构记录。</span><span class="sxs-lookup"><span data-stu-id="281e4-142">A customer hierarchy record for the business partner is also created.</span></span> <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. <span data-ttu-id="281e4-143">转到 **Retail 和 Commerce IT \> 配送计划**，运行 **1010**（**客户**）作业将新创建的客户和客户层次结构记录推送到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="281e4-143">Go to **Retail and Commerce IT \> Distribution schedule**, and run the **1010** (**Customers**) job to push the newly created customer and customer hierarchy records to the channel database.</span></span>

<span data-ttu-id="281e4-144">批准请求并将客户和客户层次结构记录同步到渠道数据库后，请求者可以使用他们在提交请求时提供的电子邮件地址登录 B2B 电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="281e4-144">After the request is approved, and the customer and customer hierarchy records are synced to the channel database, the requestor can sign in to the B2B e-commerce website by using the email address that they provided when they submitted the request.</span></span> <span data-ttu-id="281e4-145">用户可以使用注册流来定义其帐户的密码。</span><span class="sxs-lookup"><span data-stu-id="281e4-145">Users can use the sign-up flow to define the password for their account.</span></span>

## <a name="onboard-additional-business-partner-users"></a><span data-ttu-id="281e4-146">加入其他业务合作伙伴用户</span><span class="sxs-lookup"><span data-stu-id="281e4-146">Onboard additional business partner users</span></span>

<span data-ttu-id="281e4-147">业务合作伙伴管理员用户可以根据需要将其他业务合作伙伴用户加入 B2B 电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="281e4-147">The business partner administrator user can onboard additional business partner users to the B2B e-commerce website as required.</span></span>

<span data-ttu-id="281e4-148">要将其他业务合作伙伴用户加入 B2B 电子商务网站，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="281e4-148">To onboard additional business partner users to a B2B e-commerce website, follow these steps.</span></span>

1. <span data-ttu-id="281e4-149">以管理员身份登录 B2B 电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="281e4-149">Sign in to the B2B e-commerce website as an administrator.</span></span>
1. <span data-ttu-id="281e4-150">转到 **我的帐户 \> 组织用户 \> 查看详细信息**，选择 **添加用户**。</span><span class="sxs-lookup"><span data-stu-id="281e4-150">Go to **My Account \> Organization users \> View details**, and select **Add a user**.</span></span>
1. <span data-ttu-id="281e4-151">输入所需信息，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="281e4-151">Enter the required information, and then select **Save**.</span></span> <span data-ttu-id="281e4-152">新用户的状态将设置为 **待处理**。</span><span class="sxs-lookup"><span data-stu-id="281e4-152">The status of the new user is set to **Pending**.</span></span>

    <span data-ttu-id="281e4-153">**P-0001** 和 **从异步模式同步客户和业务合作伙伴** 作业运行后，将在 Commerce headquarters 中为新用户创建 **个人类型** 客户记录。</span><span class="sxs-lookup"><span data-stu-id="281e4-153">After the **P-0001** and **Synchronize customers and business partners from async mode** jobs are run, a **Type Person** customer record for the new user is created in Commerce headquarters.</span></span> <span data-ttu-id="281e4-154">此客户记录还将与相关业务合作伙伴的客户层次结构记录关联。</span><span class="sxs-lookup"><span data-stu-id="281e4-154">This customer record is also associated with the relevant business partner's customer hierarchy record.</span></span> <span data-ttu-id="281e4-155">此外，还会向新用户的电子邮件地址发送一封电子邮件，通知他们已将其添加为业务合作伙伴组织的用户，他们现在可以登录 B2B 电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="281e4-155">Additionally, an email is sent to the new user's email address to notify them that they have been added as a user of the business partner organization and can now sign in to the B2B e-commerce website.</span></span>

1. <span data-ttu-id="281e4-156">运行 **1010**（**客户**）作业将新的业务合作伙伴用户同步到渠道数据库。</span><span class="sxs-lookup"><span data-stu-id="281e4-156">Run the **1010** (**Customers**) job to sync the new business partner user to the channel database.</span></span>

<span data-ttu-id="281e4-157">同步客户记录后，B2B 电子商务网站上的用户状态将设置为 **活动**，新用户可以使用其电子邮件地址登录 B2B 电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="281e4-157">After the customer record is synced, the status of the user on the B2B e-commerce website is set to **Active**, and the new user can sign in to the B2B e-commerce website by using their email address.</span></span> <span data-ttu-id="281e4-158">用户可以使用注册流来定义其帐户的密码。</span><span class="sxs-lookup"><span data-stu-id="281e4-158">Users can use the sign-up flow to define the password for their account.</span></span>

## <a name="edit-business-partner-user-details"></a><span data-ttu-id="281e4-159">编辑业务合作伙伴用户详细信息</span><span class="sxs-lookup"><span data-stu-id="281e4-159">Edit business partner user details</span></span>

<span data-ttu-id="281e4-160">要编辑业务合作伙伴用户的详细信息，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="281e4-160">To edit the details of business partner users, follow these steps.</span></span>

1. <span data-ttu-id="281e4-161">以管理员身份登录 B2B 电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="281e4-161">Sign in to the B2B e-commerce website as an administrator.</span></span>
1. <span data-ttu-id="281e4-162">转到 **我的帐户 \> 组织用户 \> 查看详细信息**，选择 **编辑** 按钮（铅笔符号），进行所需的更改，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="281e4-162">Go to **My Account \> Organization users \> View details**, select the **Edit** button (pencil symbol), make the required changes, and then select **Save**.</span></span> <span data-ttu-id="281e4-163">更改只有在 **P-0001**、**从异步模式同步客户和业务合作伙伴** 和 **1010**（**客户**）作业运行后才会生效。</span><span class="sxs-lookup"><span data-stu-id="281e4-163">The changes take effect only after the **P-0001**, **Synchronize customers and business partners from async mode**, and **1010** (**Customers**) jobs have been run.</span></span>

## <a name="remove-a-business-partner-user"></a><span data-ttu-id="281e4-164">删除业务合作伙伴用户</span><span class="sxs-lookup"><span data-stu-id="281e4-164">Remove a business partner user</span></span>

<span data-ttu-id="281e4-165">根据需要，管理员可以从可以访问 B2B 电子商务网站的用户列表中删除业务合作伙伴组织的现有用户。</span><span class="sxs-lookup"><span data-stu-id="281e4-165">As required, an administrator can remove existing users of a business partner organization from the list of users who can access the B2B e-commerce website.</span></span>

<span data-ttu-id="281e4-166">要删除业务合作伙伴用户，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="281e4-166">To remove a business partner user, follow these steps.</span></span>

1. <span data-ttu-id="281e4-167">以管理员身份登录 B2B 电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="281e4-167">Sign in to the B2B e-commerce website as an administrator.</span></span>
1. <span data-ttu-id="281e4-168">转到 **我的帐户 \> 组织用户 \> 查看详细信息**，选择 **删除** 按钮（“X”符号）。</span><span class="sxs-lookup"><span data-stu-id="281e4-168">Go to **My Account \> Organization users \> View details**, and select the **Remove** button ("X" symbol).</span></span> <span data-ttu-id="281e4-169">当出现确认消息时，请确认您要删除该用户。</span><span class="sxs-lookup"><span data-stu-id="281e4-169">When a confirmation message appears, confirm that you want to remove the user.</span></span> <span data-ttu-id="281e4-170">更改只有在 **P-0001**、**从异步模式同步客户和业务合作伙伴** 和 **1010**（**客户**）作业运行后才会生效。</span><span class="sxs-lookup"><span data-stu-id="281e4-170">The change takes effect only after the **P-0001**, **Synchronize customers and business partners from async mode**, and **1010** (**Customers**) jobs have been run.</span></span>

> [!NOTE]
> <span data-ttu-id="281e4-171">当您从可以访问 B2B 电子商务网站的用户列表中删除用户时，对应的客户记录将从业务伙伴的客户层次结构记录中删除。</span><span class="sxs-lookup"><span data-stu-id="281e4-171">When you remove a user from the list of users who can access the B2B e-commerce website, the corresponding customer record is removed from the business partner's customer hierarchy record.</span></span> <span data-ttu-id="281e4-172">但是，客户记录本身不会从 Commerce headquarters 中删除。</span><span class="sxs-lookup"><span data-stu-id="281e4-172">However, the customer record itself isn't deleted from Commerce headquarters.</span></span>

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a><span data-ttu-id="281e4-173">在 Commerce headquarters 中加入业务合作伙伴和用户</span><span class="sxs-lookup"><span data-stu-id="281e4-173">Onboard business partner and users in Commerce headquarters</span></span>

<span data-ttu-id="281e4-174">管理员可以直接在 Commerce headquarters 中加入业务合作伙伴和用户。</span><span class="sxs-lookup"><span data-stu-id="281e4-174">Administrators can onboard business partners and users directly in Commerce headquarters.</span></span>

<span data-ttu-id="281e4-175">要在 Commerce headquarters 中加入业务合作伙伴和用户，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="281e4-175">To onboard business partners and users in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="281e4-176">为业务合作伙伴组织创建 **组织类型** 客户记录。</span><span class="sxs-lookup"><span data-stu-id="281e4-176">Create a **Type Organization** customer record for the business partner organization.</span></span>
1. <span data-ttu-id="281e4-177">为业务合作伙伴用户创建 **个人类型** 客户记录。</span><span class="sxs-lookup"><span data-stu-id="281e4-177">Create **Type Person** customer records for business partner users.</span></span> <span data-ttu-id="281e4-178">确保为每个客户指定了主要电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="281e4-178">Make sure that a primary email address is specified for every customer.</span></span>
1. <span data-ttu-id="281e4-179">对于必须指定为业务合作伙伴组织管理员用户的每个 **个人类型** 客户记录，在 **零售** 快速选项卡上，将 **B2B 管理员** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="281e4-179">For each **Type Person** customer record that must be designated as an administrator user of the business partner organization, on the **Retail** FastTab, set the **B2B administrator** option to **Yes**.</span></span>
1. <span data-ttu-id="281e4-180">创建客户层次结构 ID。</span><span class="sxs-lookup"><span data-stu-id="281e4-180">Create a customer hierarchy ID.</span></span> <span data-ttu-id="281e4-181">在 **名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="281e4-181">In the **Name** field, enter a name.</span></span>
1. <span data-ttu-id="281e4-182">在 **组织** 字段中，输入业务合作伙伴组织客户。</span><span class="sxs-lookup"><span data-stu-id="281e4-182">In the **Organization** field, enter the business partner organization customer.</span></span>
1. <span data-ttu-id="281e4-183">选择 **添加**，然后在 **名称** 字段中选择客户。</span><span class="sxs-lookup"><span data-stu-id="281e4-183">Select **Add**, and then select a customer in the **Name** field.</span></span>
1. <span data-ttu-id="281e4-184">重复此过程，将其他客户添加到层次结构中。</span><span class="sxs-lookup"><span data-stu-id="281e4-184">Repeat this process to add additional customers to the hierarchy.</span></span>

## <a name="additional-information"></a><span data-ttu-id="281e4-185">附加信息</span><span class="sxs-lookup"><span data-stu-id="281e4-185">Additional information</span></span>

- <span data-ttu-id="281e4-186">可以将本主题中提到的所有作业配置为以批格式按计划运行。</span><span class="sxs-lookup"><span data-stu-id="281e4-186">All the jobs that are mentioned in this topic can be configured to run on a schedule in a batch format.</span></span> <span data-ttu-id="281e4-187">业务合作伙伴应该会根据需要配置批处理作业。</span><span class="sxs-lookup"><span data-stu-id="281e4-187">The expectation is that business partners will configure batch jobs as required.</span></span>
- <span data-ttu-id="281e4-188">当前，只能将一个用户/客户记录指定为管理员用户，并且只能在 Commerce headquarters 中更改该角色。</span><span class="sxs-lookup"><span data-stu-id="281e4-188">Currently, only one user/customer record can be designated as an administrator user, and that role can be changed only in Commerce headquarters.</span></span> <span data-ttu-id="281e4-189">没有让业务合作伙伴从 B2B 电子商务网站指定多个管理员或更改管理员的自助服务功能支持。</span><span class="sxs-lookup"><span data-stu-id="281e4-189">There is no support for self-service capabilities that let business partners to designate multiple administrators or change administrators from B2B e-commerce websites.</span></span>
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- <span data-ttu-id="281e4-190">虽然可以为用户定义支出限制，但是尚未实现在订单输入过程中强制执行支出限制。</span><span class="sxs-lookup"><span data-stu-id="281e4-190">Although spending limits can be defined for users, enforcement of spending limits during the order entry process hasn't yet been implemented.</span></span>
- <span data-ttu-id="281e4-191">B2B 电子商务网站上用户体验的所有业务逻辑和验证均基于映射到 Commerce headquarters 中用户的客户记录的配置。</span><span class="sxs-lookup"><span data-stu-id="281e4-191">All business logic and validation for a user's experience on a B2B e-commerce website are based on the configuration of the customer record that is mapped to the user in Commerce headquarters.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="281e4-192">其他资源</span><span class="sxs-lookup"><span data-stu-id="281e4-192">Additional resources</span></span>

[<span data-ttu-id="281e4-193">建立 B2B 电子商务站点</span><span class="sxs-lookup"><span data-stu-id="281e4-193">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="281e4-194">为 B2B 组织创建组织建模层次结构</span><span class="sxs-lookup"><span data-stu-id="281e4-194">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="281e4-195">配置 B2B 电子商务站点的客户帐户付款方式</span><span class="sxs-lookup"><span data-stu-id="281e4-195">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="281e4-196">设置 B2B 电子商务站点的产品数量限制</span><span class="sxs-lookup"><span data-stu-id="281e4-196">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="281e4-197">编号规则概览</span><span class="sxs-lookup"><span data-stu-id="281e4-197">Number sequences overview</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]