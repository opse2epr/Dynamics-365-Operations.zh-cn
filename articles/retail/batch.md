---
title: 改进了批量跟踪物料的处理
description: 此主题介绍了对零售对帐单过帐驱动程序流程中批量跟踪物料的批次处理所做的改进。
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617381"
---
# <a name="improved-handling-of-batch-tracked-items"></a>改进了批量跟踪物料的处理

在 Microsoft Dynamics 365 for Retail 销售点 (POS) 中，无法在销售时捕获批量跟踪物料的批处理号。 但是，对于特定配置，在总部通过客户订单或对帐单过帐来过帐销售额时，Microsoft Dynamics 系统要求批量跟踪物料具备有效的批处理号，这些编号在开票流程中使用。

如果有效的批处理号对产品可用，则来自对帐单过帐的客户订单开票流程和销售订单开票流程使用这些编号。 否则，客户订单开票流程无法过帐，POS 用户将收到错误消息。 对帐单过帐随后会进入错误状态。 即使为产品启用了负库存，也会出现此错误状态。

在 Microsoft Dynamics for Retail 版本 10.0.4 和更高版本中进行的改进可帮助确保在为批量跟踪物料启用了负库存时，如果库存为 0（零）或者批处理号不可用，不会阻止这些物料通过对帐单过帐进行客户订单开票和销售订单开票。 批处理号不可用时，新功能会使用销售行的默认批处理 ID。

要定义为客户订单使用的默认批处理 ID，请在**零售参数**页面的**客户订单**选项卡上，在**订单**快速选项卡中设置**默认批处理 ID** 字段。

要定义为通过对帐单过帐进行的销售订单开票使用的默认批处理 ID，请在**零售参数**页面的**过帐**选项卡上，在**库存更新**快速选项卡中设置**默认批处理 ID** 字段。

> [!NOTE]
> 只有为特定商店仓库和物料启用了高级仓储时，此功能才可用。 在以后的版本中，未使用高级仓库管理的方案也将支持此功能。
