---
title: Azure Stack PowerShell 개요 | Microsoft Docs
description: 설치 및 구성에 대한 설명을 포함한 Azure Stack PowerShell 개요입니다.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 55f19ac5e6767df1312e0b531184e8621b60a011
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "67038196"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="684cf-103">AzureRM 모듈 2.5.0</span><span class="sxs-lookup"><span data-stu-id="684cf-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="684cf-104">요구 사항:</span><span class="sxs-lookup"><span data-stu-id="684cf-104">Requirements:</span></span>
<span data-ttu-id="684cf-105">지원되는 최소 Azure Stack 버전은 1904입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="684cf-106">참고: 이전 버전을 사용하는 경우 1.2.11 버전을 설치하세요.</span><span class="sxs-lookup"><span data-stu-id="684cf-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="684cf-107">설치</span><span class="sxs-lookup"><span data-stu-id="684cf-107">Install</span></span>
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a><span data-ttu-id="684cf-108">릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="684cf-108">Release Notes</span></span>
* <span data-ttu-id="684cf-109">AzureRm.Resources</span><span class="sxs-lookup"><span data-stu-id="684cf-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="684cf-110">2019-03-01-hybrid 프로필로 2018-05-01 API 버전을 지원하는 새로운 리소스 모듈</span><span class="sxs-lookup"><span data-stu-id="684cf-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="684cf-111">PolicyDefinition(2016-12-01) 및 PolicyAssisgment(2017-06-01-preview) 작업은 여전히 이전 API 버전으로 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="684cf-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="684cf-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="684cf-113">2017-12-01 API 버전을 지원하는 새로운 컴퓨팅 모듈.'</span><span class="sxs-lookup"><span data-stu-id="684cf-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="684cf-114">이 릴리스는 azurestack 특정 API 프로필 2019-03-01-hybrid에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="684cf-115">모든 모듈은 AzureRm.Profile 모듈에 대한 종속성 이상으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="684cf-116">각 모듈이 지원하는 api 버전이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="684cf-117">컴퓨팅 - 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="684cf-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="684cf-118">네트워크 - 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="684cf-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="684cf-119">스토리지 - 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="684cf-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="684cf-120">리소스 - 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="684cf-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="684cf-121">Keyvault - 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="684cf-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="684cf-122">Dns - 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="684cf-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="684cf-123">각 리소스 종류에 대한 전체 API 버전 맵은 https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json 에서 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="684cf-124">콘텐츠:</span><span class="sxs-lookup"><span data-stu-id="684cf-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="684cf-125">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="684cf-125">Azure Bridge</span></span>
<span data-ttu-id="684cf-126">Azure의 이미지를 배포할 수 있게 해주는 Azure Stack AzureBridge 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="684cf-127">Backup</span><span class="sxs-lookup"><span data-stu-id="684cf-127">Backup</span></span>
<span data-ttu-id="684cf-128">관리자가 다음을 수행할 수 있도록 해주는 Backup 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="684cf-129">백업이 저장되는 위치 구성</span><span class="sxs-lookup"><span data-stu-id="684cf-129">Configure where backups are stored</span></span>
- <span data-ttu-id="684cf-130">백업 수행</span><span class="sxs-lookup"><span data-stu-id="684cf-130">Perform backups</span></span>
- <span data-ttu-id="684cf-131">완료된 백업 나열 및 복원</span><span class="sxs-lookup"><span data-stu-id="684cf-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="684cf-132">상거래</span><span class="sxs-lookup"><span data-stu-id="684cf-132">Commerce</span></span>
<span data-ttu-id="684cf-133">Azure Stack 시스템의 집계 데이터 사용량을 볼 수 있는 방법을 제공하는 Azure Stack Commerce 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="684cf-134">컴퓨팅</span><span class="sxs-lookup"><span data-stu-id="684cf-134">Compute</span></span>
<span data-ttu-id="684cf-135">컴퓨팅 할당량, 플랫폼 이미지, 관리 디스크 및 가상 머신 확장을 관리하는 기능을 제공하는 Azure Stack Compute 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="684cf-136">Fabric</span><span class="sxs-lookup"><span data-stu-id="684cf-136">Fabric</span></span>
<span data-ttu-id="684cf-137">관리자가 다음 작업을 위해 인프라 구성 요소를 보고 관리할 수 있게 해주는 Azure Stack Fabric 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="684cf-138">배율 단위 노드의 중지, 시작 및 종료</span><span class="sxs-lookup"><span data-stu-id="684cf-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="684cf-139">FRU 관련 활동에 대한 배율 단위 노드의 배출 및 재개</span><span class="sxs-lookup"><span data-stu-id="684cf-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="684cf-140">배율 단위 노드의 복구</span><span class="sxs-lookup"><span data-stu-id="684cf-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="684cf-141">인프라 역할의 다시 시작</span><span class="sxs-lookup"><span data-stu-id="684cf-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="684cf-142">인프라 역할 인스턴스의 중지, 시작 및 종료</span><span class="sxs-lookup"><span data-stu-id="684cf-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="684cf-143">새 IP 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="684cf-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="684cf-144">갤러리</span><span class="sxs-lookup"><span data-stu-id="684cf-144">Gallery</span></span>
<span data-ttu-id="684cf-145">Azure Stack Marketplace에서 갤러리 항목을 관리하는 기능을 제공하는 Azure Stack Gallery 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="684cf-146">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="684cf-146">Infrastructure Insights</span></span>
<span data-ttu-id="684cf-147">관리자가 다음을 수행할 수 있는 Infrastructure Insight 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="684cf-148">Azure Stack 스탬프 리소스의 상태 보기</span><span class="sxs-lookup"><span data-stu-id="684cf-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="684cf-149">경고 보기 및 관리</span><span class="sxs-lookup"><span data-stu-id="684cf-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="684cf-150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="684cf-150">KeyVault</span></span>
<span data-ttu-id="684cf-151">관리자가 KeyVault 할당량을 볼 수 있는 Azure Stack KeyVault 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="684cf-152">네트워크</span><span class="sxs-lookup"><span data-stu-id="684cf-152">Network</span></span>
<span data-ttu-id="684cf-153">다음을 수행할 수 있는 Network 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="684cf-154">네트워크 할당량 관리</span><span class="sxs-lookup"><span data-stu-id="684cf-154">Management of network quotas</span></span>
- <span data-ttu-id="684cf-155">공용 IP 주소, 가상 네트워크, 부하 분산 장치와 같은 할당된 네트워크 리소스 보기</span><span class="sxs-lookup"><span data-stu-id="684cf-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="684cf-156">관리자 개요를 표시하는 cmdlet을 제공</span><span class="sxs-lookup"><span data-stu-id="684cf-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="684cf-157">스토리지</span><span class="sxs-lookup"><span data-stu-id="684cf-157">Storage</span></span>
<span data-ttu-id="684cf-158">Azure Stack Storage 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="684cf-159">이 릴리스에서는 다음을 수행하기 위한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="684cf-160">스토리지 할당량 관리</span><span class="sxs-lookup"><span data-stu-id="684cf-160">Manage storage quotas</span></span>
- <span data-ttu-id="684cf-161">삭제된 스토리지 리소스 가비지 수집</span><span class="sxs-lookup"><span data-stu-id="684cf-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="684cf-162">삭제된 스토리지 계정 복원</span><span class="sxs-lookup"><span data-stu-id="684cf-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="684cf-163">한 공유에서 다른 공유로 컨테이너 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="684cf-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="684cf-164">개별 스토리지 구성 요소에 대한 정보 보기</span><span class="sxs-lookup"><span data-stu-id="684cf-164">View information about the individual storage components</span></span>
- <span data-ttu-id="684cf-165">사용량 및 성능 정보 보기</span><span class="sxs-lookup"><span data-stu-id="684cf-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="684cf-166">구독 관리자</span><span class="sxs-lookup"><span data-stu-id="684cf-166">Subscription Admin</span></span>
<span data-ttu-id="684cf-167">Azure Stack Subscription 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="684cf-168">이 모듈은 관리자가 다음을 수행하기 위한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="684cf-169">계획 및 제안 관리</span><span class="sxs-lookup"><span data-stu-id="684cf-169">Manage plans and offers</span></span>
- <span data-ttu-id="684cf-170">사용량 및 성능 정보 보기</span><span class="sxs-lookup"><span data-stu-id="684cf-170">View usage and performance information</span></span>
- <span data-ttu-id="684cf-171">RBAC 관리</span><span class="sxs-lookup"><span data-stu-id="684cf-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="684cf-172">Subscription</span><span class="sxs-lookup"><span data-stu-id="684cf-172">Subscription</span></span>
<span data-ttu-id="684cf-173">Azure Stack Subscription 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="684cf-174">이 모듈은 사용자가 다음을 수행하기 위한 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="684cf-175">구독 생성, 삭제 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="684cf-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="684cf-176">업데이트</span><span class="sxs-lookup"><span data-stu-id="684cf-176">Update</span></span>
<span data-ttu-id="684cf-177">Azure Stack Update 관리자 모듈의 미리 보기 릴리스입니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="684cf-178">이 모듈에서 관리자는 다음을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="684cf-178">In this module administrators can:</span></span>
- <span data-ttu-id="684cf-179">사용 가능한 업데이트 나열 및 설치</span><span class="sxs-lookup"><span data-stu-id="684cf-179">List and install available updates</span></span>
- <span data-ttu-id="684cf-180">중단된 업데이트 다시 시작</span><span class="sxs-lookup"><span data-stu-id="684cf-180">Resume interrupted updates</span></span>
- <span data-ttu-id="684cf-181">설치된 업데이트 보기</span><span class="sxs-lookup"><span data-stu-id="684cf-181">View installed updates</span></span>
