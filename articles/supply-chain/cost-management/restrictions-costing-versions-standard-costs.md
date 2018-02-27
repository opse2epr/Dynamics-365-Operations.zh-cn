---
title: "对标准成本的成本计算版本的限制"
description: "本主题介绍适用于标准成本的成本计算版本的限制。"
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e14d5d11e987d2dbc841f86c39fc7e94864144d3
ms.openlocfilehash: 658575492597eed91509561f4710f07e271c53c8
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="519d4-103">对标准成本的成本计算版本的限制</span><span class="sxs-lookup"><span data-stu-id="519d4-103">Restrictions on costing versions for standard costs</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="519d4-104">本主题介绍适用于标准成本的成本计算版本的限制。</span><span class="sxs-lookup"><span data-stu-id="519d4-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="519d4-105">以下限制有助于确保符合标准成本计算准则：</span><span class="sxs-lookup"><span data-stu-id="519d4-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="519d4-106">费用必须包括在某一物料的成本中。</span><span class="sxs-lookup"><span data-stu-id="519d4-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="519d4-107">制造物料的费用表示在物料清单 (BOM) 和工艺路线信息内的摊销的固定成本。</span><span class="sxs-lookup"><span data-stu-id="519d4-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="519d4-108">因此，单位成本中必须包括这些费用。</span><span class="sxs-lookup"><span data-stu-id="519d4-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="519d4-109">采购物料的费用也包括在物料的单位成本中。</span><span class="sxs-lookup"><span data-stu-id="519d4-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="519d4-110">制造物料的标准成本计算必须基于标准成本的成本计算版本内的成本记录。</span><span class="sxs-lookup"><span data-stu-id="519d4-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="519d4-111">成本数据的备选来源只能用于计划成本的成本计算版本，例如针对采购物料的销售价贸易协议。</span><span class="sxs-lookup"><span data-stu-id="519d4-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="519d4-112">成本数据的备用来源由 BOM 计算组定义。</span><span class="sxs-lookup"><span data-stu-id="519d4-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="519d4-113">BOM 计算必须在单级分解模式下执行。</span><span class="sxs-lookup"><span data-stu-id="519d4-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="519d4-114">标准成本的物料成本数据可以复制到包含标准成本或计划成本的其他成本计算版本中。</span><span class="sxs-lookup"><span data-stu-id="519d4-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="519d4-115">但是，计划成本的物料成本数据不能复制到包含标准成本的成本版本中，因为本主题中的前述限制将不应用于计划成本。</span><span class="sxs-lookup"><span data-stu-id="519d4-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="519d4-116">相关主题</span><span class="sxs-lookup"><span data-stu-id="519d4-116">Related topics</span></span>
--------

[<span data-ttu-id="519d4-117">成本计算版本</span><span class="sxs-lookup"><span data-stu-id="519d4-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="519d4-118">更新非制造环境中的标准成本</span><span class="sxs-lookup"><span data-stu-id="519d4-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="519d4-119">准备为制造物料维护标准成本</span><span class="sxs-lookup"><span data-stu-id="519d4-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)

