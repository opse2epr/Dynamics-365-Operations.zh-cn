---
title: "用户可以访问 Core HR，但无法访问 Onboard 或 Attract 应用"
description: "此主题介绍如何解决用户可以访问 Microsoft Dynamics 365 for Talent Core HR 但无法访问 Attract 或 Onboard 应用的问题。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: zh-cn
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="6c9c0-103">用户可以访问 Core HR，但无法访问 Onboard 或 Attract 应用</span><span class="sxs-lookup"><span data-stu-id="6c9c0-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c9c0-104">**环境详细信息**</span><span class="sxs-lookup"><span data-stu-id="6c9c0-104">**Environment details**</span></span>

- <span data-ttu-id="6c9c0-105">Microsoft Dynamics Lifecycle Services (LCS) 部署由用户 A 完成。</span><span class="sxs-lookup"><span data-stu-id="6c9c0-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="6c9c0-106">用户 A 将用户 B 作为用户添加到 Microsoft Dynamics 365 for Talent Core HR。</span><span class="sxs-lookup"><span data-stu-id="6c9c0-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="6c9c0-107">**发货**</span><span class="sxs-lookup"><span data-stu-id="6c9c0-107">**Issue**</span></span>

<span data-ttu-id="6c9c0-108">用户 B 可以访问 Core HR，但无法访问 Talent: Attract 或 Talent: Onboard 应用。</span><span class="sxs-lookup"><span data-stu-id="6c9c0-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="6c9c0-109">在用户尝试转到**体验应用**时，用户被带入试用环境。</span><span class="sxs-lookup"><span data-stu-id="6c9c0-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="6c9c0-110">**解决方案**</span><span class="sxs-lookup"><span data-stu-id="6c9c0-110">**Solution**</span></span>

<span data-ttu-id="6c9c0-111">用户 B 必须在设置过程被分配查看用户 A 创建的 Microsoft PowerApps 环境的权限。</span><span class="sxs-lookup"><span data-stu-id="6c9c0-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="6c9c0-112">有关信息，请参阅[配置 Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) 中的“授予对环境的访问权限”部分。</span><span class="sxs-lookup"><span data-stu-id="6c9c0-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="6c9c0-113">**长期解决方案**</span><span class="sxs-lookup"><span data-stu-id="6c9c0-113">**Long-term solution**</span></span>

<span data-ttu-id="6c9c0-114">Microsoft 正在考虑当用户被添加到 Core HR 时自动向 Onboard 和 Attract 分配相应权限。</span><span class="sxs-lookup"><span data-stu-id="6c9c0-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
