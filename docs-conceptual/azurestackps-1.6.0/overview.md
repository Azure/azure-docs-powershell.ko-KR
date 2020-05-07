---
title: Azure Stack Admin PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 설명을 포함한 Azure Stack Admin PowerShell 개요입니다.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053318"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="51916-103">Azure Stack 모듈 1.6.0</span><span class="sxs-lookup"><span data-stu-id="51916-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="51916-104">요구 사항:</span><span class="sxs-lookup"><span data-stu-id="51916-104">Requirements:</span></span>
<span data-ttu-id="51916-105">최소 지원 Azure Stack 버전은 1811입니다.</span><span class="sxs-lookup"><span data-stu-id="51916-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="51916-106">참고: 이전 버전을 사용하는 경우 1.6.0 버전을 설치하세요.</span><span class="sxs-lookup"><span data-stu-id="51916-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="51916-107">설치</span><span class="sxs-lookup"><span data-stu-id="51916-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a><span data-ttu-id="51916-108">릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="51916-108">Release Notes</span></span>
* <span data-ttu-id="51916-109">1811 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="51916-109">Supported with 1811 update</span></span>
* <span data-ttu-id="51916-110">Azs.Compute.Admin 모듈</span><span class="sxs-lookup"><span data-stu-id="51916-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="51916-111">New-DataDiskObject에 대한 Azs 접두사가 수정되고 향후 사용되지 않을 것이라는 경고와 함께 별칭이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="51916-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="51916-112">Azs.Update.Admin 모듈</span><span class="sxs-lookup"><span data-stu-id="51916-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="51916-113">Install-AzsUpdate 실행 전에 Test-AzureStack에 대해 경고를 추가하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="51916-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="51916-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="51916-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="51916-115">새 cmdlet(기능은 Azure Stack 1811 이상에서 지원됨)</span><span class="sxs-lookup"><span data-stu-id="51916-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="51916-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="51916-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="51916-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="51916-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="51916-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="51916-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="51916-119">사용 중단</span><span class="sxs-lookup"><span data-stu-id="51916-119">Deprecation</span></span>
        * <span data-ttu-id="51916-120">Get-AzsInfrastructureVolume은 이제 Get-AzsVolume cmdlet에 대한 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="51916-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="51916-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="51916-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="51916-122">새 cmdlet Repair-AzsAlert 추가</span><span class="sxs-lookup"><span data-stu-id="51916-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="51916-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="51916-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="51916-124">기본 할당량 값이 사용되지 않는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="51916-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="51916-125">Azs.Subscriptions.Admin 모듈</span><span class="sxs-lookup"><span data-stu-id="51916-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="51916-126">New-AddonPlanDefinitionObject에 대한 Azs 접두사가 수정되고 향후 사용되지 않을 것이라는 경고와 함께 별칭이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="51916-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
