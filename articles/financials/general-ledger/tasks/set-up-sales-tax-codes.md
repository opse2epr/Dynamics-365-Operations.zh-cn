---
title: 设置销售税代码
description: 为法人实体必须计算、征收和向销售税主管机构缴纳的所有间接税或关税创建销售税代码。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571575"
---
# <a name="set-up-sales-tax-codes"></a>设置销售税代码

[!include [task guide banner](../../includes/task-guide-banner.md)]

为法人实体必须计算、征收和向销售税主管机构缴纳的所有间接税或关税创建销售税代码。

本任务使用 USMF 公司进行演示。



1. 转到报税>间接税>销售税》销售税代码。
2. 单击“新建”。
3. 在“销售税代码”字段中，输入一个值。
4. 在“名称”字段中，键入一个值。
5. 选择某一结算期间，以指定需要在哪一期间间隔内必须向哪一销售税主管机构申报和缴纳。
6. 在列表中，单击所选行中的链接。
7. 选择分类帐过帐组，以指定将销售税过帐到总帐的主科目。
8. 在列表中，找到并选择所需记录。
9. 在列表中，单击所选行中的链接。
10. 展开“计算”快速选项卡。
    * “计算”快速选项卡有多个字段，可控制销售税金额计算方式。  
11. 在操作窗格上，单击“销售税代码”。
12. 单击“数值”。
13. 在列表中，标记所选的行。
14. 输入此税费代码的值。
    * 在“计算”快速选项卡上的“来源”字段中，如果选择“单位金额”，将用该数值乘以该交易记录数量得出销售税金额。  如果销售税代码不是基于单位税，则该值为在用于该税码的来源上，用以计算销售税金额的百分比。     
15. 单击“保存”。
16. 关闭该页面。
17. 单击“保存”。

