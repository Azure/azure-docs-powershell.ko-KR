---
title: FAQ(질문과 대답)
description: Azure PowerShell에 대한 질문과 대답입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101872347"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="24006-103">Azure PowerShell에 대한 질문과 대답</span><span class="sxs-lookup"><span data-stu-id="24006-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="24006-104">Azure PowerShell이란?</span><span class="sxs-lookup"><span data-stu-id="24006-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="24006-105">Azure PowerShell은 PowerShell을 사용하여 직접 Azure 리소스를 관리할 수 있는 cmdlet 세트입니다.</span><span class="sxs-lookup"><span data-stu-id="24006-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="24006-106">2018년 12월에서는 Az PowerShell 모듈이 일반 공급되었습니다.</span><span class="sxs-lookup"><span data-stu-id="24006-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="24006-107">이제 Azure와 상호 작용하는 데 권장되는 PowerShell 모듈이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="24006-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="24006-108">Az PowerShell 모듈에 대한 자세한 내용은 [새로운 Azure PowerShell Az 모듈 소개](/powershell/azure/new-azureps-module-az)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="24006-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="24006-109">Azure PowerShell에서 호환성이 손상되는 변경 경고 메시지를 비활성화하려면 어떻게 해야 하나요?</span><span class="sxs-lookup"><span data-stu-id="24006-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="24006-110">Azure PowerShell에서 호환성이 손상되는 변경 경고 메시지를 표시하지 않으려면 환경 변수 `SuppressAzurePowerShellBreakingChangeWarnings`를 `true`로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="24006-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
