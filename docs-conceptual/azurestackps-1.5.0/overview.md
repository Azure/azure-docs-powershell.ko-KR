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
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153904"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="f7abb-103">Azure Stack 모듈 1.5.0</span><span class="sxs-lookup"><span data-stu-id="f7abb-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="f7abb-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="f7abb-104">Requirements:</span></span>
<span data-ttu-id="f7abb-105">최소 지원 Azure Stack 버전은 1808입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="f7abb-106">참고: 이전 버전을 사용하는 경우 1.4.0 버전을 설치하세요.</span><span class="sxs-lookup"><span data-stu-id="f7abb-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="f7abb-107">알려진 문제:</span><span class="sxs-lookup"><span data-stu-id="f7abb-107">Known issues:</span></span>

- <span data-ttu-id="f7abb-108">New-AzsOffer는 상태를 공개하여 제안을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="f7abb-109">상태를 변경하려면 Set-AzsOffer cmdlet을 나중에 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="f7abb-110">재배포하지 않고는 IP 풀을 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="f7abb-111">설치</span><span class="sxs-lookup"><span data-stu-id="f7abb-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a><span data-ttu-id="f7abb-112">릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="f7abb-112">Release Notes</span></span>
* <span data-ttu-id="f7abb-113">모든 Azure Stack Admin 모듈은 AzureRm.Profile 모듈에 대한 종속성 이상으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="f7abb-114">모든 모듈의 중첩된 리소스 이름 처리에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="f7abb-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="f7abb-115">ErrorActionPreference를 Stop으로 재정의되는 모든 모듈에서 버그 수정</span><span class="sxs-lookup"><span data-stu-id="f7abb-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="f7abb-116">Azs.Compute.Admin 모듈</span><span class="sxs-lookup"><span data-stu-id="f7abb-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="f7abb-117">새 할당량 속성이 추가되어 관리 디스크를 지원</span><span class="sxs-lookup"><span data-stu-id="f7abb-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="f7abb-118">디스크 마이그레이션 관련 cmdlet 또한 추가</span><span class="sxs-lookup"><span data-stu-id="f7abb-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="f7abb-119">플랫폼 이미지 및 VM 확장 개체의 추가 속성</span><span class="sxs-lookup"><span data-stu-id="f7abb-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="f7abb-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="f7abb-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="f7abb-121">배율 단위 노드를 추가하는 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="f7abb-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="f7abb-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="f7abb-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="f7abb-123">Set-AzsBackupShare는 이제 cmdlet Set-AzsBackupConfiguration에 대한 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="f7abb-124">Get-AzsBackupLocation은 이제 cmdlet Get-AzsBackupConfiguration에 대한 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="f7abb-125">Set-AzsBackupConfiguration, BackupShare 매개 변수는 이제 매개 변수 경로에 대한 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="f7abb-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="f7abb-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="f7abb-127">Get-AzsDelegatedProviderOffer, OfferName 매개 변수는 이제 제안에 대한 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="f7abb-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="f7abb-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="f7abb-129">Get-AzsDelegatedProviderOffer, OfferName 매개 변수는 이제 제안에 대한 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="f7abb-130">콘텐츠:</span><span class="sxs-lookup"><span data-stu-id="f7abb-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="f7abb-131">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="f7abb-131">Azure Bridge</span></span>
<span data-ttu-id="f7abb-132">Azure의 이미지를 배포할 수 있게 해주는 Azure Stack AzureBridge 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="f7abb-133">Backup</span><span class="sxs-lookup"><span data-stu-id="f7abb-133">Backup</span></span>
<span data-ttu-id="f7abb-134">관리자가 다음을 수행할 수 있도록 해주는 Backup 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="f7abb-135">백업이 저장되는 위치 구성</span><span class="sxs-lookup"><span data-stu-id="f7abb-135">Configure where backups are stored</span></span>
- <span data-ttu-id="f7abb-136">백업 수행</span><span class="sxs-lookup"><span data-stu-id="f7abb-136">Perform backups</span></span>
- <span data-ttu-id="f7abb-137">완료된 백업 나열 및 복원</span><span class="sxs-lookup"><span data-stu-id="f7abb-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="f7abb-138">상거래</span><span class="sxs-lookup"><span data-stu-id="f7abb-138">Commerce</span></span>
<span data-ttu-id="f7abb-139">Azure Stack 시스템의 집계 데이터 사용량을 볼 수 있는 방법을 제공하는 Azure Stack Commerce 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="f7abb-140">컴퓨팅</span><span class="sxs-lookup"><span data-stu-id="f7abb-140">Compute</span></span>
<span data-ttu-id="f7abb-141">컴퓨팅 할당량, 플랫폼 이미지, 관리 디스크 및 가상 머신 확장을 관리하는 기능을 제공하는 Azure Stack Compute 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="f7abb-142">Fabric</span><span class="sxs-lookup"><span data-stu-id="f7abb-142">Fabric</span></span>
<span data-ttu-id="f7abb-143">관리자가 다음 작업을 위해 인프라 구성 요소를 보고 관리할 수 있게 해주는 Azure Stack Fabric 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="f7abb-144">배율 단위 노드의 중지, 시작 및 종료</span><span class="sxs-lookup"><span data-stu-id="f7abb-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="f7abb-145">FRU 관련 활동에 대한 배율 단위 노드의 배출 및 재개</span><span class="sxs-lookup"><span data-stu-id="f7abb-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="f7abb-146">배율 단위 노드의 복구</span><span class="sxs-lookup"><span data-stu-id="f7abb-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="f7abb-147">인프라 역할의 다시 시작</span><span class="sxs-lookup"><span data-stu-id="f7abb-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="f7abb-148">인프라 역할 인스턴스의 중지, 시작 및 종료</span><span class="sxs-lookup"><span data-stu-id="f7abb-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="f7abb-149">새 IP 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="f7abb-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="f7abb-150">갤러리</span><span class="sxs-lookup"><span data-stu-id="f7abb-150">Gallery</span></span>
<span data-ttu-id="f7abb-151">Azure Stack Marketplace에서 갤러리 항목을 관리하는 기능을 제공하는 Azure Stack Gallery 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="f7abb-152">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="f7abb-152">Infrastructure Insights</span></span>
<span data-ttu-id="f7abb-153">관리자가 다음을 수행할 수 있는 Infrastructure Insight 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="f7abb-154">Azure Stack 스탬프 리소스의 상태 보기</span><span class="sxs-lookup"><span data-stu-id="f7abb-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="f7abb-155">경고 보기 및 관리</span><span class="sxs-lookup"><span data-stu-id="f7abb-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="f7abb-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f7abb-156">KeyVault</span></span>
<span data-ttu-id="f7abb-157">관리자가 KeyVault 할당량을 볼 수 있는 Azure Stack KeyVault 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="f7abb-158">네트워크</span><span class="sxs-lookup"><span data-stu-id="f7abb-158">Network</span></span>
<span data-ttu-id="f7abb-159">다음을 수행할 수 있는 Network 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="f7abb-160">네트워크 할당량 관리</span><span class="sxs-lookup"><span data-stu-id="f7abb-160">Management of network quotas</span></span>
- <span data-ttu-id="f7abb-161">공용 IP 주소, 가상 네트워크, 부하 분산 장치와 같은 할당된 네트워크 리소스 보기</span><span class="sxs-lookup"><span data-stu-id="f7abb-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="f7abb-162">관리자 개요를 표시하는 cmdlet을 제공</span><span class="sxs-lookup"><span data-stu-id="f7abb-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="f7abb-163">스토리지</span><span class="sxs-lookup"><span data-stu-id="f7abb-163">Storage</span></span>
<span data-ttu-id="f7abb-164">Azure Stack Storage 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="f7abb-165">이 릴리스에서는 다음을 수행하기 위한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="f7abb-166">스토리지 할당량 관리</span><span class="sxs-lookup"><span data-stu-id="f7abb-166">Manage storage quotas</span></span>
- <span data-ttu-id="f7abb-167">삭제된 스토리지 리소스 가비지 수집</span><span class="sxs-lookup"><span data-stu-id="f7abb-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="f7abb-168">삭제된 스토리지 계정 복원</span><span class="sxs-lookup"><span data-stu-id="f7abb-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="f7abb-169">한 공유에서 다른 공유로 컨테이너 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="f7abb-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="f7abb-170">개별 스토리지 구성 요소에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="f7abb-170">View information about the individual storage components</span></span>
- <span data-ttu-id="f7abb-171">사용량 및 성능 정보 보기</span><span class="sxs-lookup"><span data-stu-id="f7abb-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="f7abb-172">구독 관리자</span><span class="sxs-lookup"><span data-stu-id="f7abb-172">Subscription Admin</span></span>
<span data-ttu-id="f7abb-173">Azure Stack Subscription 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="f7abb-174">이 모듈은 관리자가 다음을 수행하기 위한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="f7abb-175">계획 및 제안 관리</span><span class="sxs-lookup"><span data-stu-id="f7abb-175">Manage plans and offers</span></span>
- <span data-ttu-id="f7abb-176">사용량 및 성능 정보 보기</span><span class="sxs-lookup"><span data-stu-id="f7abb-176">View usage and performance information</span></span>
- <span data-ttu-id="f7abb-177">RBAC 관리</span><span class="sxs-lookup"><span data-stu-id="f7abb-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="f7abb-178">구독</span><span class="sxs-lookup"><span data-stu-id="f7abb-178">Subscription</span></span>
<span data-ttu-id="f7abb-179">Azure Stack Subscription 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="f7abb-180">이 모듈은 사용자가 다음을 수행하기 위한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="f7abb-181">구독 생성, 삭제 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="f7abb-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="f7abb-182">주 지역에서</span><span class="sxs-lookup"><span data-stu-id="f7abb-182">Update</span></span>
<span data-ttu-id="f7abb-183">Azure Stack Update 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="f7abb-184">이 모듈에서 관리자는 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7abb-184">In this module administrators can:</span></span>
- <span data-ttu-id="f7abb-185">사용 가능한 업데이트 나열 및 설치</span><span class="sxs-lookup"><span data-stu-id="f7abb-185">List and install available updates</span></span>
- <span data-ttu-id="f7abb-186">중단된 업데이트 다시 시작</span><span class="sxs-lookup"><span data-stu-id="f7abb-186">Resume interrupted updates</span></span>
- <span data-ttu-id="f7abb-187">설치된 업데이트 보기</span><span class="sxs-lookup"><span data-stu-id="f7abb-187">View installed updates</span></span>
