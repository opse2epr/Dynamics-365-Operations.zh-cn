---
title: 审核特定采购类别的供应商
description: 创建采购申请时，可能需要选择核准供应商或首选供应商，具体取决于制订的采购政策。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b783d1ce8f02ad119dc6768e6d9cd3c61ae07e70
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566425"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>审核特定采购类别的供应商

[!include [task guide banner](../../includes/task-guide-banner.md)]

创建采购申请时，可能需要选择核准供应商或首选供应商，具体取决于制订的采购政策。 此过程演示如何指定供应商是特定采购类别的核准供应商或首选供应商。 此任务通常由采购专业人员完成。 您可以在演示数据公司 USMF 中使用此过程。

1. 转到“采购”>“供应商”>“所有供应商”。
2. 选择要设置为类别的核准供应商或首选供应商的供应商。
3. 在操作窗格上，单击“常规”。
4. 单击“类别”。
5. 单击“添加类别”。
6. 在“类别”字段中，选择“办公和桌面附件(办公和桌面附件)”。
7. 在“供应商类别状态”字段中，选择“首选”。
    * 可以为一个类别指定多家首选供应商。  
8. 单击“保存”。
9. 转到采购>采购目录。 
10. 在树中，选择“企业采购类别\办公和桌面附件“。
11. 展开“供应商”部分。
    * 检查所选供应商是否显示为办公室和桌面附件类别的首选供应商。 如果您要将此过程作为任务指南运行，可能必须单击“解锁”按钮才能向下滚动到供应商列表。  还可以在此页中添加首选供应商和核准供应商。  
12. 在树中，展开“办公和桌面附件”。
13. 在树中，选择“剪刀”。
14. 在“从父类别继承供应商:”字段中选择“否”。
15. 在“从父类别继承供应商:”字段中选择“是”。

