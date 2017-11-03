---
title: "导入和维护信用卡交易记录"
description: "本主题说明如何导入和维护与费用相关的信用卡交易记录。 这些交易记录可以设置为对重复执行的计划自动导入或根据需要手动导入。"
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e640c9e44add5599be4a2e381b4ffd81f212889c
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="66932-104">导入和维护信用卡交易记录</span><span class="sxs-lookup"><span data-stu-id="66932-104">Import and maintain credit card transactions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="66932-105">与费用相关的信用卡交易记录可以设置为对重复执行的计划自动导入。</span><span class="sxs-lookup"><span data-stu-id="66932-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="66932-106">或者根据需要手动导入。</span><span class="sxs-lookup"><span data-stu-id="66932-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="66932-107">信用卡交易记录通过信用卡交易记录数据实体进行导入。</span><span class="sxs-lookup"><span data-stu-id="66932-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="66932-108">有关数据实体的详细信息，请参阅[数据实体](../../dev-itpro/data-entities/data-entities.md)。</span><span class="sxs-lookup"><span data-stu-id="66932-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="66932-109">导入信用卡交易记录</span><span class="sxs-lookup"><span data-stu-id="66932-109">Import credit card transactions</span></span>

1. <span data-ttu-id="66932-110">在**信用卡交易记录**页，选择**导入交易记录**。</span><span class="sxs-lookup"><span data-stu-id="66932-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="66932-111">如果您是首次打开数据管理，系统必须更新数据实体的列表后，您才可以继续。</span><span class="sxs-lookup"><span data-stu-id="66932-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="66932-112">在**名称**字段中，输入导入的作业的唯一描述。</span><span class="sxs-lookup"><span data-stu-id="66932-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="66932-113">在**源数据格式**字段中，选择包含要导入的信用卡交易记录的文件格式。</span><span class="sxs-lookup"><span data-stu-id="66932-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="66932-114">选择**上载**，然后查找并选择要导入的文件。</span><span class="sxs-lookup"><span data-stu-id="66932-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="66932-115">在上载文件后，通过选择磁贴上的**查看映射**链接验证信用卡交易记录文件与信用卡交易记录数据实体列的映射。</span><span class="sxs-lookup"><span data-stu-id="66932-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="66932-116">如果出现映射错误，或如果必须更改映射，则从**映射可视化**选项卡或**映射详细信息**选项卡更改映射。</span><span class="sxs-lookup"><span data-stu-id="66932-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="66932-117">若要自动执行信用卡交易记录，请选择**创建重复性数据作业**。</span><span class="sxs-lookup"><span data-stu-id="66932-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="66932-118">随后可以设置定义导入信用卡交易记录的频率的重复项。</span><span class="sxs-lookup"><span data-stu-id="66932-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="66932-119">当您完成时，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="66932-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="66932-120">若想要现在导入所选文件，选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="66932-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="66932-121">如果在导入期间出现错误，您可以查看执行日志或暂存数据以查看必须修复的错误，以帮助保证导入成功。</span><span class="sxs-lookup"><span data-stu-id="66932-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="66932-122">如果必须导入多个文件格式，则必须为每种格式类型创建单独的导入作业。</span><span class="sxs-lookup"><span data-stu-id="66932-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="66932-123">重新分配离职员工的信用卡交易记录</span><span class="sxs-lookup"><span data-stu-id="66932-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="66932-124">终止员工记录后，员工的 Active Directory 域服务 (AD DS) 帐户被禁用。</span><span class="sxs-lookup"><span data-stu-id="66932-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="66932-125">但是，可能还存在仍然必须支出和偿还的有效信用卡交易记录。</span><span class="sxs-lookup"><span data-stu-id="66932-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="66932-126">从**信用卡交易记录**页可以在相关员工已离职时为任何信用卡交易记录重新分配员工。</span><span class="sxs-lookup"><span data-stu-id="66932-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="66932-127">选择一个或多个信用卡交易记录，然后选择**重新分配交易记录**。</span><span class="sxs-lookup"><span data-stu-id="66932-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="66932-128">您可以随后选择要分配信用卡交易记录的其他员工。</span><span class="sxs-lookup"><span data-stu-id="66932-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="66932-129">重新分配信用卡交易记录后，可以为费用报表选择该交易记录，并通过费用报表报销的正常流程进行支付。</span><span class="sxs-lookup"><span data-stu-id="66932-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

