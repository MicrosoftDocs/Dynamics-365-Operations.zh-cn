---
title: 创建 Azure 存储帐户和密钥保管库
description: 本主题说明如何创建 Azure 存储帐户和密钥保管库。
author: gionoder
ms.date: 08/17/2021
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
ms.openlocfilehash: 23fec7a00d800719e1a7d2c90f9d0977d56be038
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463834"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>创建 Azure 存储帐户和密钥保管库

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>先决条件

您必须确保先完成以下任务，然后才能完成本主题中的步骤：

- 在 Azure 中创建密钥保管库资源。 有关详细信息，请参阅[关于 Azure 密钥保管库](/azure/key-vault/general/overview)。
- 创建 Azure 存储帐户（Blob 存储）。 有关详细信息，请参阅[维护 Azure 存储帐户](/azure/storage/blobs/)。

## <a name="overview"></a>概览

在本主题中，您将完成两个主要步骤：

- 设置 Azure 存储帐户以获取存储帐户 URI。
- 设置密钥保管库以存储存储帐户 URI。

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>设置 Azure 存储帐户以获取存储帐户 URI

1. 打开您计划与电子开票一起使用的存储帐户。
2. 转到 **数据存储** > **容器**，然后创建一个新容器。
3. 为容器输入名称，然后将 **公共访问级别** 字段设置为 **专用(无匿名访问)**。
4. 打开该容器，然后转到 **设置** > **访问策略**。
5. 选择 **添加策略** 添加存储的访问策略。
6. 根据需要设置 **标识符** 和 **权限** 字段。 在 **权限** 字段中，您应该选择所有权限。

    ![授予 Blob 存储权限。](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. 输入开始日期和到期日期。 到期日期应该在将来。
8. 选择 **确定** 保存策略，然后保存对容器进行的更改。
9. 转到 **设置** > **共享访问令牌**，然后设置字段值。 
10. 输入开始日期和结束日期。 结束日期应该在将来。
11. 在 **权限** 字段中，选择以下权限：**读取**、**添加**、**创建**、**写入**、**删除** 和 **列举**。 
12. 选择 **生成 SAS 令牌和 URL**。
13. 复制并存储 **Blob SAS URL** 字段中的值。 此值将在下一个过程中使用，将称为 *共享访问签名 URI*。

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>设置密钥保管库以存储存储帐户 URI

1. 打开您打算与电子开票一起使用的密钥保管库。
2. 转到 **设置** \> **密码**，然后选择 **生成/导入** 创造新密码。
3. 在 **创建密码** 页上，在 **上载选项** 字段中，选择 **手动**。
4. 输入密码的名称。 此名称将在 Regulatory Configuration Service (RCS) 中的服务设置期间使用，将称为 *密钥保管库密码名称*。
5. 在 **值** 字段中，输入在上一个过程中复制的共享访问签名 URI，然后选择 **创建**。
6. 设置访问策略，以授予电子开票访问您创建的密码的正确安全访问级别。 转到 **设置 \> 访问策略**，选择 **添加访问策略**。
7. 为 **获取** 和 **列出** 操作设置密码权限。

    ![授予服务访问权限。](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. 为 **获取** 和 **列出** 操作设置证书权限。

    ![授予证书权限。](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. 在 **选择主体** 字段中，选择 **未选择**。
10. 在 **主体** 对话框中，通过添加 **电子开票服务** 选择主体。
11. 选择 **添加**，然后选择 **保存**。
12. 在 **概览** 页上，复制密钥保管库的 **DNS 名称** 值。 此值将在 RCS 中的服务设置期间使用，将称为 *密钥保管库 URI*。

> [!NOTE]
> 要额外增加存储帐户的安全性，应配置 Azure Defender for Storage。
> 
> 有关详细信息，请参阅 [Azure Defender for Storage 简介](/azure/security-center/defender-for-storage-introduction)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
