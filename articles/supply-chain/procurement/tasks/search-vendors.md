---
title: 搜索供应商
description: 了解如何基于特定条件检索供应商。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86fced38d0ac73e67d04a59c5f39f4ec9b192daa
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571902"
---
# <a name="search-for-vendors"></a>搜索供应商

[!include [task guide banner](../../includes/task-guide-banner.md)]

了解如何基于特定条件检索供应商。 此示例显示了如何检索被批准用于特定采购类别，并拥有特定国家内首选地址的供应商。 您可以使用 USMF 公司演示数据，也可使用您自己的数据运行该过程。 此任务通常由采购专业人员完成。

1. 转到“采购”>“供应商”>“供应商检索”。
2. 单击“加号”图标以打开采购类别选择页。  
3. 在树形图中，选择“企业采购类别\办公设备“。
    * 如果您正在运行该过程以作为任务指南，您可能必须单击“解除锁定”按钮，然后才可以选择正确的节点。 如果您没有使用 USMF，选择您拥有的某一类别。  
4. 单击“添加”。
    * 有可能在此选择多个类别。 如果您这样做，检索将会查找被核准用于至少一个类别的所有供应商。  
5. 单击“确定”。
6. 在“国家/地区”字段中，键入一个值。
7. 单击“确定”。

