---
title: 创建科目结构
description: 此任务指南介绍创建科目结构的步骤。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7dd71cc072d49f47b1d77d3a688984cd4aaa624
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571274"
---
# <a name="create-account-structures"></a>创建科目结构

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务指南介绍创建科目结构的步骤。 步骤使用演示数据公司 USMF。

1. 转到“总帐”>“会计科目表”>“结构”>“配置科目结构”。
2. 单击“新建”，以打开对话框。
3. 在“科目结构”字段中，输入描述科目结构的用途的名称。
4. 在“描述”字段中，输入指出科目结构用途的描述。
5. 单击“创建”。
6. 单击“添加分部”。
7. 在“维度”列表中，选择要添加到科目结构的维度。
8. 单击“添加分部”。
9. 单击“添加分部”。
10. 在“维度”列表中，选择要添加到科目结构的维度。
11. 单击“添加分部”。
12. 单击“添加分部”。
13. 在“维度”列表中，选择要添加到科目结构的维度。
14. 单击“添加分部”。
15. 在网格中，选择分部以编辑允许的值。
    * 例如，单击“主科目”。  
16. 在“运算符”字段中，选择一个选项，例如“介于并包含”。
17. 在“值”字段中，键入一个值。
    * 例如：600000。  
18. 在“范围”字段中，键入一个值。
    * 例如：699999。  
19. 单击“应用”。
20. 在网格中，选择分部以编辑允许的值。
    * 例如：部门。  
21. 在“运算符”字段中，选择一个选项，例如“介于并包含”。
22. 在“值”字段中，键入一个值。
    * 例如：022。  
23. 在“范围”字段中，键入一个值。
    * 例如：031。  
24. 单击“添加新条件”。
25. 在“运算符”字段中，选择一个选项，例如“介于并包含”。
26. 在“值”字段中，键入一个值。
    * 例如：033。  
27. 在“范围”字段中，键入一个值。
    * 例如：034。  
28. 单击“应用”。
29. 在网格中，选择分部以编辑允许的值。
    * 例如：成本中心。  
30. 在“成本中心”字段中，键入一个值。
    * 例如：007..021。  
31. 单击“添加”。
32. 在“主科目”字段中，键入一个值。
    * 例如：600000..699999  
33. 在网格中，选择分部以编辑允许的值。
    * 例如：部门。  
34. 在“部门”字段中，键入一个值。
    * 例如：032。  
35. 在“成本中心”字段中，键入一个值。
    * 例如：086。  
36. 单击“验证”。
37. 单击“启用”。
38. 单击“启用”。

