---
title: 针对每个公司配置福利管理参数
description: 在 Microsoft Dynamics 365 Human Resources 中针对每个公司配置福利管理的参数。
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "4984592"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="ef508-103">针对每个公司配置福利管理参数</span><span class="sxs-lookup"><span data-stu-id="ef508-103">Configure Benefits management parameters per company</span></span>

<span data-ttu-id="ef508-104">对于每个提供福利的组织，您必须配置福利确认电子邮件的设置。</span><span class="sxs-lookup"><span data-stu-id="ef508-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="ef508-105">配置确认电子邮件设置</span><span class="sxs-lookup"><span data-stu-id="ef508-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="ef508-106">在 **福利管理** 工作区中，在 **设置** 下，选择 **人力资源参数**。</span><span class="sxs-lookup"><span data-stu-id="ef508-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="ef508-107">在 **福利管理** 选项卡上，为以下字段指定值：</span><span class="sxs-lookup"><span data-stu-id="ef508-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="ef508-108">字段</span><span class="sxs-lookup"><span data-stu-id="ef508-108">Field</span></span> | <span data-ttu-id="ef508-109">说明</span><span class="sxs-lookup"><span data-stu-id="ef508-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ef508-110">**发送确认电子邮件**</span><span class="sxs-lookup"><span data-stu-id="ef508-110">**Send confirmation email**</span></span> | <span data-ttu-id="ef508-111">打开此功能后，当员工从员工自助服务中的福利登记体验中签出时，将向他们发送确认电子邮件。</span><span class="sxs-lookup"><span data-stu-id="ef508-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="ef508-112">**确认电子邮件模板**</span><span class="sxs-lookup"><span data-stu-id="ef508-112">**Confirmation email template**</span></span> | <span data-ttu-id="ef508-113">选择发送登记确认时要使用的组织电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="ef508-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="ef508-114">如果您不选择模板，将发送以下通用电子邮件：</span><span class="sxs-lookup"><span data-stu-id="ef508-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="ef508-115">%EmployeeFirstName%，</span><span class="sxs-lookup"><span data-stu-id="ef508-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="ef508-116">恭喜!</span><span class="sxs-lookup"><span data-stu-id="ef508-116">Congratulations!</span></span> <span data-ttu-id="ef508-117">您已成功完成福利登记。</span><span class="sxs-lookup"><span data-stu-id="ef508-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="ef508-118">谢谢，</span><span class="sxs-lookup"><span data-stu-id="ef508-118">Thank you,</span></span><br><span data-ttu-id="ef508-119"><Company/Org name> 福利。</span><span class="sxs-lookup"><span data-stu-id="ef508-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="ef508-120">**默认电子邮件发件人地址**</span><span class="sxs-lookup"><span data-stu-id="ef508-120">**Default email sender address**</span></span> | <span data-ttu-id="ef508-121">发送确认电子邮件时要使用的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="ef508-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="ef508-122">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="ef508-122">Select **Save**.</span></span>