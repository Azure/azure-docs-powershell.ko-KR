---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 98a24c805fbf43dd899119d43301b4261c1f60dc
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/16/2019
ms.locfileid: "75035764"
---
## <a name="280---october-2019"></a><span data-ttu-id="eadbe-103">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="eadbe-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="eadbe-104">일반</span><span class="sxs-lookup"><span data-stu-id="eadbe-104">General</span></span>
* <span data-ttu-id="eadbe-105">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="eadbe-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="eadbe-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-106">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-107">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="eadbe-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eadbe-108">Az.ApiManagement</span></span>
* <span data-ttu-id="eadbe-109">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="eadbe-110">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eadbe-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-111">Az.Automation</span></span>
* <span data-ttu-id="eadbe-112">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="eadbe-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="eadbe-113">Az.Batch</span></span>
* <span data-ttu-id="eadbe-114">**Get-AzBatchNodeAgentSku**가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-115">Az.Compute</span></span>
* <span data-ttu-id="eadbe-116">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="eadbe-117">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="eadbe-118">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="eadbe-119">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eadbe-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eadbe-120">Az.DataFactory</span></span>
* <span data-ttu-id="eadbe-121">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="eadbe-122">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="eadbe-123">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="eadbe-125">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="eadbe-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="eadbe-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="eadbe-127">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="eadbe-128">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="eadbe-129">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="eadbe-130">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="eadbe-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-131">Az.IotHub</span></span>
* <span data-ttu-id="eadbe-132">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="eadbe-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="eadbe-133">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="eadbe-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eadbe-134">Az.Monitor</span></span>
* <span data-ttu-id="eadbe-135">New-AzActionGroupReceiver에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="eadbe-136">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="eadbe-137">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="eadbe-138">웹후크는 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-139">Az.Network</span></span>
* <span data-ttu-id="eadbe-140">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="eadbe-141">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="eadbe-142">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-142">New cmdlets added:</span></span>
        - <span data-ttu-id="eadbe-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="eadbe-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="eadbe-144">선택적 매개 변수 -TrafficSelectorPolicies를 사용하여 cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="eadbe-145">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-145">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="eadbe-146">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-146">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="eadbe-147">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-147">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="eadbe-148">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-148">Updated cmdlets:</span></span>
        - <span data-ttu-id="eadbe-149">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-149">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="eadbe-150">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-150">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="eadbe-151">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-151">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="eadbe-152">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-152">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="eadbe-153">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="eadbe-153">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="eadbe-154">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-154">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="eadbe-155">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-155">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="eadbe-156">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="eadbe-156">Az.RedisCache</span></span>
* <span data-ttu-id="eadbe-157">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-157">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-158">Az.Sql</span></span>
* <span data-ttu-id="eadbe-159">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-159">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-160">Az.Storage</span></span>
* <span data-ttu-id="eadbe-161">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-161">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="eadbe-162">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-162">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="eadbe-163">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eadbe-163">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="eadbe-164">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-164">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="eadbe-165">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eadbe-165">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="eadbe-166">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="eadbe-166">Az.StorageSync</span></span>
* <span data-ttu-id="eadbe-167">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-167">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-168">Az.Websites</span></span>
* <span data-ttu-id="eadbe-169">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-169">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="eadbe-170">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="eadbe-170">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="eadbe-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eadbe-171">Az.ApiManagement</span></span>
* <span data-ttu-id="eadbe-172">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-172">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="eadbe-173">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-173">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="eadbe-174">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-174">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eadbe-175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-175">Az.Automation</span></span>
* <span data-ttu-id="eadbe-176">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-176">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="eadbe-177">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-177">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="eadbe-178">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-178">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-179">Az.Compute</span></span>
* <span data-ttu-id="eadbe-180">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-180">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="eadbe-181">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-181">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="eadbe-182">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-182">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="eadbe-183">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-183">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="eadbe-184">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-184">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="eadbe-185">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-185">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="eadbe-186">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-186">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="eadbe-187">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-187">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="eadbe-188">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-188">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eadbe-189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eadbe-189">Az.DataFactory</span></span>
* <span data-ttu-id="eadbe-190">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-190">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="eadbe-191">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-191">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="eadbe-192">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="eadbe-192">Az.HDInsight</span></span>
* <span data-ttu-id="eadbe-193">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="eadbe-193">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="eadbe-194">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-194">Az.IotHub</span></span>
* <span data-ttu-id="eadbe-195">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-195">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="eadbe-196">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-196">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="eadbe-197">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-197">New cmdlets are:</span></span>
    - <span data-ttu-id="eadbe-198">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="eadbe-198">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="eadbe-199">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="eadbe-199">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="eadbe-200">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="eadbe-200">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="eadbe-201">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="eadbe-201">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="eadbe-202">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eadbe-202">Az.Monitor</span></span>
* <span data-ttu-id="eadbe-203">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-203">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="eadbe-204">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-204">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="eadbe-205">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-205">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="eadbe-206">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-206">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="eadbe-207">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-207">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="eadbe-208">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-208">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="eadbe-209">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-209">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="eadbe-210">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-210">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="eadbe-211">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-211">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="eadbe-212">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="eadbe-213">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-213">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="eadbe-214">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-214">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="eadbe-215">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-215">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="eadbe-216">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-216">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="eadbe-217">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-217">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="eadbe-218">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="eadbe-218">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="eadbe-219">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-219">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="eadbe-220">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="eadbe-220">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="eadbe-221">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-221">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="eadbe-222">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-222">Overall improved help files</span></span>
* <span data-ttu-id="eadbe-223">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-223">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-224">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-224">Az.Network</span></span>
* <span data-ttu-id="eadbe-225">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-225">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="eadbe-226">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-226">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="eadbe-227">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-227">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="eadbe-228">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-228">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="eadbe-229">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-229">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="eadbe-230">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-230">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="eadbe-231">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-231">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="eadbe-232">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-232">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="eadbe-233">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-233">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="eadbe-234">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-234">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="eadbe-235">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-235">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="eadbe-236">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-236">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="eadbe-237">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-237">New cmdlets</span></span>
        - <span data-ttu-id="eadbe-238">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="eadbe-238">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="eadbe-239">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-239">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="eadbe-240">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="eadbe-240">Updated cmdlet:</span></span>
        - <span data-ttu-id="eadbe-241">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="eadbe-241">New-VpnSite</span></span>
        - <span data-ttu-id="eadbe-242">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="eadbe-242">Update-VpnSite</span></span>
        - <span data-ttu-id="eadbe-243">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-243">New-VpnConnection</span></span>
        - <span data-ttu-id="eadbe-244">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-244">Update-VpnConnection</span></span>
* <span data-ttu-id="eadbe-245">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-245">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="eadbe-247">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-247">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="eadbe-248">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-248">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-249">Az.Resources</span></span>
* <span data-ttu-id="eadbe-250">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-250">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="eadbe-251">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eadbe-251">Az.ServiceFabric</span></span>
* <span data-ttu-id="eadbe-252">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-252">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="eadbe-253">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-253">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="eadbe-254">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="eadbe-254">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="eadbe-255">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="eadbe-255">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="eadbe-256">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="eadbe-256">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="eadbe-257">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="eadbe-257">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="eadbe-258">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="eadbe-258">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="eadbe-259">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="eadbe-259">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="eadbe-260">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="eadbe-260">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="eadbe-261">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="eadbe-261">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="eadbe-262">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="eadbe-262">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="eadbe-263">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="eadbe-263">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="eadbe-264">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="eadbe-264">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="eadbe-265">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="eadbe-265">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="eadbe-266">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="eadbe-266">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="eadbe-267">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-267">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="eadbe-268">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="eadbe-268">Az.SignalR</span></span>
* <span data-ttu-id="eadbe-269">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-269">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-270">Az.Sql</span></span>
* <span data-ttu-id="eadbe-271">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-271">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="eadbe-272">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="eadbe-272">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="eadbe-273">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-273">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="eadbe-274">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-274">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="eadbe-275">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="eadbe-275">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-276">Az.Storage</span></span>
* <span data-ttu-id="eadbe-277">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-277">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="eadbe-278">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-278">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="eadbe-279">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="eadbe-279">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="eadbe-280">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="eadbe-280">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="eadbe-281">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-281">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="eadbe-282">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="eadbe-282">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="eadbe-283">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-283">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="eadbe-284">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="eadbe-284">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="eadbe-285">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="eadbe-285">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="eadbe-286">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="eadbe-286">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="eadbe-287">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="eadbe-287">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-288">Az.Websites</span></span>
* <span data-ttu-id="eadbe-289">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 문제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-289">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="eadbe-290">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-290">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="eadbe-291">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-291">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="eadbe-292">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="eadbe-292">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="eadbe-293">일반</span><span class="sxs-lookup"><span data-stu-id="eadbe-293">General</span></span>
* <span data-ttu-id="eadbe-294">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-294">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="eadbe-295">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-295">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-296">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="eadbe-296">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="eadbe-297">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="eadbe-297">Az.Aks</span></span>
* <span data-ttu-id="eadbe-298">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-298">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="eadbe-299">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-299">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="eadbe-300">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eadbe-300">Az.ApiManagement</span></span>
* <span data-ttu-id="eadbe-301">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-301">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="eadbe-302">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-302">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="eadbe-303">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-303">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="eadbe-304">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-304">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="eadbe-305">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-305">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="eadbe-306">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="eadbe-306">Az.Batch</span></span>
* <span data-ttu-id="eadbe-307">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-307">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="eadbe-308">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="eadbe-308">Az.Cdn</span></span>
* <span data-ttu-id="eadbe-309">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-309">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-310">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-310">Az.Compute</span></span>
* <span data-ttu-id="eadbe-311">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-311">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="eadbe-312">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-312">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="eadbe-313">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-313">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="eadbe-314">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-314">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="eadbe-315">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="eadbe-315">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="eadbe-316">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-316">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="eadbe-317">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-317">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="eadbe-318">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-318">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eadbe-319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eadbe-319">Az.DataFactory</span></span>
* <span data-ttu-id="eadbe-320">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-320">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="eadbe-321">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-321">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="eadbe-322">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-322">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="eadbe-323">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-323">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-324">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-324">Az.DataLakeStore</span></span>
* <span data-ttu-id="eadbe-325">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-325">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="eadbe-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-326">Az.EventHub</span></span>
* <span data-ttu-id="eadbe-327">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="eadbe-327">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="eadbe-328">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-328">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="eadbe-329">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-329">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="eadbe-330">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="eadbe-330">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="eadbe-331">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="eadbe-331">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="eadbe-332">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-332">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="eadbe-333">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eadbe-333">Az.Monitor</span></span>
* <span data-ttu-id="eadbe-334">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-334">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-335">Az.Network</span></span>
* <span data-ttu-id="eadbe-336">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-336">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="eadbe-337">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="eadbe-337">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="eadbe-338">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-338">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="eadbe-339">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-339">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="eadbe-340">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-340">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="eadbe-341">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-341">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="eadbe-342">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-342">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="eadbe-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="eadbe-344">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-344">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="eadbe-345">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-345">Added example</span></span>
    - <span data-ttu-id="eadbe-346">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-346">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="eadbe-347">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-347">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="eadbe-348">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-348">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-349">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-349">Az.RecoveryServices</span></span>
* <span data-ttu-id="eadbe-350">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-350">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-351">Az.Resources</span></span>
* <span data-ttu-id="eadbe-352">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-352">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="eadbe-353">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-353">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="eadbe-354">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-354">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="eadbe-355">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-355">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="eadbe-356">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eadbe-356">Az.ServiceBus</span></span>
* <span data-ttu-id="eadbe-357">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="eadbe-357">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="eadbe-358">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="eadbe-358">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="eadbe-359">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-359">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="eadbe-360">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eadbe-360">Az.ServiceFabric</span></span>
* <span data-ttu-id="eadbe-361">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="eadbe-361">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="eadbe-362">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="eadbe-362">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="eadbe-363">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="eadbe-363">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="eadbe-364">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-364">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="eadbe-365">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="eadbe-365">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="eadbe-366">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="eadbe-366">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-367">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-367">Az.Sql</span></span>
* <span data-ttu-id="eadbe-368">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-368">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-369">Az.Storage</span></span>
* <span data-ttu-id="eadbe-370">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-370">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="eadbe-371">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-371">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="eadbe-372">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="eadbe-372">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="eadbe-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="eadbe-373">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="eadbe-374">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-374">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="eadbe-375">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="eadbe-375">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-376">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-376">Az.Websites</span></span>
* <span data-ttu-id="eadbe-377">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-377">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="eadbe-378">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="eadbe-378">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eadbe-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-379">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-380">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-380">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="eadbe-381">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-381">Az.ApplicationInsights</span></span>
* <span data-ttu-id="eadbe-382">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-382">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="eadbe-383">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-383">Az.Automation</span></span>
* <span data-ttu-id="eadbe-384">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-384">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="eadbe-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="eadbe-386">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-386">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-387">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-387">Az.Compute</span></span>
* <span data-ttu-id="eadbe-388">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-388">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="eadbe-389">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eadbe-389">Az.ContainerRegistry</span></span>
* <span data-ttu-id="eadbe-390">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-390">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="eadbe-391">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-391">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eadbe-392">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eadbe-392">Az.DataFactory</span></span>
* <span data-ttu-id="eadbe-393">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-393">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="eadbe-394">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-394">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="eadbe-395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-395">Az.EventHub</span></span>
* <span data-ttu-id="eadbe-396">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="eadbe-396">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="eadbe-397">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-397">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="eadbe-398">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eadbe-398">Az.KeyVault</span></span>
* <span data-ttu-id="eadbe-399">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-399">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="eadbe-400">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eadbe-400">Az.LogicApp</span></span>
* <span data-ttu-id="eadbe-401">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-401">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="eadbe-402">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-402">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="eadbe-403">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-403">Az.ManagedServices</span></span>
* <span data-ttu-id="eadbe-404">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-404">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-405">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-405">Az.Network</span></span>
* <span data-ttu-id="eadbe-406">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-406">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="eadbe-407">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-407">New cmdlets</span></span>
        - <span data-ttu-id="eadbe-408">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="eadbe-408">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="eadbe-409">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="eadbe-409">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="eadbe-410">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-410">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="eadbe-411">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-411">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="eadbe-412">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-412">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="eadbe-413">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-413">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="eadbe-414">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="eadbe-414">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="eadbe-415">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="eadbe-415">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="eadbe-416">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="eadbe-416">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="eadbe-417">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-417">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="eadbe-418">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-418">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="eadbe-419">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-419">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="eadbe-420">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-420">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="eadbe-421">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="eadbe-421">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="eadbe-422">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-422">Updated cmdlets</span></span>
        - <span data-ttu-id="eadbe-423">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-423">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="eadbe-424">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-424">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="eadbe-425">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-425">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="eadbe-426">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-426">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="eadbe-427">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-427">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="eadbe-428">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="eadbe-428">Updated cmdlet:</span></span>
        - <span data-ttu-id="eadbe-429">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-429">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="eadbe-430">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-430">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="eadbe-431">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-431">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="eadbe-432">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-432">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="eadbe-433">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-433">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="eadbe-434">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-434">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="eadbe-435">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-435">Az.OperationalInsights</span></span>
* <span data-ttu-id="eadbe-436">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-436">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="eadbe-437">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-437">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="eadbe-439">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-439">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="eadbe-440">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-440">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="eadbe-441">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-441">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="eadbe-442">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-442">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="eadbe-443">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-443">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="eadbe-444">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-444">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="eadbe-445">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-445">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="eadbe-446">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-446">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="eadbe-447">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-447">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="eadbe-448">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-448">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-449">Az.Resources</span></span>
- <span data-ttu-id="eadbe-450">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="eadbe-450">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="eadbe-451">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-451">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="eadbe-452">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eadbe-452">Az.ServiceBus</span></span>
* <span data-ttu-id="eadbe-453">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="eadbe-453">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="eadbe-454">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-454">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-455">Az.Sql</span></span>
* <span data-ttu-id="eadbe-456">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-456">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="eadbe-457">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-457">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="eadbe-458">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-458">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-459">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-459">Az.Storage</span></span>
* <span data-ttu-id="eadbe-460">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="eadbe-460">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="eadbe-461">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="eadbe-461">Az.StorageSync</span></span>
* <span data-ttu-id="eadbe-462">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-462">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="eadbe-463">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-463">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-464">Az.Websites</span></span>
* <span data-ttu-id="eadbe-465">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-465">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="eadbe-466">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-466">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="eadbe-467">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-467">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="eadbe-468">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="eadbe-468">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eadbe-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-469">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-470">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-470">Add support for profile cmdlets</span></span>
* <span data-ttu-id="eadbe-471">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-471">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="eadbe-472">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-472">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="eadbe-473">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="eadbe-473">Az.Advisor</span></span>
* <span data-ttu-id="eadbe-474">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="eadbe-474">GA release of Az.Advisor</span></span>
* <span data-ttu-id="eadbe-475">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-475">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="eadbe-476">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eadbe-476">Az.ApiManagement</span></span>
* <span data-ttu-id="eadbe-477">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-477">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="eadbe-478">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="eadbe-478">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="eadbe-479">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-479">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="eadbe-480">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-480">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="eadbe-481">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-481">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="eadbe-482">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="eadbe-482">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="eadbe-483">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-483">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eadbe-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-484">Az.Automation</span></span>
* <span data-ttu-id="eadbe-485">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-485">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-486">Az.Compute</span></span>
* <span data-ttu-id="eadbe-487">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-487">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eadbe-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eadbe-488">Az.DataFactory</span></span>
* <span data-ttu-id="eadbe-489">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-489">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="eadbe-490">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="eadbe-490">Az.EventGrid</span></span>
* <span data-ttu-id="eadbe-491">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-491">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="eadbe-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-492">Az.IotHub</span></span>
* <span data-ttu-id="eadbe-493">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-493">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-494">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-494">Az.Network</span></span>
* <span data-ttu-id="eadbe-495">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="eadbe-495">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="eadbe-496">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="eadbe-496">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="eadbe-497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-497">Az.PolicyInsights</span></span>
* <span data-ttu-id="eadbe-498">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="eadbe-498">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="eadbe-499">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-499">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="eadbe-500">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-500">Az.OperationalInsights</span></span>
* <span data-ttu-id="eadbe-501">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-501">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-502">Az.RecoveryServices</span></span>
* <span data-ttu-id="eadbe-503">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-503">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-504">Az.Resources</span></span>
    - <span data-ttu-id="eadbe-505">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-505">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="eadbe-506">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-506">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="eadbe-507">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-507">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="eadbe-508">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-508">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="eadbe-509">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eadbe-509">Az.ServiceBus</span></span>
* <span data-ttu-id="eadbe-510">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="eadbe-510">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-511">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-511">Az.Sql</span></span>
* <span data-ttu-id="eadbe-512">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-512">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="eadbe-513">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-513">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="eadbe-514">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="eadbe-514">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="eadbe-515">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="eadbe-515">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="eadbe-516">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="eadbe-516">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="eadbe-517">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="eadbe-517">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="eadbe-518">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="eadbe-518">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="eadbe-519">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="eadbe-519">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="eadbe-520">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="eadbe-520">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-521">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-521">Az.Storage</span></span>
* <span data-ttu-id="eadbe-522">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-522">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="eadbe-523">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="eadbe-523">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="eadbe-524">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-524">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="eadbe-525">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="eadbe-525">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="eadbe-526">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-526">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="eadbe-527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eadbe-527">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="eadbe-528">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eadbe-528">Set-AzStorageAccount</span></span>
* <span data-ttu-id="eadbe-529">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="eadbe-529">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="eadbe-530">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="eadbe-530">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="eadbe-531">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="eadbe-531">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="eadbe-532">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="eadbe-532">Az.StorageSync</span></span>
* <span data-ttu-id="eadbe-533">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-533">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="eadbe-534">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="eadbe-534">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eadbe-535">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-535">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-536">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-536">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="eadbe-537">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-537">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="eadbe-538">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="eadbe-538">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="eadbe-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="eadbe-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="eadbe-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="eadbe-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-541">Az.Compute</span></span>
* <span data-ttu-id="eadbe-542">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-542">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="eadbe-543">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-543">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="eadbe-544">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="eadbe-544">Az.Dns</span></span>
* <span data-ttu-id="eadbe-545">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-545">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="eadbe-546">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="eadbe-546">Az.EventGrid</span></span>
* <span data-ttu-id="eadbe-547">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-547">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="eadbe-548">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="eadbe-548">New cmdlets:</span></span>
    - <span data-ttu-id="eadbe-549">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="eadbe-549">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="eadbe-550">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-550">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="eadbe-551">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="eadbe-551">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="eadbe-552">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-552">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="eadbe-553">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="eadbe-553">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="eadbe-554">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-554">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="eadbe-555">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="eadbe-555">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="eadbe-556">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-556">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="eadbe-557">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="eadbe-557">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="eadbe-558">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-558">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="eadbe-559">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="eadbe-559">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="eadbe-560">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-560">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="eadbe-561">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="eadbe-561">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="eadbe-562">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-562">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="eadbe-563">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="eadbe-563">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="eadbe-564">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-564">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="eadbe-565">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-565">Updated cmdlets:</span></span>
    - <span data-ttu-id="eadbe-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="eadbe-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="eadbe-567">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-567">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="eadbe-568">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-568">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="eadbe-569">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-569">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="eadbe-570">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-570">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="eadbe-571">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="eadbe-571">Event subscription expiration date,</span></span>
            - <span data-ttu-id="eadbe-572">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="eadbe-572">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="eadbe-573">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-573">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="eadbe-574">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="eadbe-574">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="eadbe-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="eadbe-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="eadbe-576">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-576">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="eadbe-577">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="eadbe-577">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="eadbe-578">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-578">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="eadbe-579">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-579">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="eadbe-580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="eadbe-580">Az.FrontDoor</span></span>
* <span data-ttu-id="eadbe-581">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="eadbe-581">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="eadbe-582">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-582">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="eadbe-583">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="eadbe-583">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="eadbe-584">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-584">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-585">Az.Network</span></span>
* <span data-ttu-id="eadbe-586">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-586">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="eadbe-587">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-587">New cmdlets</span></span>
        - <span data-ttu-id="eadbe-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="eadbe-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="eadbe-589">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-589">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="eadbe-590">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-590">New cmdlets</span></span> 
        - <span data-ttu-id="eadbe-591">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="eadbe-591">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="eadbe-592">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-592">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="eadbe-593">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-593">New cmdlets</span></span> 
        - <span data-ttu-id="eadbe-594">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="eadbe-594">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="eadbe-595">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="eadbe-595">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="eadbe-596">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="eadbe-596">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="eadbe-597">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-597">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="eadbe-598">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-598">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="eadbe-599">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-599">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="eadbe-600">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-600">New cmdlets</span></span>
        - <span data-ttu-id="eadbe-601">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="eadbe-601">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="eadbe-602">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="eadbe-602">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="eadbe-603">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="eadbe-603">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="eadbe-604">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="eadbe-604">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="eadbe-605">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="eadbe-605">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="eadbe-606">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-606">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="eadbe-607">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-607">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="eadbe-608">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-608">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="eadbe-609">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-609">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="eadbe-610">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-610">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="eadbe-611">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-611">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="eadbe-612">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-612">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="eadbe-613">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-613">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="eadbe-614">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-614">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="eadbe-615">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-615">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="eadbe-616">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-616">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="eadbe-617">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-617">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="eadbe-618">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-618">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="eadbe-619">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="eadbe-619">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="eadbe-620">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-620">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="eadbe-621">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-621">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="eadbe-622">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="eadbe-622">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="eadbe-623">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="eadbe-623">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="eadbe-624">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-624">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="eadbe-625">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-625">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="eadbe-626">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-626">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="eadbe-627">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-627">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="eadbe-628">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-628">Az.OperationalInsights</span></span>
* <span data-ttu-id="eadbe-629">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="eadbe-629">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-630">Az.Resources</span></span>
* <span data-ttu-id="eadbe-631">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-631">Support for additional Template Export options</span></span>
    - <span data-ttu-id="eadbe-632">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-632">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="eadbe-633">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-633">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="eadbe-634">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-634">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="eadbe-635">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eadbe-635">Az.ServiceFabric</span></span>
* <span data-ttu-id="eadbe-636">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-636">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-637">Az.Sql</span></span>
* <span data-ttu-id="eadbe-638">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-638">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="eadbe-639">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-639">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="eadbe-640">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-640">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="eadbe-641">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eadbe-641">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="eadbe-642">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eadbe-642">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="eadbe-643">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="eadbe-643">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="eadbe-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="eadbe-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="eadbe-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="eadbe-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-646">Az.Storage</span></span>
* <span data-ttu-id="eadbe-647">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-647">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="eadbe-648">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eadbe-648">New-AzStorageAccount</span></span>
* <span data-ttu-id="eadbe-649">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="eadbe-649">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="eadbe-650">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="eadbe-650">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-651">Az.Websites</span></span>
* <span data-ttu-id="eadbe-652">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="eadbe-652">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="eadbe-653">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-653">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="eadbe-654">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="eadbe-654">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="eadbe-655">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="eadbe-655">Az.Cdn</span></span>
* <span data-ttu-id="eadbe-656">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-656">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-657">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-657">Az.Compute</span></span>
* <span data-ttu-id="eadbe-658">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-658">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="eadbe-659">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="eadbe-659">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="eadbe-660">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-660">Az.EventHub</span></span>
* <span data-ttu-id="eadbe-661">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="eadbe-661">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="eadbe-662">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="eadbe-662">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-663">Az.Network</span></span>
* <span data-ttu-id="eadbe-664">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-664">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="eadbe-665">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-665">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="eadbe-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="eadbe-667">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="eadbe-667">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-668">Az.RecoveryServices</span></span>
* <span data-ttu-id="eadbe-669">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-669">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="eadbe-670">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eadbe-670">Az.ServiceBus</span></span>
* <span data-ttu-id="eadbe-671">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="eadbe-671">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="eadbe-672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eadbe-672">Az.ServiceFabric</span></span>
* <span data-ttu-id="eadbe-673">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-673">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="eadbe-674">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-674">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-675">Az.Sql</span></span>
* <span data-ttu-id="eadbe-676">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-676">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="eadbe-677">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="eadbe-677">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="eadbe-678">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="eadbe-678">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="eadbe-679">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-679">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-680">Az.Websites</span></span>
* <span data-ttu-id="eadbe-681">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="eadbe-681">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="eadbe-682">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="eadbe-682">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="eadbe-683">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eadbe-683">Az.ApiManagement</span></span>
* <span data-ttu-id="eadbe-684">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-684">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="eadbe-685">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="eadbe-685">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="eadbe-686">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="eadbe-686">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="eadbe-687">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="eadbe-687">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="eadbe-688">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="eadbe-688">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="eadbe-689">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="eadbe-689">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="eadbe-690">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="eadbe-690">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="eadbe-691">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-691">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="eadbe-692">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-692">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="eadbe-693">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="eadbe-693">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="eadbe-694">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="eadbe-694">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="eadbe-695">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="eadbe-695">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="eadbe-696">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-696">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="eadbe-697">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-697">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="eadbe-698">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="eadbe-698">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="eadbe-699">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="eadbe-699">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="eadbe-700">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="eadbe-700">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="eadbe-701">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-701">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="eadbe-702">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-702">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="eadbe-703">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-703">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="eadbe-704">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-704">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="eadbe-705">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-705">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="eadbe-706">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-706">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="eadbe-707">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-707">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="eadbe-708">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-708">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="eadbe-709">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-709">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="eadbe-710">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-710">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="eadbe-711">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-711">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="eadbe-712">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-712">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="eadbe-713">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-713">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="eadbe-714">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-714">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="eadbe-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="eadbe-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="eadbe-716">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-716">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="eadbe-717">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-717">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="eadbe-718">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="eadbe-718">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="eadbe-719">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="eadbe-719">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="eadbe-720">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="eadbe-720">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="eadbe-721">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-721">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="eadbe-722">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-722">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="eadbe-723">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-723">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="eadbe-724">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="eadbe-724">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="eadbe-725">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="eadbe-725">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="eadbe-726">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="eadbe-726">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="eadbe-727">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="eadbe-727">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="eadbe-728">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-728">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="eadbe-729">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="eadbe-729">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="eadbe-730">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-730">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="eadbe-731">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="eadbe-731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="eadbe-732">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-732">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="eadbe-733">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="eadbe-733">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="eadbe-734">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-734">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="eadbe-735">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="eadbe-735">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="eadbe-736">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="eadbe-736">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="eadbe-737">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-737">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="eadbe-738">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="eadbe-738">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="eadbe-739">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="eadbe-739">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="eadbe-740">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-740">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="eadbe-741">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="eadbe-741">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="eadbe-742">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="eadbe-742">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="eadbe-743">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-743">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="eadbe-744">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-744">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="eadbe-745">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="eadbe-745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="eadbe-746">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="eadbe-746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="eadbe-747">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="eadbe-748">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="eadbe-748">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="eadbe-749">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="eadbe-749">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="eadbe-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="eadbe-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="eadbe-751">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="eadbe-751">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="eadbe-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="eadbe-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="eadbe-753">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="eadbe-753">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="eadbe-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="eadbe-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="eadbe-755">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="eadbe-755">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="eadbe-756">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="eadbe-756">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="eadbe-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="eadbe-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="eadbe-758">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="eadbe-758">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="eadbe-759">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="eadbe-759">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="eadbe-760">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="eadbe-760">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eadbe-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-761">Az.Automation</span></span>
* <span data-ttu-id="eadbe-762">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-762">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="eadbe-763">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-763">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="eadbe-764">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="eadbe-765">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-765">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="eadbe-766">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-766">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="eadbe-767">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="eadbe-767">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="eadbe-768">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-768">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-769">Az.Compute</span></span>
* <span data-ttu-id="eadbe-770">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-770">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="eadbe-771">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-771">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-772">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-772">Az.DataLakeStore</span></span>
* <span data-ttu-id="eadbe-773">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-773">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="eadbe-774">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eadbe-774">Az.Monitor</span></span>
* <span data-ttu-id="eadbe-775">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-775">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-776">Az.Network</span></span>
* <span data-ttu-id="eadbe-777">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-777">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="eadbe-778">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="eadbe-778">Updated cmdlet:</span></span>
        - <span data-ttu-id="eadbe-779">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="eadbe-779">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="eadbe-780">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-780">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-781">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-781">Az.Resources</span></span>
* <span data-ttu-id="eadbe-782">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-782">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-783">Az.Sql</span></span>
* <span data-ttu-id="eadbe-784">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-784">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="eadbe-785">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="eadbe-785">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eadbe-786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-786">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-787">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-787">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="eadbe-788">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-788">Az.CognitiveServices</span></span>
* <span data-ttu-id="eadbe-789">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-789">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="eadbe-790">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="eadbe-790">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-791">Az.Compute</span></span>
* <span data-ttu-id="eadbe-792">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="eadbe-792">Proximity placement group feature.</span></span>
    - <span data-ttu-id="eadbe-793">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="eadbe-793">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="eadbe-794">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-794">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="eadbe-795">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-795">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="eadbe-796">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-796">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="eadbe-797">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-797">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="eadbe-798">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="eadbe-798">Breaking changes</span></span>
    - <span data-ttu-id="eadbe-799">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-799">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="eadbe-800">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-800">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="eadbe-801">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="eadbe-801">Az.DeploymentManager</span></span>
* <span data-ttu-id="eadbe-802">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="eadbe-802">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="eadbe-803">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="eadbe-803">Az.Dns</span></span>
* <span data-ttu-id="eadbe-804">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="eadbe-804">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="eadbe-805">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-805">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="eadbe-806">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-806">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="eadbe-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="eadbe-807">Az.FrontDoor</span></span>
* <span data-ttu-id="eadbe-808">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="eadbe-808">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="eadbe-809">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="eadbe-809">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="eadbe-810">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="eadbe-810">Az.HDInsight</span></span>
* <span data-ttu-id="eadbe-811">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-811">Removed two cmdlets:</span></span>
    - <span data-ttu-id="eadbe-812">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="eadbe-812">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="eadbe-813">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="eadbe-813">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="eadbe-814">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-814">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="eadbe-815">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="eadbe-815">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="eadbe-816">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-816">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="eadbe-817">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-817">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="eadbe-818">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eadbe-818">Az.Monitor</span></span>
* <span data-ttu-id="eadbe-819">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-819">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="eadbe-820">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="eadbe-820">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="eadbe-821">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="eadbe-821">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="eadbe-822">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="eadbe-822">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="eadbe-823">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="eadbe-823">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="eadbe-824">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="eadbe-824">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="eadbe-825">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="eadbe-825">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="eadbe-826">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="eadbe-826">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="eadbe-827">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="eadbe-827">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="eadbe-828">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="eadbe-828">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="eadbe-829">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="eadbe-829">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="eadbe-830">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="eadbe-830">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="eadbe-831">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="eadbe-831">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="eadbe-832">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-832">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-833">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-833">Az.Network</span></span>
* <span data-ttu-id="eadbe-834">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-834">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="eadbe-835">새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-835">New cmdlets</span></span>
        - <span data-ttu-id="eadbe-836">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="eadbe-836">New-AzNatGateway</span></span>
        - <span data-ttu-id="eadbe-837">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="eadbe-837">Get-AzNatGateway</span></span>
        - <span data-ttu-id="eadbe-838">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="eadbe-838">Set-AzNatGateway</span></span>
        - <span data-ttu-id="eadbe-839">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="eadbe-839">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="eadbe-840">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-840">Updated cmdlets</span></span>
        - <span data-ttu-id="eadbe-841">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="eadbe-841">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="eadbe-842">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="eadbe-842">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="eadbe-843">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="eadbe-843">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="eadbe-844">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-844">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="eadbe-845">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-845">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="eadbe-846">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-846">Az.PolicyInsights</span></span>
* <span data-ttu-id="eadbe-847">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-847">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="eadbe-848">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-848">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="eadbe-849">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-849">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-850">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-850">Az.RecoveryServices</span></span>
* <span data-ttu-id="eadbe-851">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-851">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="eadbe-852">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="eadbe-852">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="eadbe-853">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-853">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="eadbe-854">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-854">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="eadbe-855">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-855">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="eadbe-856">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="eadbe-856">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="eadbe-857">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="eadbe-857">Az.Relay</span></span>
* <span data-ttu-id="eadbe-858">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-858">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="eadbe-859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eadbe-859">Az.ServiceBus</span></span>
* <span data-ttu-id="eadbe-860">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="eadbe-860">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-861">Az.Storage</span></span>
* <span data-ttu-id="eadbe-862">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="eadbe-862">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="eadbe-863">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-863">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="eadbe-864">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-864">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="eadbe-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eadbe-865">New-AzStorageAccount</span></span>
* <span data-ttu-id="eadbe-866">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-866">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="eadbe-867">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eadbe-867">New-AzStorageAccount</span></span>
    - <span data-ttu-id="eadbe-868">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eadbe-868">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="eadbe-869">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eadbe-869">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-870">Az.Websites</span></span>
* <span data-ttu-id="eadbe-871">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-871">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="eadbe-872">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-872">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="eadbe-873">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="eadbe-873">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="eadbe-874">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="eadbe-874">Highlights since the last major release</span></span>
* <span data-ttu-id="eadbe-875">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="eadbe-875">General availability of `Az` module</span></span>
* <span data-ttu-id="eadbe-876">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-876">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="eadbe-877">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="eadbe-877">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="eadbe-878">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-878">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="eadbe-879">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-879">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="eadbe-880">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-880">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="eadbe-881">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-881">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="eadbe-882">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-882">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-883">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-883">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="eadbe-884">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="eadbe-884">Az.Batch</span></span>
* <span data-ttu-id="eadbe-885">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="eadbe-886">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="eadbe-886">Az.Cdn</span></span>
* <span data-ttu-id="eadbe-887">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="eadbe-888">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-888">Az.CognitiveServices</span></span>
* <span data-ttu-id="eadbe-889">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-890">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-890">Az.Compute</span></span>
* <span data-ttu-id="eadbe-891">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-891">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="eadbe-892">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="eadbe-893">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-893">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eadbe-894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eadbe-894">Az.DataFactory</span></span>
* <span data-ttu-id="eadbe-895">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-895">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-896">Az.DataLakeStore</span></span>
* <span data-ttu-id="eadbe-897">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="eadbe-898">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="eadbe-898">Az.EventGrid</span></span>
* <span data-ttu-id="eadbe-899">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-899">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="eadbe-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-900">Az.EventHub</span></span>
* <span data-ttu-id="eadbe-901">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="eadbe-901">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="eadbe-902">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="eadbe-902">Az.HDInsight</span></span>
* <span data-ttu-id="eadbe-903">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="eadbe-904">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-904">Az.IotHub</span></span>
* <span data-ttu-id="eadbe-905">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="eadbe-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eadbe-906">Az.KeyVault</span></span>
* <span data-ttu-id="eadbe-907">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="eadbe-908">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-908">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="eadbe-909">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="eadbe-909">Az.MachineLearning</span></span>
* <span data-ttu-id="eadbe-910">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="eadbe-911">Az.Media</span><span class="sxs-lookup"><span data-stu-id="eadbe-911">Az.Media</span></span>
* <span data-ttu-id="eadbe-912">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-912">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="eadbe-913">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eadbe-913">Az.Monitor</span></span>
  * <span data-ttu-id="eadbe-914">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-914">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="eadbe-915">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="eadbe-915">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="eadbe-916">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="eadbe-916">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="eadbe-917">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="eadbe-917">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="eadbe-918">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="eadbe-918">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="eadbe-919">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="eadbe-919">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="eadbe-920">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-920">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-921">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-921">Az.Network</span></span>
* <span data-ttu-id="eadbe-922">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-922">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="eadbe-923">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-923">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="eadbe-924">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="eadbe-924">Az.NotificationHubs</span></span>
* <span data-ttu-id="eadbe-925">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="eadbe-926">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-926">Az.OperationalInsights</span></span>
* <span data-ttu-id="eadbe-927">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="eadbe-928">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="eadbe-928">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="eadbe-929">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-930">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-930">Az.RecoveryServices</span></span>
* <span data-ttu-id="eadbe-931">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="eadbe-932">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-932">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="eadbe-933">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-933">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="eadbe-934">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-934">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="eadbe-935">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="eadbe-935">Az.RedisCache</span></span>
* <span data-ttu-id="eadbe-936">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-937">Az.Resources</span></span>
* <span data-ttu-id="eadbe-938">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-938">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-939">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-939">Az.Sql</span></span>
* <span data-ttu-id="eadbe-940">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-940">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="eadbe-941">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="eadbe-942">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-942">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="eadbe-943">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-943">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="eadbe-944">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-944">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="eadbe-945">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-945">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="eadbe-946">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-946">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-947">Az.Websites</span></span>
* <span data-ttu-id="eadbe-948">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-948">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="eadbe-949">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-949">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="eadbe-950">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-950">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="eadbe-951">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-951">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="eadbe-952">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="eadbe-952">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="eadbe-953">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="eadbe-953">Highlights since the last major release</span></span>
* <span data-ttu-id="eadbe-954">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="eadbe-954">General availability of `Az` module</span></span>
* <span data-ttu-id="eadbe-955">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-955">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="eadbe-956">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="eadbe-956">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="eadbe-957">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-957">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="eadbe-958">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-958">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="eadbe-959">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-959">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="eadbe-960">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-960">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="eadbe-961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-961">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-962">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-962">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="eadbe-963">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-963">Az.AnalysisServices</span></span>
* <span data-ttu-id="eadbe-964">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="eadbe-964">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="eadbe-965">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="eadbe-965">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eadbe-966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-966">Az.Automation</span></span>
* <span data-ttu-id="eadbe-967">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-967">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="eadbe-968">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="eadbe-968">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="eadbe-969">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-969">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-970">Az.Compute</span></span>
* <span data-ttu-id="eadbe-971">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-971">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="eadbe-972">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="eadbe-972">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="eadbe-973">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="eadbe-973">Az.ContainerInstance</span></span>
* <span data-ttu-id="eadbe-974">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-974">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eadbe-975">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eadbe-975">Az.DataFactory</span></span>
* <span data-ttu-id="eadbe-976">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-976">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="eadbe-977">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-977">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-978">Az.Resources</span></span>
* <span data-ttu-id="eadbe-979">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="eadbe-979">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="eadbe-980">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="eadbe-980">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="eadbe-981">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="eadbe-981">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="eadbe-982">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="eadbe-983">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-983">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="eadbe-984">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-984">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-985">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-985">Az.Sql</span></span>
* <span data-ttu-id="eadbe-986">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-986">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-987">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-987">Az.Storage</span></span>
* <span data-ttu-id="eadbe-988">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="eadbe-988">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="eadbe-989">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="eadbe-989">New-AzStorageContext</span></span>
* <span data-ttu-id="eadbe-990">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-990">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="eadbe-991">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="eadbe-991">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="eadbe-992">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="eadbe-992">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="eadbe-993">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="eadbe-993">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="eadbe-994">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="eadbe-994">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="eadbe-995">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-995">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="eadbe-996">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="eadbe-996">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="eadbe-997">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="eadbe-997">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="eadbe-998">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="eadbe-998">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="eadbe-999">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="eadbe-999">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="eadbe-1000">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1000">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="eadbe-1001">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="eadbe-1001">Highlights since the last major release</span></span>
* <span data-ttu-id="eadbe-1002">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="eadbe-1002">General availability of `Az` module</span></span>
* <span data-ttu-id="eadbe-1003">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1003">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="eadbe-1004">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="eadbe-1004">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="eadbe-1005">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1005">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="eadbe-1006">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1006">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="eadbe-1007">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1007">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="eadbe-1008">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1008">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eadbe-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-1009">Az.Automation</span></span>
* <span data-ttu-id="eadbe-1010">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1010">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="eadbe-1011">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="eadbe-1011">Dynamic grouping</span></span>
    * <span data-ttu-id="eadbe-1012">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1012">Pre-Post script</span></span>
    * <span data-ttu-id="eadbe-1013">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1013">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-1014">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1014">Az.Compute</span></span>
* <span data-ttu-id="eadbe-1015">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1015">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="eadbe-1016">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1016">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="eadbe-1017">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eadbe-1017">Az.KeyVault</span></span>
* <span data-ttu-id="eadbe-1018">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1018">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-1019">Az.Network</span></span>
* <span data-ttu-id="eadbe-1020">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1020">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="eadbe-1021">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1021">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-1022">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1022">Az.RecoveryServices</span></span>
* <span data-ttu-id="eadbe-1023">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1023">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="eadbe-1024">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1024">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1025">Az.Resources</span></span>
* <span data-ttu-id="eadbe-1026">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1026">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="eadbe-1027">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1027">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-1028">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-1028">Az.Sql</span></span>
* <span data-ttu-id="eadbe-1029">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1029">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-1030">Az.Storage</span></span>
* <span data-ttu-id="eadbe-1031">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1031">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="eadbe-1032">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="eadbe-1032">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="eadbe-1033">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="eadbe-1033">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="eadbe-1034">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="eadbe-1034">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="eadbe-1035">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="eadbe-1035">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="eadbe-1036">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="eadbe-1036">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="eadbe-1037">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="eadbe-1037">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-1038">Az.Websites</span></span>
* <span data-ttu-id="eadbe-1039">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1039">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="eadbe-1040">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1040">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eadbe-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-1041">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-1042">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-1042">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="eadbe-1043">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1043">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eadbe-1044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-1044">Az.Automation</span></span>
* <span data-ttu-id="eadbe-1045">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1045">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="eadbe-1046">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1046">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="eadbe-1047">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="eadbe-1047">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="eadbe-1048">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="eadbe-1048">Az.Cdn</span></span>
* <span data-ttu-id="eadbe-1049">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1049">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-1050">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1050">Az.Compute</span></span>
* <span data-ttu-id="eadbe-1051">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1051">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eadbe-1052">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eadbe-1052">Az.DataFactory</span></span>
* <span data-ttu-id="eadbe-1053">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1053">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="eadbe-1054">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eadbe-1054">Az.LogicApp</span></span>
* <span data-ttu-id="eadbe-1055">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1055">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-1056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-1056">Az.Network</span></span>
* <span data-ttu-id="eadbe-1057">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1057">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-1058">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1058">Az.RecoveryServices</span></span>
* <span data-ttu-id="eadbe-1059">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1059">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="eadbe-1060">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1060">SDK Update</span></span>
* <span data-ttu-id="eadbe-1061">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="eadbe-1061">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="eadbe-1062">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1062">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1063">Az.Resources</span></span>
* <span data-ttu-id="eadbe-1064">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="eadbe-1064">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="eadbe-1065">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1065">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="eadbe-1066">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1066">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="eadbe-1067">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1067">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="eadbe-1068">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="eadbe-1068">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="eadbe-1069">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1069">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-1070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-1070">Az.Sql</span></span>
* <span data-ttu-id="eadbe-1071">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1071">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="eadbe-1072">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1072">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-1073">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-1073">Az.Storage</span></span>
* <span data-ttu-id="eadbe-1074">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-1074">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="eadbe-1075">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1075">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="eadbe-1076">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1076">Az.AnalysisServices</span></span>
* <span data-ttu-id="eadbe-1077">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1077">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eadbe-1078">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-1078">Az.Automation</span></span>
* <span data-ttu-id="eadbe-1079">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1079">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="eadbe-1080">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1080">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="eadbe-1081">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="eadbe-1081">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="eadbe-1082">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1082">Az.CognitiveServices</span></span>
* <span data-ttu-id="eadbe-1083">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1083">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-1084">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1084">Az.Compute</span></span>
* <span data-ttu-id="eadbe-1085">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="eadbe-1085">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="eadbe-1086">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1086">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="eadbe-1087">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1087">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="eadbe-1088">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1088">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-1089">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-1089">Az.DataLakeStore</span></span>
* <span data-ttu-id="eadbe-1090">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1090">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="eadbe-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-1091">Az.EventHub</span></span>
* <span data-ttu-id="eadbe-1092">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1092">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="eadbe-1093">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eadbe-1093">Az.KeyVault</span></span>
* <span data-ttu-id="eadbe-1094">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1094">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="eadbe-1095">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eadbe-1095">Az.LogicApp</span></span>
* <span data-ttu-id="eadbe-1096">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1096">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="eadbe-1097">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1097">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="eadbe-1098">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1098">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="eadbe-1099">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eadbe-1099">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="eadbe-1100">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eadbe-1100">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="eadbe-1101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eadbe-1101">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="eadbe-1102">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eadbe-1102">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="eadbe-1103">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1103">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="eadbe-1104">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eadbe-1104">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="eadbe-1105">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eadbe-1105">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="eadbe-1106">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eadbe-1106">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="eadbe-1107">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eadbe-1107">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="eadbe-1108">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1108">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="eadbe-1109">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eadbe-1109">Az.Monitor</span></span>
* <span data-ttu-id="eadbe-1110">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1110">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-1111">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-1111">Az.Network</span></span>
* <span data-ttu-id="eadbe-1112">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1112">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="eadbe-1113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-1113">Az.OperationalInsights</span></span>
* <span data-ttu-id="eadbe-1114">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1114">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="eadbe-1115">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1115">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="eadbe-1116">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1116">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="eadbe-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1117">Az.Resources</span></span>
* <span data-ttu-id="eadbe-1118">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="eadbe-1119">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="eadbe-1120">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="eadbe-1121">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1121">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-1122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-1122">Az.Sql</span></span>
* <span data-ttu-id="eadbe-1123">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1123">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="eadbe-1124">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1124">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-1125">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-1125">Az.Websites</span></span>
* <span data-ttu-id="eadbe-1126">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="eadbe-1126">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="eadbe-1127">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1127">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eadbe-1128">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-1128">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-1129">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1129">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="eadbe-1130">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1130">Az.AnalysisServices</span></span>
<span data-ttu-id="eadbe-1131">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1131">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1132">Az.Compute</span></span>
* <span data-ttu-id="eadbe-1133">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1133">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="eadbe-1134">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1134">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="eadbe-1135">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1135">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1136">Az.RecoveryServices</span></span>
<span data-ttu-id="eadbe-1137">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1137">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-1138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1138">Az.Resources</span></span>
* <span data-ttu-id="eadbe-1139">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1139">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="eadbe-1140">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1140">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="eadbe-1141">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1141">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="eadbe-1142">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1142">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-1143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-1143">Az.Sql</span></span>
* <span data-ttu-id="eadbe-1144">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="eadbe-1145">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1145">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="eadbe-1146">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1146">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="eadbe-1147">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1147">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eadbe-1148">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-1148">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-1149">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="eadbe-1149">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="eadbe-1150">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1150">Az.AnalysisServices</span></span>
* <span data-ttu-id="eadbe-1151">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="eadbe-1151">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-1152">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1152">Az.RecoveryServices</span></span>
* <span data-ttu-id="eadbe-1153">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="eadbe-1153">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="eadbe-1154">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1154">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eadbe-1155">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-1155">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-1156">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1156">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="eadbe-1157">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1157">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eadbe-1158">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1158">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="eadbe-1159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="eadbe-1159">Az.Aks</span></span>
* <span data-ttu-id="eadbe-1160">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1160">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eadbe-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-1161">Az.Automation</span></span>
* <span data-ttu-id="eadbe-1162">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1162">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="eadbe-1163">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1163">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="eadbe-1164">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="eadbe-1164">Az.Cdn</span></span>
* <span data-ttu-id="eadbe-1165">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1165">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1166">Az.Compute</span></span>
* <span data-ttu-id="eadbe-1167">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1167">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="eadbe-1168">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1168">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="eadbe-1169">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1169">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="eadbe-1170">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eadbe-1170">Az.ContainerRegistry</span></span>
* <span data-ttu-id="eadbe-1171">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1171">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eadbe-1172">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eadbe-1172">Az.DataFactory</span></span>
* <span data-ttu-id="eadbe-1173">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1173">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-1174">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-1174">Az.DataLakeStore</span></span>
* <span data-ttu-id="eadbe-1175">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1175">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="eadbe-1176">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1176">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="eadbe-1177">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1177">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="eadbe-1178">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-1178">Az.IotHub</span></span>
* <span data-ttu-id="eadbe-1179">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1179">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="eadbe-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eadbe-1180">Az.KeyVault</span></span>
* <span data-ttu-id="eadbe-1181">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1181">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-1182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-1182">Az.Network</span></span>
* <span data-ttu-id="eadbe-1183">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1183">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1184">Az.Resources</span></span>
* <span data-ttu-id="eadbe-1185">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1185">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="eadbe-1186">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1186">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="eadbe-1187">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="eadbe-1187">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="eadbe-1188">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1188">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="eadbe-1189">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="eadbe-1190">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1190">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="eadbe-1191">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1191">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="eadbe-1192">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eadbe-1192">Az.ServiceFabric</span></span>
* <span data-ttu-id="eadbe-1193">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1193">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="eadbe-1194">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1194">Fix some error messages.</span></span>
* <span data-ttu-id="eadbe-1195">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1195">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="eadbe-1196">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1196">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="eadbe-1197">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="eadbe-1197">Az.SignalR</span></span>
* <span data-ttu-id="eadbe-1198">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1198">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-1199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-1199">Az.Sql</span></span>
* <span data-ttu-id="eadbe-1200">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1200">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eadbe-1201">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1201">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="eadbe-1202">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1202">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="eadbe-1203">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-1203">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-1204">Az.Storage</span></span>
* <span data-ttu-id="eadbe-1205">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1205">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eadbe-1206">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1206">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="eadbe-1207">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="eadbe-1207">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="eadbe-1208">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="eadbe-1208">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="eadbe-1209">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="eadbe-1209">Az.TrafficManager</span></span>
* <span data-ttu-id="eadbe-1210">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1210">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-1211">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-1211">Az.Websites</span></span>
* <span data-ttu-id="eadbe-1212">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1212">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eadbe-1213">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1213">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="eadbe-1214">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1214">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="eadbe-1215">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1215">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eadbe-1216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-1216">Az.Accounts</span></span>
* <span data-ttu-id="eadbe-1217">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1217">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-1218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1218">Az.Compute</span></span>
* <span data-ttu-id="eadbe-1219">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1219">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="eadbe-1220">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1220">Updated the description of ID in help files</span></span>
* <span data-ttu-id="eadbe-1221">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1221">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-1222">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-1222">Az.DataLakeStore</span></span>
* <span data-ttu-id="eadbe-1223">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1223">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="eadbe-1224">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1224">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="eadbe-1225">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="eadbe-1225">Az.EventGrid</span></span>
* <span data-ttu-id="eadbe-1226">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1226">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="eadbe-1227">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1227">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="eadbe-1228">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1228">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="eadbe-1229">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="eadbe-1229">Event Time-To-Live,</span></span>
        - <span data-ttu-id="eadbe-1230">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="eadbe-1230">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="eadbe-1231">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1231">Dead letter endpoint.</span></span>
    - <span data-ttu-id="eadbe-1232">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1232">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="eadbe-1233">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="eadbe-1233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="eadbe-1234">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="eadbe-1234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="eadbe-1235">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1235">Dead letter endpoint.</span></span>
* <span data-ttu-id="eadbe-1236">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1236">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="eadbe-1237">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1237">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="eadbe-1238">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="eadbe-1238">Az.IotHub</span></span>
* <span data-ttu-id="eadbe-1239">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-1239">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="eadbe-1240">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eadbe-1240">Az.LogicApp</span></span>
* <span data-ttu-id="eadbe-1241">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="eadbe-1241">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-1242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1242">Az.Resources</span></span>
* <span data-ttu-id="eadbe-1243">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1243">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="eadbe-1244">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1244">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="eadbe-1245">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1245">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="eadbe-1246">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1246">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="eadbe-1247">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-1247">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="eadbe-1248">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1248">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="eadbe-1249">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="eadbe-1249">Az.SignalR</span></span>
* <span data-ttu-id="eadbe-1250">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1250">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-1251">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-1251">Az.Sql</span></span>
* <span data-ttu-id="eadbe-1252">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1252">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eadbe-1253">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-1253">Az.Storage</span></span>
* <span data-ttu-id="eadbe-1254">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1254">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="eadbe-1255">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="eadbe-1255">New-AzStorageContext</span></span>
* <span data-ttu-id="eadbe-1256">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1256">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="eadbe-1257">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="eadbe-1257">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-1258">Az.Websites</span></span>
* <span data-ttu-id="eadbe-1259">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1259">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="eadbe-1260">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1260">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="eadbe-1261">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1261">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="eadbe-1262">일반</span><span class="sxs-lookup"><span data-stu-id="eadbe-1262">General</span></span>

- <span data-ttu-id="eadbe-1263">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="eadbe-1263">General Availability of Az Module</span></span>
- <span data-ttu-id="eadbe-1264">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="eadbe-1264">Online help for each module</span></span>
- <span data-ttu-id="eadbe-1265">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1265">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="eadbe-1266">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1266">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="eadbe-1267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eadbe-1267">Az.Accounts</span></span>
- <span data-ttu-id="eadbe-1268">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="eadbe-1268">Changed from Az.Profile</span></span>
- <span data-ttu-id="eadbe-1269">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1269">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="eadbe-1270">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eadbe-1270">Az.ApiManagement</span></span>
- <span data-ttu-id="eadbe-1271">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1271">Fixes for #7002</span></span>
- <span data-ttu-id="eadbe-1272">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1272">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="eadbe-1273">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="eadbe-1273">Az.Batch</span></span>
- <span data-ttu-id="eadbe-1274">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1274">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="eadbe-1275">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1275">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="eadbe-1276">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="eadbe-1277">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="eadbe-1277">Az.Billing</span></span>
- <span data-ttu-id="eadbe-1278">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1278">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="eadbe-1279">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1279">Az.CognitivServices</span></span>
- <span data-ttu-id="eadbe-1280">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1280">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="eadbe-1281">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="eadbe-1281">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="eadbe-1282">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="eadbe-1282">Az.ContainerInstance</span></span>
- <span data-ttu-id="eadbe-1283">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-1283">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="eadbe-1284">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="eadbe-1284">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="eadbe-1285">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-1286">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-1286">Az.DataLakeStore</span></span>
- <span data-ttu-id="eadbe-1287">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1287">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="eadbe-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eadbe-1288">Az.Monitor</span></span>
- <span data-ttu-id="eadbe-1289">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1289">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="eadbe-1290">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eadbe-1290">Az.KeyVault</span></span>
- <span data-ttu-id="eadbe-1291">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="eadbe-1291">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="eadbe-1292">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="eadbe-1292">Az.MachineLearning</span></span>
- <span data-ttu-id="eadbe-1293">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="eadbe-1293">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="eadbe-1294">Az.Media</span><span class="sxs-lookup"><span data-stu-id="eadbe-1294">Az.Media</span></span>
- <span data-ttu-id="eadbe-1295">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-1295">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="eadbe-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-1296">Az.Network</span></span>
<span data-ttu-id="eadbe-1297">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-1297">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="eadbe-1298">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1298">New cmdlets added:</span></span>
        - <span data-ttu-id="eadbe-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eadbe-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eadbe-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eadbe-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eadbe-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eadbe-1304">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="eadbe-1304">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="eadbe-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="eadbe-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="eadbe-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="eadbe-1307">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1307">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="eadbe-1308">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eadbe-1308">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="eadbe-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eadbe-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="eadbe-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eadbe-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="eadbe-1311">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-1311">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="eadbe-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="eadbe-1313">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="eadbe-1314">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="eadbe-1314">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="eadbe-1315">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="eadbe-1315">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="eadbe-1316">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="eadbe-1316">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="eadbe-1317">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="eadbe-1317">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="eadbe-1318">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="eadbe-1318">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="eadbe-1319">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="eadbe-1320">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-1320">Az.OperationalInsights</span></span>
- <span data-ttu-id="eadbe-1321">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1321">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="eadbe-1322">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="eadbe-1322">Az.Profile</span></span>
- <span data-ttu-id="eadbe-1323">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-1323">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-1324">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1324">Az.RecoveryServices</span></span>
- <span data-ttu-id="eadbe-1325">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="eadbe-1326">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1326">Az.Resources</span></span>
- <span data-ttu-id="eadbe-1327">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1327">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="eadbe-1328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eadbe-1328">Az.ServiceFabric</span></span>
- <span data-ttu-id="eadbe-1329">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-1329">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="eadbe-1330">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1330">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="eadbe-1331">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="eadbe-1331">Az.SIgnalR</span></span>
- <span data-ttu-id="eadbe-1332">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="eadbe-1332">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="eadbe-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-1333">Az.Sql</span></span>
- <span data-ttu-id="eadbe-1334">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1334">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="eadbe-1335">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1335">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="eadbe-1336">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="eadbe-1337">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-1337">Az.Storage</span></span>
- <span data-ttu-id="eadbe-1338">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="eadbe-1339">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-1339">Az.Websites</span></span>
- <span data-ttu-id="eadbe-1340">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="eadbe-1341">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1341">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="eadbe-1342">일반</span><span class="sxs-lookup"><span data-stu-id="eadbe-1342">General</span></span>

* <span data-ttu-id="eadbe-1343">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="eadbe-1343">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="eadbe-1344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1344">Az.Compute</span></span>

* <span data-ttu-id="eadbe-1345">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1345">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-1346">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-1346">Az.DataLakeStore</span></span>

* <span data-ttu-id="eadbe-1347">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1347">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="eadbe-1348">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="eadbe-1348">Az.FrontDoor</span></span>

* <span data-ttu-id="eadbe-1349">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1349">Fixed some broken links</span></span>
    - <span data-ttu-id="eadbe-1350">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1350">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="eadbe-1351">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1351">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="eadbe-1352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1352">Az.RecoveryServices</span></span>

* <span data-ttu-id="eadbe-1353">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1353">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="eadbe-1354">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1354">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="eadbe-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1355">Az.Resources</span></span>

* <span data-ttu-id="eadbe-1356">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="eadbe-1356">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="eadbe-1357">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1357">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="eadbe-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-1358">Az.Sql</span></span>

* <span data-ttu-id="eadbe-1359">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="eadbe-1359">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="eadbe-1360">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="eadbe-1360">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="eadbe-1361">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1361">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="eadbe-1362">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-1362">Az.Storage</span></span>

* <span data-ttu-id="eadbe-1363">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1363">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="eadbe-1364">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1364">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="eadbe-1365">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="eadbe-1365">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="eadbe-1366">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="eadbe-1366">Support Static Website configuration</span></span>
    - <span data-ttu-id="eadbe-1367">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="eadbe-1367">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="eadbe-1368">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="eadbe-1368">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="eadbe-1369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-1369">Az.Websites</span></span>

* <span data-ttu-id="eadbe-1370">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eadbe-1370">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="eadbe-1371">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1371">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="eadbe-1372">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1372">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="eadbe-1373">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1373">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="eadbe-1374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eadbe-1374">Az.ApiManagement</span></span>
* <span data-ttu-id="eadbe-1375">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1375">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="eadbe-1376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eadbe-1376">Az.Automation</span></span>
* <span data-ttu-id="eadbe-1377">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="eadbe-1377">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="eadbe-1378">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1378">Added Update Management cmdlets</span></span>
* <span data-ttu-id="eadbe-1379">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1379">Added Source Control cmdlets</span></span>
* <span data-ttu-id="eadbe-1380">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1380">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="eadbe-1381">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1381">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="eadbe-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1382">Az.Compute</span></span>
* <span data-ttu-id="eadbe-1383">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1383">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="eadbe-1384">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1384">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="eadbe-1385">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="eadbe-1385">Az.ContainerInstance</span></span>
* <span data-ttu-id="eadbe-1386">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1386">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="eadbe-1387">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="eadbe-1387">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="eadbe-1388">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1388">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="eadbe-1389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-1389">Az.Network</span></span>
* <span data-ttu-id="eadbe-1390">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1390">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="eadbe-1391">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1391">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="eadbe-1392">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1392">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="eadbe-1393">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="eadbe-1393">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="eadbe-1394">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="eadbe-1394">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="eadbe-1395">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1395">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="eadbe-1396">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1396">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="eadbe-1397">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="eadbe-1397">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="eadbe-1398">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1398">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="eadbe-1399">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1399">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="eadbe-1400">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="eadbe-1400">Az.Relay</span></span>
* <span data-ttu-id="eadbe-1401">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1401">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="eadbe-1402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1402">Az.Resources</span></span>
* <span data-ttu-id="eadbe-1403">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="eadbe-1403">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="eadbe-1404">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1404">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="eadbe-1405">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="eadbe-1405">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="eadbe-1406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eadbe-1406">Az.ServiceFabric</span></span>
* <span data-ttu-id="eadbe-1407">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1407">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="eadbe-1408">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-1408">Az.Sql</span></span>
* <span data-ttu-id="eadbe-1409">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1409">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="eadbe-1410">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eadbe-1410">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eadbe-1411">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eadbe-1411">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eadbe-1412">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eadbe-1412">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eadbe-1413">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eadbe-1413">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eadbe-1414">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eadbe-1414">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eadbe-1415">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eadbe-1415">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eadbe-1416">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eadbe-1416">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eadbe-1417">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eadbe-1417">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="eadbe-1418">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1418">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="eadbe-1419">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1419">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="eadbe-1420">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1420">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="eadbe-1421">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1421">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="eadbe-1422">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1422">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="eadbe-1423">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1423">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="eadbe-1424">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1424">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="eadbe-1425">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="eadbe-1425">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="eadbe-1426">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1426">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="eadbe-1427">일반</span><span class="sxs-lookup"><span data-stu-id="eadbe-1427">General</span></span>
* <span data-ttu-id="eadbe-1428">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1428">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="eadbe-1429">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="eadbe-1429">Az.Profile</span></span>
* <span data-ttu-id="eadbe-1430">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1430">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="eadbe-1431">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="eadbe-1431">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="eadbe-1432">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="eadbe-1432">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="eadbe-1433">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1433">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="eadbe-1434">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1434">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="eadbe-1435">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1435">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="eadbe-1436">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1436">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="eadbe-1437">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1437">Az.CognitiveServices</span></span>
* <span data-ttu-id="eadbe-1438">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1438">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-1439">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1439">Az.Compute</span></span>
* <span data-ttu-id="eadbe-1440">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="eadbe-1440">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="eadbe-1441">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="eadbe-1441">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="eadbe-1442">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1442">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="eadbe-1444">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1444">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="eadbe-1445">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1445">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="eadbe-1446">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="eadbe-1446">Az.Insights</span></span>
* <span data-ttu-id="eadbe-1447">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="eadbe-1447">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="eadbe-1448">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="eadbe-1448">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="eadbe-1449">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="eadbe-1449">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="eadbe-1450">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="eadbe-1450">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-1451">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-1451">Az.Network</span></span>
* <span data-ttu-id="eadbe-1452">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1452">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="eadbe-1453">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="eadbe-1453">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="eadbe-1454">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="eadbe-1454">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="eadbe-1455">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eadbe-1455">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="eadbe-1456">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="eadbe-1456">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="eadbe-1457">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="eadbe-1457">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="eadbe-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eadbe-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="eadbe-1459">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="eadbe-1459">Az.PolicyInsights</span></span>
* <span data-ttu-id="eadbe-1460">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="eadbe-1460">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-1461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1461">Az.Resources</span></span>
* <span data-ttu-id="eadbe-1462">에 대 한 수정 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="eadbe-1462">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="eadbe-1463">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="eadbe-1463">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="eadbe-1464">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eadbe-1464">Az.ServiceBus</span></span>
* <span data-ttu-id="eadbe-1465">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1465">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="eadbe-1466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eadbe-1466">Az.ServiceFabric</span></span>
* <span data-ttu-id="eadbe-1467">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1467">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="eadbe-1468">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1468">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="eadbe-1469">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1469">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="eadbe-1470">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="eadbe-1470">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="eadbe-1471">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1471">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="eadbe-1472">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1472">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="eadbe-1473">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="eadbe-1473">Az.Profile</span></span>
* <span data-ttu-id="eadbe-1474">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1474">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="eadbe-1475">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1475">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-1476">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1476">Az.Compute</span></span>
* <span data-ttu-id="eadbe-1477">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1477">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="eadbe-1478">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1478">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eadbe-1479">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eadbe-1479">Az.DataLakeStore</span></span>
* <span data-ttu-id="eadbe-1480">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1480">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="eadbe-1481">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1481">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="eadbe-1482">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="eadbe-1483">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="eadbe-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-1485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-1485">Az.Network</span></span>
* <span data-ttu-id="eadbe-1486">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1486">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="eadbe-1487">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1487">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-1488">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1488">Az.Resources</span></span>
* <span data-ttu-id="eadbe-1489">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1489">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="eadbe-1490">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1490">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="eadbe-1491">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1491">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="eadbe-1492">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="eadbe-1492">Azure.Storage</span></span>
* <span data-ttu-id="eadbe-1493">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1493">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="eadbe-1494">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="eadbe-1494">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="eadbe-1495">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="eadbe-1495">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="eadbe-1496">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1496">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="eadbe-1497">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="eadbe-1497">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="eadbe-1498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eadbe-1498">Az.CognitiveServices</span></span>
* <span data-ttu-id="eadbe-1499">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1499">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eadbe-1500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eadbe-1500">Az.Compute</span></span>
* <span data-ttu-id="eadbe-1501">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1501">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="eadbe-1502">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="eadbe-1502">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="eadbe-1503">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1503">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="eadbe-1504">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eadbe-1504">Az.DataFactoryV2</span></span>
* <span data-ttu-id="eadbe-1505">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="eadbe-1505">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eadbe-1506">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eadbe-1506">Az.Network</span></span>
* <span data-ttu-id="eadbe-1507">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1507">Added NetworkProfile functionality.</span></span> <span data-ttu-id="eadbe-1508">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1508">new cmdlets added</span></span>
    - <span data-ttu-id="eadbe-1509">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eadbe-1509">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="eadbe-1510">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eadbe-1510">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="eadbe-1511">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eadbe-1511">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="eadbe-1512">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eadbe-1512">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="eadbe-1513">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-1513">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="eadbe-1514">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="eadbe-1514">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="eadbe-1515">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1515">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="eadbe-1516">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1516">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="eadbe-1517">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1517">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="eadbe-1518">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="eadbe-1518">Az.RedisCache</span></span>
* <span data-ttu-id="eadbe-1519">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="eadbe-1519">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="eadbe-1520">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1520">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="eadbe-1521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eadbe-1521">Az.Resources</span></span>
* <span data-ttu-id="eadbe-1522">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="eadbe-1522">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="eadbe-1523">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="eadbe-1523">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="eadbe-1524">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eadbe-1524">Az.Sql</span></span>
* <span data-ttu-id="eadbe-1525">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="eadbe-1525">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eadbe-1526">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eadbe-1526">Az.Websites</span></span>
* <span data-ttu-id="eadbe-1527">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1527">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="eadbe-1528">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="eadbe-1528">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="eadbe-1529">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="eadbe-1529">0.2.0 - September 2018</span></span>
 <span data-ttu-id="eadbe-1530">최초 릴리스</span><span class="sxs-lookup"><span data-stu-id="eadbe-1530">Initial Release</span></span>
