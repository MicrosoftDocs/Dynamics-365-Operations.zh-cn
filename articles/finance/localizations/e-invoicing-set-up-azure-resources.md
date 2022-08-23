---
title: 设置电子开票的 Azure 资源
description: 本文概述了为电子开票设置 Microsoft Azure 资源的流程。
author: gionoder
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f11e4eac831d54a6cac765a5adc4e4ffddbe0a22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283076"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>设置电子开票的 Azure 资源

[!include [banner](../includes/banner.md)]

为电子开票设置 Microsoft Azure 资源的流程分为三个步骤。 前两个步骤“在 Azure 门户中创建 Azure 密钥保管库”和“在 Azure 门户中创建 Azure 存储帐户”是必须完成的步骤。 第三个步骤“配置 SharePoint 连接”是可选的。

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>在 Azure 门户中创建 Azure 密钥保管库

在 Azure 订阅中创建密钥保管库。 我们建议您为电子开票创建单独的密钥保管库，并且不要将机密与其他应用程序合并。 在电子单据中为您的场景创建所需数量的机密和证书。 您必须创建至少一个机密来存储您将在下一步中创建的 Azure 存储帐户的共享访问签名 (SAS) 令牌。

有关如何完成此步骤的信息，请参阅[在 Azure 门户中创建 Azure 密钥保管库](e-invoicing-create-azure-key-vault-azure-portal.md)。

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>在 Azure 门户中创建 Azure 存储帐户

您负责由电子开票服务生成或进入该服务的所有电子单据和文件。 这些单据和文件存储在您在 Azure 订阅中创建的 Azure 存储帐户中。 服务将使用从您的 Key Vault 机密中获取的 SAS 令牌访问您的存储帐户。

有关如何完成此步骤的信息，请参阅[在 Azure 门户中创建 Azure 存储帐户](e-invoicing-create-azure-storage-account-azure-portal.md)。

## <a name="configure-a-sharepoint-connection"></a>配置 SharePoint 连接

在某些情况下，您可能需要将电子文件保存到 SharePoint 并从 SharePoint 检索它们。 为确保电子开票服务可以访问您的 SharePoint 文件夹，请配置对 SharePoint 的访问权限。

有关如何完成此步骤的信息，请参阅[配置 SharePoint 连接](e-invoicing-create-sharepoint-connection.md)。
