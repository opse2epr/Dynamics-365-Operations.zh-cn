---
title: "设置固定资产"
description: "文主题提供固定资产模块设置的概览。"
author: twheeloc
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 668fea64810524e8ce0c3833d25656c026f2780a
ms.openlocfilehash: d16c9ca5740c27528d74800957f9b47984c135cd
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2017

---

# <a name="set-up-fixed-assets"></a>设置固定资产

[!include[banner](../includes/banner.md)]


文主题提供固定资产模块设置的概览。

<a name="overview"></a>概览
--------
参数控制固定资产内的常规行为。

固定资产组可以对您的资产分组以及为分配到组的每项资产指定缺省属性。 将帐簿分配到固定资产组。 帐簿使用在折旧模板中定义的折旧配置跟踪固定资产在一段时期内的经济价值。

固定资产在创建时分配到组。 默认情况下，分配到固定资产组的帐簿会分配到固定资产。 配置为过帐到总帐的帐簿与过帐模板相关联 会计科目按照过帐模板中的帐簿进行定义，对固定资产交易记录过帐时使用。 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>折旧模板
您应首先设置折旧模板。 在折旧模板中，您可以配置资产价值随时间推移折旧的方式。 您必须定义折旧方法、折旧年份（日历年度或会计年度）和折旧频率。 有关详细信息，请参阅[设置和创建折旧模板](tasks/set-up-depreciation-profiles.md)。

## <a name="books"></a>帐簿
在设置折旧模板后，您必须为您的资产创建所需帐簿。 每个帐簿跟踪资产的一个独立的财务生命周期。 帐簿可以配置为将关联交易记录过帐到总帐。 此配置为默认设置，因为它通常用于公司财务报告。 不过帐到总帐的帐簿仅过帐到固定资产子分类账，并且通常用于税务申报目的。

主折旧模板分配给每个帐簿。 帐簿还有备选或替换的折旧模板，如果这种模板类型适用。 若要自动在折旧运行时包括固定资产帐簿，则必须启用此“计算折旧”选项。 如果不为资产选择此选项，折旧方案将跳过资产。

您还可以设置衍生帐簿。 指定的衍生交易记录将过帐为针对衍生帐簿的主交易记录的精确副本。 因此，衍生交易记录通常针对购置和处置进行设置，而不是针对折旧交易记录。
有关详细信息，请参阅[设置帐簿](tasks/set-up-value-models.md)。

## <a name="fixed-asset-posting-profiles"></a>固定资产过帐模板
设置帐簿后，您可以创建过帐模板。 过帐模板必须由帐簿定义，但也可以在更详细的级别上进行定义。 例如，您可以为帐簿和固定资产组的组合，或者甚至是单独的固定资产帐簿定义过帐模板。 默认情况下，固定资产交易记录会使用定义的会计科目。

您必须定义在处理流程（处置销售和处置报废）中使用的会计科目。 在处置时，之前过帐的固定资产交易记录将在原始科目之外进行冲销并且会将净额移至相应的资产处置的损益科目。 为了帮助保障交易记录已正确冲销，您必须为您在业务中使用的每种交易记录类型设置科目。 主科目应为您在该交易记录类型过帐模板上设置的原始科目，而对方科目应为处置损益科目。 帐面净值是例外情况。 在这种情况下，应将主科目和对方科目设置为处置损益科目。 有关详细信息，请参阅[设置固定资产过帐模板](tasks/set-up-fixed-asset-posting-profiles.md)。

## <a name="fixed-asset-groups"></a>固定资产组
固定资产组是在创建固定资产时的唯一必需字段。 此字段值将决定资产若干信息字段的默认值。 设置帐簿，以便将默认帐簿分配到组中的每一个资产。 您之后可以设置资产组的特定帐簿属性，例如“使用年限”和“折旧惯例”。

您还可以为固定资产组与帐簿的特定组合定义特殊折旧补偿或额外折旧。 您必须为特殊折旧补偿指定优先级，以指定在为一个帐簿分配多个补偿时的补偿计算顺序。 有关详细信息，请参阅[设置固定资产组](tasks/set-up-fixed-asset-groups.md)。

## <a name="fixed-asset-parameters"></a>固定资产参数
最后一步是更新固定资产参数。

**资本化阈值**字段确定折旧的资产。 如果选择采购行为固定资产，但不满足指定的资本化阈值，则将仍然创建或更新固定资产，但“计算折旧”选项设置为“否”。 因此，资产不会作为折旧方案的一部分自动折旧。

一个重要选项是“**使用处置来自动创建折旧调整金额**”。 将此选项设置为“**是**”后，将基于资产处置时的折旧设置自动调整资产折旧。 另外一个选项可以在使用供应商发票购置固定资产时从您的购置金额中扣减现金折扣。

在“采购订单”快速选项卡上，您可以将创建资产的方式配置为采购流程的一部分。 第一个选项是“允许从采购中购置资产”。 如果将此选项设置为“是”，则在过帐发票时发生资产购置。 如果将此选项设置为“否”，您仍然可以将固定资产放在采购订单 (PO) 和发票上，但不会过帐购置。 过帐需要作为与固定资产日记帐不同的单独步骤完成。 “在物料收货或发票过帐期间创建资产”选项可以在过帐期间“快速”创建新资产，因此新资产不需要在交易记录之前设置为固定资产。 最后一个选项，“检查行输入期间的固定资产创建”，仅适用于采购申请。

您可以配置原因代码，以便在更改固定资产或特定固定资产交易记录时需要使用。

最后，在“编号规则”选项卡上定义固定资产的编号规则。 如果指定了固定资产组编号规则，固定资产组编号规则将覆盖固定资产编号规则。

有关详细信息，请参阅[创建固定资产](tasks/create-fixed-asset.md)。

