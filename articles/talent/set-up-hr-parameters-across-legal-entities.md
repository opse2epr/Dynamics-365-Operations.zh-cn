---
title: 跨法人设置人力资源 (HR) 参数
description: 您必须为在公司间共享的记录设置共享参数，例如职位记录。 本文说明如何设置跨法人的人力资源参数。
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: a8167545864a1cc2fc22f044f7d16ca590d59b43
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517460"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a>跨法人设置人力资源 (HR) 参数

[!include [banner](includes/banner.md)]

您必须为在公司间共享的记录设置共享参数，例如职位记录。 本文说明如何设置跨法人的人力资源参数。

某些类型的记录（如位置记录）将在公司间共享。 对于这些记录，您必须设置共享的参数。 例如，您使用**人力资源共享参数**页设置法人之间的人力资源参数。 

在**人力资源共享参数**页上，将根据区域的功能将参数分组到相应区域中。 

### <a name="previously-released-functionality"></a>以前发布的功能
在**标识**选项卡上，您必须选择表示页面上列出的标识号的标识类型。 在您可以输入工作的人员的标识信息之前，必须设置标识类型。 有关社会保险号、国家/地区 ID 号、侨民 ID 号和个人 ID 代码的信息保留在**标识类型**页上。 要定义新的标识类型或检查现有类型的列表，请单击**人事管理** &gt; **链接选项卡** &gt; **设置** &gt; **标识类型**。 您可以输入简单的代码和描述。 

### <a name="if-youre-using-dynamics-365-for-talent"></a>如果您使用的是 Dynamics 365 for Talent
在**标识**选项卡上，您必须选择表示页面上列出的标识号的标识类型。 在您可以输入工作的人员的标识信息之前，必须设置标识类型。 有关社会保险号、国家/地区 ID 号、侨民 ID 号和个人 ID 代码的信息保留在**标识类型**页上。 要定义新的标识类型或检查现有类型的列表，请单击**人力资源** &gt; **设置** &gt; **标识类型**。 您可以输入简单的代码和描述。 

在**编号规则**选项卡上，您可以选择用于以下记录的编号规则：人员编号、职位、用户请求 ID、I-9 文档、申请人、讨论、福利 ID 和人事操作（如果此记录类型已启用）。 要维护编号规则引用和代码，请使用**编号规则**列表页。 要查找此页，请使用页搜索功能。 

在**职位**选项卡上，指示新的职位在默认情况下是否可分配：

-   **始终** – 创建新的职位时，可将工作人员分配到这些职位。 在创建职位时，**职位**页的**常规**选项卡上的**可进行分配的日期和时间**将自动设置为创建日期和时间。
-   **从不** – 创建新的职位时，您无法将工作人员分配到这些职位。 如果选择此选项，则您必须在每个新职位可用时打开其**职位**页，然后在**常规**选项卡上，输入**可用于分配**日期以启用工作人员分配。


<a name="additional-resources"></a>其他资源
--------

[设置特定于公司的 HR 参数](set-up-company-specific-hr-parameters.md)



