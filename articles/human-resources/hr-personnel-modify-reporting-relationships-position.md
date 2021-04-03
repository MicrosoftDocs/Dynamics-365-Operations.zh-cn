---
title: 修改职位的报告关系
description: 该过程展示如何更改员工的报告关系。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd884362393674a4f55ea0410548edbb72786fff
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465382"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="ea01e-103">修改职位的报告关系</span><span class="sxs-lookup"><span data-stu-id="ea01e-103">Modify reporting relationships for a position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="ea01e-104">该过程展示如何更改员工的报告关系。</span><span class="sxs-lookup"><span data-stu-id="ea01e-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="ea01e-105">该报告关系可以通过工作流用于路线选择文件。</span><span class="sxs-lookup"><span data-stu-id="ea01e-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="ea01e-106">该过程同时也说明了如何分配给该员工附加的层次结构。</span><span class="sxs-lookup"><span data-stu-id="ea01e-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="ea01e-107">例如，一个员工作为某项目组的成员，与项目主管是非正式报告关系。</span><span class="sxs-lookup"><span data-stu-id="ea01e-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="ea01e-108">通过职位定义附加的报告关系可以用于调节各种项目或者矩阵方案。</span><span class="sxs-lookup"><span data-stu-id="ea01e-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="ea01e-109">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="ea01e-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="ea01e-110">转到“人力资源”>“职位”>“职位”。</span><span class="sxs-lookup"><span data-stu-id="ea01e-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="ea01e-111">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="ea01e-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ea01e-112">例如，在“职位”字段中用值“000091”进行筛选。</span><span class="sxs-lookup"><span data-stu-id="ea01e-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="ea01e-113">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ea01e-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ea01e-114">展开“职位报告”部分。</span><span class="sxs-lookup"><span data-stu-id="ea01e-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="ea01e-115">单击“新建”，以打开对话框。</span><span class="sxs-lookup"><span data-stu-id="ea01e-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="ea01e-116">在“报告”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea01e-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="ea01e-117">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="ea01e-117">Click Create.</span></span>
8. <span data-ttu-id="ea01e-118">展开“关系”部分。</span><span class="sxs-lookup"><span data-stu-id="ea01e-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="ea01e-119">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ea01e-119">Click Add.</span></span>
10. <span data-ttu-id="ea01e-120">选择表格左侧的复选框。</span><span class="sxs-lookup"><span data-stu-id="ea01e-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="ea01e-121">在“层次结构名称”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea01e-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="ea01e-122">示例：项目</span><span class="sxs-lookup"><span data-stu-id="ea01e-122">Example: Project</span></span>  
12. <span data-ttu-id="ea01e-123">在“直接上级职位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea01e-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="ea01e-124">示例：000437</span><span class="sxs-lookup"><span data-stu-id="ea01e-124">Example:  000437</span></span>
13. <span data-ttu-id="ea01e-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ea01e-125">Click Save.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]