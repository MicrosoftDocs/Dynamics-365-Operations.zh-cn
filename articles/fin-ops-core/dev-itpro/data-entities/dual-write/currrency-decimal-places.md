---
title: 双写入货币数据类型迁移
description: 本主题介绍如何更改双写入支持的货币的小数位数。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 5d39bf28dba951a1483412d967c8c6fc6dbcc610
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744367"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="1a023-103">双写入货币数据类型迁移</span><span class="sxs-lookup"><span data-stu-id="1a023-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1a023-104">您最多可以将货币值支持的小数位数增加到 10。</span><span class="sxs-lookup"><span data-stu-id="1a023-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="1a023-105">默认限制是四个小数位。</span><span class="sxs-lookup"><span data-stu-id="1a023-105">The default limit is four decimal places.</span></span> <span data-ttu-id="1a023-106">通过增加小数位数，可以帮助您防止在使用双写入同步数据时丢失数据。</span><span class="sxs-lookup"><span data-stu-id="1a023-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="1a023-107">小数位数的增加是一种选择更改。</span><span class="sxs-lookup"><span data-stu-id="1a023-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="1a023-108">要实现它，您必须寻求 Microsoft 的帮助。</span><span class="sxs-lookup"><span data-stu-id="1a023-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="1a023-109">更改小数位数的流程分为两个步骤：</span><span class="sxs-lookup"><span data-stu-id="1a023-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="1a023-110">从 Microsoft 请求迁移。</span><span class="sxs-lookup"><span data-stu-id="1a023-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="1a023-111">在 Dataverse 中更改小数位数。</span><span class="sxs-lookup"><span data-stu-id="1a023-111">Change the number of decimal places in Dataverse.</span></span>

<span data-ttu-id="1a023-112">Finance and Operations 应用和 Dataverse 必须在货币值中支持相同数量的小数位数。</span><span class="sxs-lookup"><span data-stu-id="1a023-112">The Finance and Operations app and Dataverse must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="1a023-113">否则，在应用之间同步此信息时，可能会发生数据丢失。</span><span class="sxs-lookup"><span data-stu-id="1a023-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="1a023-114">迁移流程将重新配置货币和汇率值的存储方式，但不会更改任何数据。</span><span class="sxs-lookup"><span data-stu-id="1a023-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="1a023-115">迁移完成后，可以增加币种代码和定价的小数位数，用户输入和查看的数据可以具有更高的小数精度。</span><span class="sxs-lookup"><span data-stu-id="1a023-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="1a023-116">迁移是可选的。</span><span class="sxs-lookup"><span data-stu-id="1a023-116">Migration is optional.</span></span> <span data-ttu-id="1a023-117">如果支持更多小数位可能对您有好处，建议您考虑迁移。</span><span class="sxs-lookup"><span data-stu-id="1a023-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="1a023-118">不需要四位以上小数位的值的组织不必迁移。</span><span class="sxs-lookup"><span data-stu-id="1a023-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="1a023-119">从 Microsoft 请求迁移</span><span class="sxs-lookup"><span data-stu-id="1a023-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="1a023-120">Dataverse 中现有货币列的存储无法支持超过四个小数位。</span><span class="sxs-lookup"><span data-stu-id="1a023-120">Storage for existing currency columns in Dataverse can't support more than four decimal places.</span></span> <span data-ttu-id="1a023-121">因此，在迁移流程中，货币值将被复制到数据库中的新内部列。</span><span class="sxs-lookup"><span data-stu-id="1a023-121">Therefore, during the migration process, currency values are copied to new internal columns in the database.</span></span> <span data-ttu-id="1a023-122">此流程将持续进行，直到所有数据都已迁移。</span><span class="sxs-lookup"><span data-stu-id="1a023-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="1a023-123">在内部，在迁移结束时，新的存储类型将替换旧的存储类型，但是数据值不变。</span><span class="sxs-lookup"><span data-stu-id="1a023-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="1a023-124">然后，货币列最多可以支持 10 个小数位。</span><span class="sxs-lookup"><span data-stu-id="1a023-124">The currency columns can then support up to 10 decimal places.</span></span> <span data-ttu-id="1a023-125">在迁移流程中，Dataverse 可以继续使用而不会中断。</span><span class="sxs-lookup"><span data-stu-id="1a023-125">During the migration process, Dataverse can continue to be used without interruption.</span></span>

<span data-ttu-id="1a023-126">同时，汇率将修改，使其支持最多 12 个小数位，而不是当前的 10 个限制。</span><span class="sxs-lookup"><span data-stu-id="1a023-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="1a023-127">此更改是必需的，以使 Finance and Operations 应用和 Dataverse 中的小数位数相同。</span><span class="sxs-lookup"><span data-stu-id="1a023-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Dataverse.</span></span>

<span data-ttu-id="1a023-128">迁移不会更改任何数据。</span><span class="sxs-lookup"><span data-stu-id="1a023-128">Migration doesn't change any data.</span></span> <span data-ttu-id="1a023-129">货币和汇率列转换后，管理员可以通过指定每种交易货币和定价的小数位数来配置系统以最多为货币列使用 10 个小数位。</span><span class="sxs-lookup"><span data-stu-id="1a023-129">After the currency and exchange rate columns are converted, admins can configure the system to use up to 10 decimal places for currency columns by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="1a023-130">请求迁移</span><span class="sxs-lookup"><span data-stu-id="1a023-130">Request a migration</span></span>

<span data-ttu-id="1a023-131">要使此功能可用，请发送电子邮件到 **CDSExpandDecimal@microsoft.com**，并包含以下信息：</span><span class="sxs-lookup"><span data-stu-id="1a023-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="1a023-132">**主题：** 请求为 \<organizationID\> 启用扩展的十进制支持</span><span class="sxs-lookup"><span data-stu-id="1a023-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="1a023-133">**正文：** 我想要为我的组织 \<organizationID\> 启用扩展的十进制支持。</span><span class="sxs-lookup"><span data-stu-id="1a023-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="1a023-134">Microsoft 代表将在两到三个工作日内与您联系以完成后续步骤。</span><span class="sxs-lookup"><span data-stu-id="1a023-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="1a023-135">当您请求迁移时，您应该了解以下详细信息并相应地进行计划：</span><span class="sxs-lookup"><span data-stu-id="1a023-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="1a023-136">迁移数据所需的时间取决于系统中的数据量。</span><span class="sxs-lookup"><span data-stu-id="1a023-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="1a023-137">大型数据库的迁移可能需要几天时间。</span><span class="sxs-lookup"><span data-stu-id="1a023-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="1a023-138">在迁移运行时，数据库的大小会临时增加，因为索引需要更多空间。</span><span class="sxs-lookup"><span data-stu-id="1a023-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="1a023-139">迁移完成后，大多数增加的空间将被释放。</span><span class="sxs-lookup"><span data-stu-id="1a023-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="1a023-140">在迁移流程中，如果发生妨碍迁移完成的错误，系统会向 Microsoft 支持部门发出警报，以便支持人员可以进行干预。</span><span class="sxs-lookup"><span data-stu-id="1a023-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="1a023-141">但是，即使在迁移过程中发生错误，Dataverse 仍然可以正常使用。</span><span class="sxs-lookup"><span data-stu-id="1a023-141">However, even if errors occur during the migration, Dataverse remains fully available for regular use.</span></span>
+ <span data-ttu-id="1a023-142">迁移流程是不可逆的。</span><span class="sxs-lookup"><span data-stu-id="1a023-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="1a023-143">更改小数位数</span><span class="sxs-lookup"><span data-stu-id="1a023-143">Changing the number of decimal places</span></span>

<span data-ttu-id="1a023-144">迁移完成后，Dataverse 可以存储具有更多小数位的数字。</span><span class="sxs-lookup"><span data-stu-id="1a023-144">After the migration is completed, Dataverse can store numbers that have more decimal places.</span></span> <span data-ttu-id="1a023-145">管理员可以选择用于特定币种代码和定价的小数位数。</span><span class="sxs-lookup"><span data-stu-id="1a023-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="1a023-146">然后，Microsoft Power Apps、Power BI 和 Power Automate 的用户可以查看和使用具有更多小数位的数字。</span><span class="sxs-lookup"><span data-stu-id="1a023-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="1a023-147">要进行此更改，您必须在 Power Apps 中更新以下设置：</span><span class="sxs-lookup"><span data-stu-id="1a023-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="1a023-148">**系统设置：定价的货币精度** – **设置用于整个系统定价的货币精度** 列定义当选择 **定价精度** 时货币在组织中的行为方式。</span><span class="sxs-lookup"><span data-stu-id="1a023-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** column defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="1a023-149">**业务管理：货币** – **货币精度** 列可让您指定特定货币的自定义小数位数。</span><span class="sxs-lookup"><span data-stu-id="1a023-149">**Business Management: Currencies** – The **Currency Precision** column lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="1a023-150">组织范围的设置可以回退。</span><span class="sxs-lookup"><span data-stu-id="1a023-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="1a023-151">存在一些限制：</span><span class="sxs-lookup"><span data-stu-id="1a023-151">There are some limitations:</span></span>

+ <span data-ttu-id="1a023-152">您无法在表上配置货币列。</span><span class="sxs-lookup"><span data-stu-id="1a023-152">You can't configure the currency column on a table.</span></span>
+ <span data-ttu-id="1a023-153">您只能在 **定价** 和 **交易货币** 级别指定四个以上的小数位。</span><span class="sxs-lookup"><span data-stu-id="1a023-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="1a023-154">系统设置：定价的货币精度</span><span class="sxs-lookup"><span data-stu-id="1a023-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="1a023-155">迁移完成后，管理员可以设置货币精度。</span><span class="sxs-lookup"><span data-stu-id="1a023-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="1a023-156">转到 **设置 \> 管理**，然后选择 **系统设置**。</span><span class="sxs-lookup"><span data-stu-id="1a023-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="1a023-157">然后，在 **常规** 选项卡上，更改 **设置用于整个系统定价的货币精度** 列的值，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="1a023-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** column, as shown in the following illustration.</span></span>

![货币的系统设置](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="1a023-159">业务管理：货币</span><span class="sxs-lookup"><span data-stu-id="1a023-159">Business Management: Currencies</span></span>

<span data-ttu-id="1a023-160">如果您需要特定货币的货币精度与用于定价的货币精度不同，可以对其进行更改。</span><span class="sxs-lookup"><span data-stu-id="1a023-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="1a023-161">转到 **设置 \> 业务管理**，选择 **货币**，然后选择要更改的货币。</span><span class="sxs-lookup"><span data-stu-id="1a023-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="1a023-162">然后，将 **货币精度** 列设置为所需的小数位数，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="1a023-162">Then set the **Currency Precision** column to the number of decimal places that you want, as shown in the following illustration.</span></span>

![特定区域的货币设置](media/specific-currency.png)

### <a name="tables-currency-column"></a><span data-ttu-id="1a023-164">表：货币列</span><span class="sxs-lookup"><span data-stu-id="1a023-164">tables: Currency column</span></span>

<span data-ttu-id="1a023-165">可以为特定货币列配置的小数位数限制为四个。</span><span class="sxs-lookup"><span data-stu-id="1a023-165">The number of decimal places that can be configured for specific currency columns is limited to four.</span></span>
