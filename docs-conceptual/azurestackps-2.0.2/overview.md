---
title: Azure Stack Hub Admin PowerShell 개요 | Microsoft Docs
description: 설치 및 구성 지침이 포함된 Azure Stack Hub Admin PowerShell 개요입니다.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: 754038a312a20e0dd87075bdeb51b13a1f1810a1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "88022969"
---
# <a name="azure-stack-hub-module-202"></a><span data-ttu-id="32e06-103">Azure Stack Hub 모듈 2.0.2</span><span class="sxs-lookup"><span data-stu-id="32e06-103">Azure Stack Hub Module 2.0.2</span></span>

## <a name="requirements"></a><span data-ttu-id="32e06-104">요구 사항:</span><span class="sxs-lookup"><span data-stu-id="32e06-104">Requirements:</span></span>

<span data-ttu-id="32e06-105">지원되는 최소 Azure Stack Hub 버전은 2002입니다.</span><span class="sxs-lookup"><span data-stu-id="32e06-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="32e06-106">참고: 이전 버전의 Azure Stack인 경우 [Azure Stack Powershell 설치](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="32e06-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="32e06-107">설치</span><span class="sxs-lookup"><span data-stu-id="32e06-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.2-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="32e06-108">릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="32e06-108">Release Notes</span></span>

* <span data-ttu-id="32e06-109">2002 업데이트가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="32e06-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="32e06-110">Azure Stack Hub 2.0.0은 호환성이 손상되는 변경입니다.</span><span class="sxs-lookup"><span data-stu-id="32e06-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="32e06-111">이 모듈은 AzureRM 모듈이 아니라 Az 모듈을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="32e06-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="32e06-112">[Azure Stack Hub에서 AzureRM을 Azure PowerShell Az로 마이그레이션](https://aka.ms/AA7qsji)에서 마이그레이션 가이드 및 호환성이 손상되는 변경 목록을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32e06-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](https://aka.ms/AA7qsji).</span></span>
