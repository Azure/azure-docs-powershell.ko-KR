---
title: Azure Stack Admin PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 설명을 포함한 Azure Stack Admin PowerShell 개요입니다.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: 1b3d707e862dd0c21e9e6b0a89f429ff21b1a99d
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861338"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="ca09a-103">Azure Stack 모듈 1.7.2</span><span class="sxs-lookup"><span data-stu-id="ca09a-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="ca09a-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="ca09a-104">Requirements:</span></span>

<span data-ttu-id="ca09a-105">지원되는 최소 Azure Stack 버전은 1904입니다.</span><span class="sxs-lookup"><span data-stu-id="ca09a-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="ca09a-106">참고: 이전 버전의 Azure Stack인 경우 [Azure Stack Powershell 설치](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="ca09a-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="ca09a-107">설치</span><span class="sxs-lookup"><span data-stu-id="ca09a-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="ca09a-108">릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="ca09a-108">Release Notes</span></span>

* <span data-ttu-id="ca09a-109">1904 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="ca09a-109">Supported with 1904 update</span></span>
* <span data-ttu-id="ca09a-110">이는 호환성이 손상되는 변경 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="ca09a-110">This a breaking change release.</span></span> <span data-ttu-id="ca09a-111">호환성이 손상되는 변경에 대한 자세한 내용은 <https://aka.ms/azspshmigration170>를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca09a-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="ca09a-112">호환성이 손상되는 변경 내용: Backup이 인증서 기반 암호화 모드로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca09a-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="ca09a-113">대칭 키에 대한 지원은 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca09a-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="ca09a-114">호환성이 손상되는 변경에 대한 자세한 내용은 https://aka.ms/azspshmigration170 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca09a-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="ca09a-115">Azs.Storage.Admin 모듈</span><span class="sxs-lookup"><span data-stu-id="ca09a-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="ca09a-116">버그 수정 - 새 스토리지 할당량이 제공되지 않을 경우 기본값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ca09a-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>
