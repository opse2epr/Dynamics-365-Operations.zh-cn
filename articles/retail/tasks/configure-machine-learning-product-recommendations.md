---
title: 配置机器学习支持的产品建议
description: 此过程刷新实体商店中为生产建议提供支持的机器学习系统使用的数据，然后启用有关 POS 客户端的产品建议。
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548431"
---
# <a name="configure-machine-learning-powered-product-recommendations"></a>配置机器学习支持的产品建议

[!include[task guide banner](../includes/task-guide-banner.md)]

此过程刷新实体商店中为生产建议提供支持的机器学习系统使用的数据，然后启用有关 POS 客户端的产品建议。 此程序使用 USRT 演示数据公司。

1. 转到“系统管理”>“设置”>“实体商店”。
2. 在列表中，找到并选择记录“RetailSales”。
3. 单击“刷新”。
4. 单击“确定”。
5. 关闭该页面。
6. 转到“零售和商业”>“总部设置”>“参数”>“零售参数”。
7. 单击“机器学习”选项卡。
8. 在“启用产品建议”字段中选择“是”。
    * 如果收到消息“无法检索建议模型”，这是因为您最近刷新了实体商店，并且系统可能尚未完成新数据的吸收。 等待 2-3 小时再重试。  
9. 单击“保存”。
10. 关闭该页面。

