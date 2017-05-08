---
title: "使用普通日记帐实体导入凭证的最佳实践"
description: "本主题提供使用普通日记帐实体将数据导入到普通日记帐的建议。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>使用普通日记帐实体导入凭证的最佳实践

[!include[banner](../includes/banner.md)]


本主题提供使用普通日记帐实体将数据导入到普通日记帐的建议。  

您可以使用一般日记帐实体导入类型为**分类帐、客户或银行**的科目或对方科目。 凭证可以同时使用**科目**字段和**对方科目**字段输入为一行，也可以输入为多行凭证，这种情况下仅使用**科目**字段（每行中将**对方科目**保留为空。） 普通日记帐实体并非支持每个科目类型。 相反，其他实体在需要帐户类型的不同组合的情况下存在。 例如，要导入项目交易记录，请使用项目费用日记帐实体。 每个实体设计为支持特定方案，这意味着这些方案的实体中可能有更多字段，但是在其他方案的实体中则未必。

## <a name="setup"></a>设置
在使用一般日记帐实体导入之前，请验证以下设置︰

-   **日记帐批处理号的编号规则设置** – 默认情况下，当您使用一般日记帐实体导入时，日记帐批处理号将使用在总帐参数中定义的编号规则。 对于到日记帐批处理号，如果设置编号规则为**手动**，则不应用默认编号。 不支持此设置。
-   **财务维度配置** – 当实体用于导入交易记录时，每个组织必须定义财务维度的顺序。 为**分类帐维度集成**格式定义顺序，在**总帐** &gt; **会计科目表** &gt; **维度** &gt; **用于集成应用程序的财务维度配置 **&gt; **选择数据实体**。 导入的会计科目的段必须具有相同的顺序。 否则，导入过程中将发生错误。

## <a name="general-journal-entity-setup"></a>普通日记帐实体设置
数据管理的两个设置影响如何应用默认日记帐批处理号或凭证号︰

-   **基于集的处理**（在数据实体上）
-   **自动生成**（在字段映射时）)

以下各部分描述了这些设置的效果，还介绍了如何生成日记帐批处理号和凭证号。

### <a name="journal-batch-number"></a>日记帐批处理号

-   在普通日记帐实体上设置的**基于集的处理**不会影响生成日记帐批处理号的方式。
-   如果**日记帐批处理号**字段设置为**自动生成**，则为导入的每一行创建新的日记帐批处理号。 不建议此行为。 **自动生成**设置在导入项目中，在**查看地图**下，**映射详细信息**选项卡上。
-   如果**日记帐批处理号**字段未设置为**自动生成**，则按如下方式创建日记帐批处理号：
    -   如果在导入文件中定义的日记帐批处理号匹配 Microsoft Dynamics 365 for Operations 中现有的未过帐的每日日记帐，具有匹配日记帐批处理号的所有行导都入到现有日记帐。 行不会导入已过帐的日记帐批处理号。 相反，将创建新编号。
    -   如果在导入文件中定义的日记帐批处理号不匹配 Dynamics 365 for Operations 中现有的未过帐的每日日记帐，相同日记帐批处理号将在新日记帐下分组。 例如，有 1 日记帐批处理号的所有行都导都入到某一新日记帐，并且日记帐批处理号为 2 的所有行都导入到第二个新的日记帐。 通过使用在总帐参数中定义的编号规则创建日记帐批处理号。

### <a name="voucher-number"></a>凭证号

-   当您在普通日记帐实体中使用**基于集的处理**设置时，凭证号必须在导入的文件中提供。 普通日记帐中的每个交易记录被分配在导入文件中提供的凭证编号，即使凭证不均衡。 如果您想要使用基于集的处理，但还需要使用为 Dynamics 365 for Operations 中的凭证号定义的编号规则，则为 2016 年 2 月版本提供修复程序。 修补程序编号为 3170316，可从 Lifecycle services (LCS) 下载。 有关详细信息，请参阅[从 Lifecycle Services 下载修补程序](..\migration-upgrade\download-hotfix-lcs.md)。
    -   若要启用此功能，在用于在 Dynamics 365 for Operations 中导入的日记帐名称中，设置**过帐时分配编号**为**是**。
    -   仍然必须在导入文件中定义一个凭证号。 但是，此数字是临时的并在过帐日记帐时由 Dynamics 365 for Operations 凭证号覆盖。 您必须确保日记帐的各行按临时凭证号进行正确分组。 例如，在过帐期间，发现三行具有临时凭证号 1。 所有三个行的临时凭证号由编号规则中的下一个编号覆盖。 如果这三行不是平衡条目，将不过帐凭证。 接下来，如果找到具有临时凭证号 2 的行，这个数字将由编号规则中的下个凭证号覆盖，依此类推。

<!-- -->

-   当您不使用**基于集的处理**设置时，无需在导入的文件中提供凭证号。 在基于日记帐名称的设置导入过程中创建凭证号（**仅一个凭证**，**与余额有关联**等）。 例如，如果日记帐名称定义为**与余额有关联**，第一行接收新的默认凭证号。 然后，系统评估行以确定借方是否等于贷方。 如果行上存在对方科目，导入的下一行接收新的凭证号。 如果对方科目不存在，系统会评估借方是否等于贷方，因为将导入每个新行。
-   如果**凭证号**字段设置为**自动生成**，导入将不会成功。 **凭证号**字段的**自动生成**设置不受支持。

默认情况下，普通日记帐实体使用基于集的处理。 评估您的组织的业务需求之后，您可以通过单击**数据管理**工作区的**数据实体**更改**基于集的处理**设置。 基于集的处理用于加快导入流程。 如果不使用基于集的处理，普通日记帐实体导入的导入将变慢。



