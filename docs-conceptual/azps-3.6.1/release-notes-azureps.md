---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: f24e5ef66f9c49976c550c9847903bd0608c5123
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/11/2020
ms.locfileid: "79111035"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="d521f-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="d521f-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="d521f-104">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="d521f-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-105">Az.Accounts</span></span>
* <span data-ttu-id="d521f-106">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="d521f-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="d521f-107">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="d521f-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="d521f-108">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d521f-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d521f-109">Az.ApiManagement</span></span>
* <span data-ttu-id="d521f-110">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="d521f-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="d521f-111">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="d521f-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="d521f-112">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="d521f-113">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="d521f-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-115">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d521f-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d521f-116">Az.IotHub</span></span>
* <span data-ttu-id="d521f-117">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="d521f-118">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="d521f-119">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d521f-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d521f-120">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d521f-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d521f-121">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d521f-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d521f-122">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d521f-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="d521f-123">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="d521f-124">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="d521f-125">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="d521f-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="d521f-126">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="d521f-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="d521f-127">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="d521f-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="d521f-128">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="d521f-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="d521f-129">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="d521f-130">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="d521f-131">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="d521f-132">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="d521f-133">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="d521f-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="d521f-134">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="d521f-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="d521f-135">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d521f-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-136">Az.Monitor</span></span>
* <span data-ttu-id="d521f-137">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="d521f-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-138">Az.Network</span></span>
* <span data-ttu-id="d521f-139">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="d521f-140">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="d521f-141">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="d521f-142">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-143">Az.Resources</span></span>
* <span data-ttu-id="d521f-144">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="d521f-145">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="d521f-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="d521f-146">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="d521f-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="d521f-147">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="d521f-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="d521f-148">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="d521f-149">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="d521f-150">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="d521f-151">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="d521f-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d521f-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="d521f-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d521f-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="d521f-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d521f-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="d521f-155">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="d521f-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d521f-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="d521f-157">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-157">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-158">Az.Sql</span></span>
* <span data-ttu-id="d521f-159">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="d521f-160">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="d521f-161">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-161">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="d521f-162">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="d521f-163">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-163">Remove an LTR backup</span></span>
    - <span data-ttu-id="d521f-164">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="d521f-165">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="d521f-166">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="d521f-167">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-168">Az.Storage</span></span>
* <span data-ttu-id="d521f-169">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="d521f-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="d521f-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="d521f-171">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="d521f-172">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="d521f-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="d521f-173">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="d521f-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-174">Az.Websites</span></span>
* <span data-ttu-id="d521f-175">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="d521f-176">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="d521f-177">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="d521f-178">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="d521f-179">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="d521f-180">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="d521f-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d521f-181">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="d521f-181">Highlights since the last major release</span></span>
* <span data-ttu-id="d521f-182">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="d521f-183">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="d521f-184">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d521f-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-185">Az.Accounts</span></span>
* <span data-ttu-id="d521f-186">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-187">Az.Automation</span></span>
* <span data-ttu-id="d521f-188">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d521f-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d521f-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="d521f-190">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="d521f-191">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-192">Az.Compute</span></span>
* <span data-ttu-id="d521f-193">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d521f-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d521f-194">Az.FrontDoor</span></span>
* <span data-ttu-id="d521f-195">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d521f-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d521f-196">Az.IotHub</span></span>
* <span data-ttu-id="d521f-197">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="d521f-198">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="d521f-199">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d521f-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d521f-200">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d521f-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d521f-201">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d521f-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d521f-202">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d521f-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d521f-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d521f-203">Az.KeyVault</span></span>
* <span data-ttu-id="d521f-204">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d521f-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-205">Az.Monitor</span></span>
* <span data-ttu-id="d521f-206">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="d521f-207">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="d521f-208">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-209">Az.Network</span></span>
* <span data-ttu-id="d521f-210">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="d521f-211">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="d521f-212">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="d521f-213">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="d521f-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="d521f-214">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-214">No new cmdlets are added.</span></span> <span data-ttu-id="d521f-215">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-217">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-218">Az.Resources</span></span>
* <span data-ttu-id="d521f-219">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="d521f-220">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="d521f-221">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="d521f-222">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="d521f-223">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="d521f-224">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="d521f-225">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="d521f-226">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-227">Az.Sql</span></span>
* <span data-ttu-id="d521f-228">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="d521f-229">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="d521f-230">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d521f-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d521f-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d521f-232">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d521f-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d521f-233">Az.StorageSync</span></span>
* <span data-ttu-id="d521f-234">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="d521f-235">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="d521f-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d521f-236">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="d521f-236">Highlights since the last major release</span></span>
* <span data-ttu-id="d521f-237">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="d521f-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="d521f-238">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d521f-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-239">Az.Accounts</span></span>
* <span data-ttu-id="d521f-240">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="d521f-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="d521f-241">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d521f-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d521f-242">Az.ApiManagement</span></span>
* <span data-ttu-id="d521f-243">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="d521f-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="d521f-244">**New-AzApiManagementProduct**\* 및 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="d521f-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="d521f-245">https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="d521f-246">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-247">Az.Compute</span></span>
* <span data-ttu-id="d521f-248">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="d521f-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="d521f-249">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="d521f-250">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="d521f-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="d521f-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="d521f-252">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-253">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-254">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d521f-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d521f-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="d521f-256">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="d521f-257">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d521f-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d521f-258">Az.HDInsight</span></span>
* <span data-ttu-id="d521f-259">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d521f-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d521f-260">Az.KeyVault</span></span>
* <span data-ttu-id="d521f-261">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-262">Az.Network</span></span>
* <span data-ttu-id="d521f-263">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="d521f-264">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="d521f-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="d521f-265">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="d521f-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d521f-266">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="d521f-267">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="d521f-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="d521f-268">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="d521f-269">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="d521f-270">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="d521f-271">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-271">New cmdlets added:</span></span>
        - <span data-ttu-id="d521f-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d521f-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="d521f-273">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d521f-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="d521f-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d521f-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="d521f-275">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d521f-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="d521f-277">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="d521f-278">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="d521f-279">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="d521f-280">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-282">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="d521f-283">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-284">Az.Resources</span></span>
* <span data-ttu-id="d521f-285">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="d521f-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="d521f-286">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-287">Az.Sql</span></span>
<span data-ttu-id="d521f-288">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-289">Az.Storage</span></span>
* <span data-ttu-id="d521f-290">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="d521f-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="d521f-292">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="d521f-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="d521f-293">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-294">Az.Websites</span></span>
* <span data-ttu-id="d521f-295">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="d521f-296">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="d521f-297">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="d521f-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-298">Az.Accounts</span></span>
* <span data-ttu-id="d521f-299">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d521f-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d521f-300">Az.Cdn</span></span>
* <span data-ttu-id="d521f-301">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="d521f-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-302">Az.Compute</span></span>
* <span data-ttu-id="d521f-303">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d521f-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d521f-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="d521f-305">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="d521f-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d521f-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d521f-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d521f-307">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d521f-308">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="d521f-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="d521f-309">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d521f-310">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="d521f-311">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d521f-312">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="d521f-313">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d521f-314">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="d521f-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="d521f-315">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d521f-316">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="d521f-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="d521f-317">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d521f-318">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="d521f-319">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d521f-320">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="d521f-321">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="d521f-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="d521f-322">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="d521f-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="d521f-323">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="d521f-324">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="d521f-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-325">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-326">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="d521f-327">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="d521f-328">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="d521f-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="d521f-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="d521f-330">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d521f-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d521f-331">Az.EventHub</span></span>
* <span data-ttu-id="d521f-332">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d521f-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d521f-333">Az.HDInsight</span></span>
* <span data-ttu-id="d521f-334">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d521f-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d521f-335">Az.MachineLearning</span></span>
* <span data-ttu-id="d521f-336">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="d521f-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d521f-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="d521f-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="d521f-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="d521f-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d521f-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="d521f-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d521f-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="d521f-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d521f-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="d521f-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="d521f-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="d521f-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="d521f-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-344">Az.Network</span></span>
* <span data-ttu-id="d521f-345">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="d521f-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-347">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="d521f-348">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d521f-349">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d521f-350">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-351">Az.Resources</span></span>
* <span data-ttu-id="d521f-352">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-353">Az.Sql</span></span>
* <span data-ttu-id="d521f-354">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="d521f-355">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d521f-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d521f-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d521f-357">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-358">Az.Storage</span></span>
* <span data-ttu-id="d521f-359">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="d521f-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d521f-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="d521f-361">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="d521f-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="d521f-363">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="d521f-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="d521f-364">일반</span><span class="sxs-lookup"><span data-stu-id="d521f-364">General</span></span>
* <span data-ttu-id="d521f-365">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d521f-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-366">Az.Accounts</span></span>
* <span data-ttu-id="d521f-367">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="d521f-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="d521f-368">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="d521f-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d521f-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d521f-369">Az.Batch</span></span>
* <span data-ttu-id="d521f-370">**New-AzBatchPool**이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-371">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-372">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d521f-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d521f-373">Az.FrontDoor</span></span>
* <span data-ttu-id="d521f-374">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="d521f-375">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d521f-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d521f-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="d521f-377">예외 처리</span><span class="sxs-lookup"><span data-stu-id="d521f-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d521f-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d521f-378">Az.KeyVault</span></span>
* <span data-ttu-id="d521f-379">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="d521f-380">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="d521f-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="d521f-381">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d521f-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-382">Az.Monitor</span></span>
* <span data-ttu-id="d521f-383">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="d521f-384">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="d521f-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="d521f-385">나타냄</span><span class="sxs-lookup"><span data-stu-id="d521f-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-386">Az.Network</span></span>
* <span data-ttu-id="d521f-387">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="d521f-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-388">Az.Resources</span></span>
* <span data-ttu-id="d521f-389">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="d521f-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="d521f-390">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="d521f-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-391">Az.Sql</span></span>
* <span data-ttu-id="d521f-392">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="d521f-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-393">Az.Storage</span></span>
* <span data-ttu-id="d521f-394">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="d521f-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d521f-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="d521f-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d521f-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="d521f-397">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="d521f-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="d521f-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="d521f-399">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="d521f-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="d521f-400">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="d521f-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d521f-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="d521f-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d521f-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="d521f-403">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="d521f-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="d521f-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="d521f-405">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="d521f-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="d521f-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="d521f-407">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="d521f-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d521f-408">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="d521f-408">Highlights since the last major release</span></span>
* <span data-ttu-id="d521f-409">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="d521f-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="d521f-410">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="d521f-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-411">Az.Compute</span></span>
* <span data-ttu-id="d521f-412">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="d521f-412">VM Reapply feature</span></span>
    - <span data-ttu-id="d521f-413">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="d521f-414">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="d521f-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="d521f-415">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d521f-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="d521f-416">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="d521f-417">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d521f-418">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="d521f-419">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="d521f-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="d521f-420">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="d521f-421">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="d521f-422">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d521f-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d521f-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d521f-424">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d521f-425">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="d521f-425">Get the Order</span></span>
* <span data-ttu-id="d521f-426">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d521f-427">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-427">Create new Order</span></span>
* <span data-ttu-id="d521f-428">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d521f-429">주문 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-429">Remove the Order</span></span>
* <span data-ttu-id="d521f-430">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="d521f-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="d521f-431">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="d521f-431">Now creates Local Share</span></span>
* <span data-ttu-id="d521f-432">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="d521f-433">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="d521f-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="d521f-434">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="d521f-435">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="d521f-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="d521f-436">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d521f-437">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d521f-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="d521f-438">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d521f-439">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-439">Create new Triggers</span></span>
* <span data-ttu-id="d521f-440">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d521f-441">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-442">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-443">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="d521f-444">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-446">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d521f-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d521f-447">Az.EventHub</span></span>
* <span data-ttu-id="d521f-448">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d521f-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d521f-449">Az.FrontDoor</span></span>
* <span data-ttu-id="d521f-450">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="d521f-451">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="d521f-452">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="d521f-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="d521f-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-454">Az.Network</span></span>
* <span data-ttu-id="d521f-455">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="d521f-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="d521f-456">Az.PrivateDns</span></span>
* <span data-ttu-id="d521f-457">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="d521f-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-459">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="d521f-460">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="d521f-461">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d521f-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d521f-462">Az.RedisCache</span></span>
* <span data-ttu-id="d521f-463">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="d521f-464">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="d521f-465">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-466">Az.Resources</span></span>
- <span data-ttu-id="d521f-467">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="d521f-468">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="d521f-469">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="d521f-470">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="d521f-471">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-472">Az.Sql</span></span>
* <span data-ttu-id="d521f-473">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="d521f-474">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="d521f-475">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="d521f-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="d521f-476">일반</span><span class="sxs-lookup"><span data-stu-id="d521f-476">General</span></span>
* <span data-ttu-id="d521f-477">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="d521f-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d521f-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-478">Az.Accounts</span></span>
* <span data-ttu-id="d521f-479">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d521f-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d521f-480">Az.Advisor</span></span>
* <span data-ttu-id="d521f-481">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d521f-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d521f-482">Az.Batch</span></span>
* <span data-ttu-id="d521f-483">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="d521f-484">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="d521f-485">이 변경 사항은 **Get-AzBatchAccount**에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="d521f-486">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="d521f-487">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="d521f-488">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask**에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="d521f-489">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="d521f-490">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="d521f-491">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="d521f-492">**Get-AzBatchApplication**으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d521f-493">이제 **Get-AzBatchApplicationPackage**를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="d521f-494">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="d521f-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="d521f-495">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication**에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d521f-496">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="d521f-497">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="d521f-498">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="d521f-499">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="d521f-500">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="d521f-501">**Set-AzBatchPoolOSVersion**이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="d521f-502">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="d521f-503">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d521f-504">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d521f-505">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="d521f-506">**Get-AzBatchNodeAgentSku**가 제거되고 **Get-AzBatchSupportedImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="d521f-507">**Get-AzBatchSupportedImage**가 **Get-AzBatchNodeAgentSku**와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="d521f-508">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="d521f-509">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="d521f-510">**New-AzBatchPool**의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="d521f-511">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="d521f-512">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="d521f-513">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="d521f-514">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="d521f-515">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="d521f-516">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="d521f-517">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="d521f-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="d521f-518">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="d521f-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d521f-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d521f-519">Az.Cdn</span></span>
* <span data-ttu-id="d521f-520">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="d521f-521">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-522">Az.Compute</span></span>
* <span data-ttu-id="d521f-523">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="d521f-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="d521f-524">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d521f-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="d521f-525">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d521f-525">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="d521f-526">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-526">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d521f-527">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-527">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="d521f-528">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="d521f-528">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="d521f-529">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-529">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="d521f-530">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="d521f-530">Breaking changes</span></span>
    - <span data-ttu-id="d521f-531">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-531">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="d521f-532">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-532">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-533">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-533">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-534">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-534">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-535">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-535">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-536">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="d521f-536">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="d521f-537">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-537">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="d521f-538">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="d521f-538">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="d521f-539">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-539">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="d521f-540">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-540">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="d521f-541">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-541">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d521f-542">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d521f-542">Az.FrontDoor</span></span>
* <span data-ttu-id="d521f-543">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-543">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d521f-544">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d521f-544">Az.HDInsight</span></span>
* <span data-ttu-id="d521f-545">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-545">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="d521f-546">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-546">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="d521f-547">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="d521f-547">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="d521f-548">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-548">Removed five cmdlets:</span></span>
    - <span data-ttu-id="d521f-549">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d521f-549">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d521f-550">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d521f-550">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d521f-551">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d521f-551">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d521f-552">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d521f-552">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="d521f-553">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d521f-553">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="d521f-554">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-554">Added three cmdlets:</span></span>
    - <span data-ttu-id="d521f-555">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="d521f-555">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d521f-556">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="d521f-556">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d521f-557">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="d521f-557">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="d521f-558">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-558">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="d521f-559">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-559">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="d521f-560">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-560">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="d521f-561">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-561">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="d521f-562">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-562">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="d521f-563">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-563">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="d521f-564">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-564">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="d521f-565">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-565">Added some scenario test cases.</span></span>
* <span data-ttu-id="d521f-566">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="d521f-566">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d521f-567">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d521f-567">Az.IotHub</span></span>
* <span data-ttu-id="d521f-568">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="d521f-568">Breaking changes:</span></span>
    - <span data-ttu-id="d521f-569">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-569">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d521f-570">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-570">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d521f-571">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-571">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d521f-572">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-572">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d521f-573">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-573">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="d521f-574">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="d521f-575">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-575">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="d521f-576">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-576">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="d521f-577">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-577">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d521f-578">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-578">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d521f-579">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-579">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d521f-580">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-580">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-581">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-581">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-582">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-582">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="d521f-583">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-583">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="d521f-584">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-584">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="d521f-585">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-585">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="d521f-586">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-586">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="d521f-587">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-587">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="d521f-588">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-588">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="d521f-589">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-589">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="d521f-590">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-590">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-591">Az.Resources</span></span>
* <span data-ttu-id="d521f-592">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-592">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-593">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-593">Az.Network</span></span>
* <span data-ttu-id="d521f-594">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-594">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="d521f-595">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d521f-595">Updated cmdlet:</span></span>
        - <span data-ttu-id="d521f-596">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-596">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d521f-597">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-597">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d521f-598">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-598">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d521f-599">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-599">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d521f-600">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-600">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d521f-601">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-601">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="d521f-602">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d521f-602">New cmdlet:</span></span>
        - <span data-ttu-id="d521f-603">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d521f-603">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="d521f-604">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-604">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="d521f-605">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-605">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="d521f-606">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-606">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="d521f-607">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-607">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="d521f-608">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-608">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="d521f-609">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-609">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="d521f-610">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-610">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="d521f-611">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-611">New cmdlets added:</span></span>
        - <span data-ttu-id="d521f-612">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="d521f-612">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="d521f-613">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d521f-613">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d521f-614">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d521f-614">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d521f-615">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d521f-615">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d521f-616">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d521f-616">Set-AzVirtualHub</span></span>
* <span data-ttu-id="d521f-617">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-617">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="d521f-618">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-618">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d521f-619">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="d521f-619">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d521f-620">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="d521f-620">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d521f-621">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="d521f-621">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="d521f-622">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="d521f-622">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="d521f-623">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-623">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="d521f-624">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-624">New cmdlets added:</span></span>
        - <span data-ttu-id="d521f-625">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-625">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="d521f-626">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-626">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d521f-627">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d521f-627">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d521f-628">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d521f-628">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d521f-629">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d521f-629">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d521f-630">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d521f-630">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d521f-631">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="d521f-631">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="d521f-632">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-632">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="d521f-633">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-633">New cmdlets added:</span></span>
        - <span data-ttu-id="d521f-634">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="d521f-634">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="d521f-635">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d521f-635">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="d521f-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d521f-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="d521f-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="d521f-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="d521f-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="d521f-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="d521f-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d521f-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="d521f-640">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-640">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d521f-641">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d521f-641">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="d521f-642">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-642">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="d521f-643">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-643">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="d521f-644">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-644">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="d521f-645">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-645">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d521f-646">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d521f-646">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="d521f-647">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d521f-647">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="d521f-648">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-648">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="d521f-649">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-649">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="d521f-650">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-650">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="d521f-651">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-651">New cmdlets added:</span></span>
        - <span data-ttu-id="d521f-652">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d521f-652">New-AzIpGroup</span></span>
        - <span data-ttu-id="d521f-653">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d521f-653">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="d521f-654">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d521f-654">Get-AzIpGroup</span></span>
        - <span data-ttu-id="d521f-655">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d521f-655">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d521f-656">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d521f-656">Az.ServiceFabric</span></span>
* <span data-ttu-id="d521f-657">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-657">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-658">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-658">Az.Sql</span></span>
* <span data-ttu-id="d521f-659">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-659">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="d521f-660">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-660">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="d521f-661">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-661">Removed deprecated aliases:</span></span>
* <span data-ttu-id="d521f-662">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="d521f-662">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="d521f-663">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="d521f-663">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="d521f-664">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-664">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d521f-665">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-665">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="d521f-666">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="d521f-666">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="d521f-667">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-667">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-668">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-668">Az.Storage</span></span>
* <span data-ttu-id="d521f-669">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-669">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="d521f-670">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-670">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d521f-671">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-671">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d521f-672">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-672">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="d521f-673">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d521f-673">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="d521f-674">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d521f-674">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="d521f-675">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="d521f-675">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="d521f-676">일반</span><span class="sxs-lookup"><span data-stu-id="d521f-676">General</span></span>
* <span data-ttu-id="d521f-677">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="d521f-677">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d521f-678">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-678">Az.Accounts</span></span>
* <span data-ttu-id="d521f-679">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-679">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d521f-680">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d521f-680">Az.ApiManagement</span></span>
* <span data-ttu-id="d521f-681">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-681">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="d521f-682">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-682">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-683">Az.Automation</span></span>
* <span data-ttu-id="d521f-684">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-684">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d521f-685">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d521f-685">Az.Batch</span></span>
* <span data-ttu-id="d521f-686">**Get-AzBatchNodeAgentSku**가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-686">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-687">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-687">Az.Compute</span></span>
* <span data-ttu-id="d521f-688">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-688">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d521f-689">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-689">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="d521f-690">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-690">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="d521f-691">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-691">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-692">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-693">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-693">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="d521f-694">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-694">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="d521f-695">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-695">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-696">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-696">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-697">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-697">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d521f-698">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d521f-698">Az.HealthcareApis</span></span>
* <span data-ttu-id="d521f-699">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-699">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="d521f-700">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-700">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="d521f-701">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-701">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="d521f-702">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-702">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d521f-703">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d521f-703">Az.IotHub</span></span>
* <span data-ttu-id="d521f-704">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="d521f-704">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="d521f-705">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-705">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d521f-706">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-706">Az.Monitor</span></span>
* <span data-ttu-id="d521f-707">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-707">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="d521f-708">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-708">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="d521f-709">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-709">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="d521f-710">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-710">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-711">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-711">Az.Network</span></span>
* <span data-ttu-id="d521f-712">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-712">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="d521f-713">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-713">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="d521f-714">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-714">New cmdlets added:</span></span>
        - <span data-ttu-id="d521f-715">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="d521f-715">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="d521f-716">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-716">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d521f-717">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-717">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="d521f-718">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-718">Updated cmdlets:</span></span>
        - <span data-ttu-id="d521f-719">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-719">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d521f-720">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-720">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d521f-721">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-721">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d521f-722">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-722">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="d521f-723">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="d521f-723">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="d521f-724">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-724">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="d521f-725">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-725">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d521f-726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d521f-726">Az.RedisCache</span></span>
* <span data-ttu-id="d521f-727">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-727">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-728">Az.Sql</span></span>
* <span data-ttu-id="d521f-729">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-729">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-730">Az.Storage</span></span>
* <span data-ttu-id="d521f-731">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-731">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="d521f-732">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-732">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d521f-733">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d521f-733">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="d521f-734">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-734">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d521f-735">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-735">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d521f-736">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d521f-736">Az.StorageSync</span></span>
* <span data-ttu-id="d521f-737">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-737">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-738">Az.Websites</span></span>
* <span data-ttu-id="d521f-739">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-739">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="d521f-740">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="d521f-740">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d521f-741">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d521f-741">Az.ApiManagement</span></span>
* <span data-ttu-id="d521f-742">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-742">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="d521f-743">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-743">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="d521f-744">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-744">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-745">Az.Automation</span></span>
* <span data-ttu-id="d521f-746">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-746">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="d521f-747">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-747">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="d521f-748">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-748">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-749">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-749">Az.Compute</span></span>
* <span data-ttu-id="d521f-750">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-750">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="d521f-751">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-751">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d521f-752">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-752">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="d521f-753">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-753">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="d521f-754">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-754">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="d521f-755">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-755">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="d521f-756">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-756">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="d521f-757">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-757">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="d521f-758">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-758">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-759">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-760">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-760">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="d521f-761">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-761">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d521f-762">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d521f-762">Az.HDInsight</span></span>
* <span data-ttu-id="d521f-763">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="d521f-763">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d521f-764">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d521f-764">Az.IotHub</span></span>
* <span data-ttu-id="d521f-765">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-765">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="d521f-766">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-766">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="d521f-767">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-767">New cmdlets are:</span></span>
    - <span data-ttu-id="d521f-768">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d521f-768">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d521f-769">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d521f-769">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d521f-770">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d521f-770">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d521f-771">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d521f-771">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d521f-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-772">Az.Monitor</span></span>
* <span data-ttu-id="d521f-773">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-773">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="d521f-774">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-774">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="d521f-775">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-775">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="d521f-776">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-776">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="d521f-777">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-777">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="d521f-778">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-778">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="d521f-779">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-779">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="d521f-780">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-780">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="d521f-781">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-781">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d521f-782">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-782">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="d521f-783">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-783">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d521f-784">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-784">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="d521f-785">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-785">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="d521f-786">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-786">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="d521f-787">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-787">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="d521f-788">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="d521f-788">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="d521f-789">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-789">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="d521f-790">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d521f-790">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="d521f-791">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-791">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="d521f-792">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-792">Overall improved help files</span></span>
* <span data-ttu-id="d521f-793">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-793">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-794">Az.Network</span></span>
* <span data-ttu-id="d521f-795">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-795">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="d521f-796">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-796">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="d521f-797">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-797">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="d521f-798">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-798">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="d521f-799">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-799">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="d521f-800">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-800">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="d521f-801">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-801">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="d521f-802">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-802">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="d521f-803">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-803">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="d521f-804">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-804">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="d521f-805">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-805">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="d521f-806">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-806">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="d521f-807">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-807">New cmdlets</span></span>
        - <span data-ttu-id="d521f-808">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d521f-808">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="d521f-809">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-809">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="d521f-810">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d521f-810">Updated cmdlet:</span></span>
        - <span data-ttu-id="d521f-811">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d521f-811">New-VpnSite</span></span>
        - <span data-ttu-id="d521f-812">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d521f-812">Update-VpnSite</span></span>
        - <span data-ttu-id="d521f-813">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-813">New-VpnConnection</span></span>
        - <span data-ttu-id="d521f-814">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-814">Update-VpnConnection</span></span>
* <span data-ttu-id="d521f-815">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-815">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-817">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-817">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="d521f-818">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-818">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-819">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-819">Az.Resources</span></span>
* <span data-ttu-id="d521f-820">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-820">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d521f-821">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d521f-821">Az.ServiceFabric</span></span>
* <span data-ttu-id="d521f-822">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-822">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="d521f-823">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-823">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="d521f-824">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d521f-824">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d521f-825">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d521f-825">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d521f-826">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d521f-826">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d521f-827">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d521f-827">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="d521f-828">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d521f-828">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d521f-829">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d521f-829">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d521f-830">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d521f-830">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d521f-831">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d521f-831">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d521f-832">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d521f-832">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="d521f-833">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d521f-833">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d521f-834">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d521f-834">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d521f-835">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d521f-835">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d521f-836">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="d521f-836">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="d521f-837">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-837">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d521f-838">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d521f-838">Az.SignalR</span></span>
* <span data-ttu-id="d521f-839">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-839">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-840">Az.Sql</span></span>
* <span data-ttu-id="d521f-841">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-841">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="d521f-842">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="d521f-842">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="d521f-843">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-843">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="d521f-844">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-844">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="d521f-845">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="d521f-845">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-846">Az.Storage</span></span>
* <span data-ttu-id="d521f-847">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-847">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d521f-848">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-848">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="d521f-849">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d521f-849">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="d521f-850">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d521f-850">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="d521f-851">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-851">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="d521f-852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d521f-852">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="d521f-853">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-853">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="d521f-854">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d521f-854">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d521f-855">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d521f-855">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d521f-856">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d521f-856">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d521f-857">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d521f-857">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-858">Az.Websites</span></span>
* <span data-ttu-id="d521f-859">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-859">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="d521f-860">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-860">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="d521f-861">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-861">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="d521f-862">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="d521f-862">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="d521f-863">일반</span><span class="sxs-lookup"><span data-stu-id="d521f-863">General</span></span>
* <span data-ttu-id="d521f-864">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-864">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d521f-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-865">Az.Accounts</span></span>
* <span data-ttu-id="d521f-866">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="d521f-866">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="d521f-867">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d521f-867">Az.Aks</span></span>
* <span data-ttu-id="d521f-868">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="d521f-868">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="d521f-869">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-869">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d521f-870">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d521f-870">Az.ApiManagement</span></span>
* <span data-ttu-id="d521f-871">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-871">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="d521f-872">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-872">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="d521f-873">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-873">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="d521f-874">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="d521f-874">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="d521f-875">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-875">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d521f-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d521f-876">Az.Batch</span></span>
* <span data-ttu-id="d521f-877">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-877">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d521f-878">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d521f-878">Az.Cdn</span></span>
* <span data-ttu-id="d521f-879">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-879">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-880">Az.Compute</span></span>
* <span data-ttu-id="d521f-881">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-881">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="d521f-882">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-882">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="d521f-883">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-883">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="d521f-884">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-884">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="d521f-885">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="d521f-885">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="d521f-886">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-886">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="d521f-887">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-887">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="d521f-888">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-888">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-889">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-890">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-890">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="d521f-891">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-891">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="d521f-892">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-892">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="d521f-893">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-893">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-895">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-895">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d521f-896">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d521f-896">Az.EventHub</span></span>
* <span data-ttu-id="d521f-897">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="d521f-897">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="d521f-898">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="d521f-898">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="d521f-899">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-899">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="d521f-900">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="d521f-900">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="d521f-901">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d521f-901">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d521f-902">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-902">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d521f-903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-903">Az.Monitor</span></span>
* <span data-ttu-id="d521f-904">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-904">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-905">Az.Network</span></span>
* <span data-ttu-id="d521f-906">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-906">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="d521f-907">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="d521f-907">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="d521f-908">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-908">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="d521f-909">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="d521f-909">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="d521f-910">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-910">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="d521f-911">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-911">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="d521f-912">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-912">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d521f-913">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-913">Az.OperationalInsights</span></span>
* <span data-ttu-id="d521f-914">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-914">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="d521f-915">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-915">Added example</span></span>
    - <span data-ttu-id="d521f-916">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-916">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="d521f-917">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-917">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="d521f-918">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="d521f-918">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-920">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-920">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-921">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-921">Az.Resources</span></span>
* <span data-ttu-id="d521f-922">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-922">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="d521f-923">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-923">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="d521f-924">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="d521f-924">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="d521f-925">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-925">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d521f-926">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d521f-926">Az.ServiceBus</span></span>
* <span data-ttu-id="d521f-927">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="d521f-927">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="d521f-928">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="d521f-928">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="d521f-929">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-929">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d521f-930">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d521f-930">Az.ServiceFabric</span></span>
* <span data-ttu-id="d521f-931">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="d521f-931">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="d521f-932">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="d521f-932">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="d521f-933">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="d521f-933">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="d521f-934">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-934">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="d521f-935">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="d521f-935">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="d521f-936">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="d521f-936">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-937">Az.Sql</span></span>
* <span data-ttu-id="d521f-938">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-938">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-939">Az.Storage</span></span>
* <span data-ttu-id="d521f-940">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-940">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="d521f-941">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="d521f-941">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="d521f-942">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d521f-942">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="d521f-943">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d521f-943">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="d521f-944">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="d521f-944">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="d521f-945">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d521f-945">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-946">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-946">Az.Websites</span></span>
* <span data-ttu-id="d521f-947">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-947">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="d521f-948">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="d521f-948">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-949">Az.Accounts</span></span>
* <span data-ttu-id="d521f-950">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-950">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d521f-951">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-951">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d521f-952">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-952">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-953">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-953">Az.Automation</span></span>
* <span data-ttu-id="d521f-954">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-954">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d521f-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d521f-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="d521f-956">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-956">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-957">Az.Compute</span></span>
* <span data-ttu-id="d521f-958">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-958">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d521f-959">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d521f-959">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d521f-960">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-960">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="d521f-961">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-961">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-962">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-963">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-963">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="d521f-964">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-964">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d521f-965">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d521f-965">Az.EventHub</span></span>
* <span data-ttu-id="d521f-966">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d521f-966">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d521f-967">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-967">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d521f-968">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d521f-968">Az.KeyVault</span></span>
* <span data-ttu-id="d521f-969">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-969">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d521f-970">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d521f-970">Az.LogicApp</span></span>
* <span data-ttu-id="d521f-971">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-971">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="d521f-972">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-972">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d521f-973">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d521f-973">Az.ManagedServices</span></span>
* <span data-ttu-id="d521f-974">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-974">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-975">Az.Network</span></span>
* <span data-ttu-id="d521f-976">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-976">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="d521f-977">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-977">New cmdlets</span></span>
        - <span data-ttu-id="d521f-978">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d521f-978">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d521f-979">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d521f-979">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d521f-980">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-980">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d521f-981">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-981">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d521f-982">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-982">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d521f-983">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-983">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d521f-984">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="d521f-984">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="d521f-985">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d521f-985">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="d521f-986">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="d521f-986">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="d521f-987">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-987">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="d521f-988">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-988">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="d521f-989">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-989">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="d521f-990">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-990">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="d521f-991">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="d521f-991">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="d521f-992">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-992">Updated cmdlets</span></span>
        - <span data-ttu-id="d521f-993">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-993">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d521f-994">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-994">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d521f-995">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-995">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d521f-996">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-996">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d521f-997">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-997">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="d521f-998">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d521f-998">Updated cmdlet:</span></span>
        - <span data-ttu-id="d521f-999">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-999">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d521f-1000">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-1000">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d521f-1001">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-1001">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="d521f-1002">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1002">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="d521f-1003">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1003">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="d521f-1004">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1004">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d521f-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="d521f-1006">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1006">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="d521f-1007">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1007">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1008">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1008">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-1009">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1009">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d521f-1010">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1010">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="d521f-1011">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1011">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="d521f-1012">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1012">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d521f-1013">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1013">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="d521f-1014">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1014">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d521f-1015">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1015">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="d521f-1016">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1016">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d521f-1017">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1017">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="d521f-1018">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1018">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1019">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1019">Az.Resources</span></span>
- <span data-ttu-id="d521f-1020">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-1020">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="d521f-1021">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1021">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d521f-1022">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d521f-1022">Az.ServiceBus</span></span>
* <span data-ttu-id="d521f-1023">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d521f-1023">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d521f-1024">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1024">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1025">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1025">Az.Sql</span></span>
* <span data-ttu-id="d521f-1026">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1026">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="d521f-1027">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1027">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="d521f-1028">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1028">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-1029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1029">Az.Storage</span></span>
* <span data-ttu-id="d521f-1030">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="d521f-1030">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d521f-1031">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d521f-1031">Az.StorageSync</span></span>
* <span data-ttu-id="d521f-1032">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1032">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="d521f-1033">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1033">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-1034">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1034">Az.Websites</span></span>
* <span data-ttu-id="d521f-1035">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1035">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="d521f-1036">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1036">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="d521f-1037">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1037">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="d521f-1038">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="d521f-1038">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1039">Az.Accounts</span></span>
* <span data-ttu-id="d521f-1040">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1040">Add support for profile cmdlets</span></span>
* <span data-ttu-id="d521f-1041">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1041">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="d521f-1042">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1042">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d521f-1043">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d521f-1043">Az.Advisor</span></span>
* <span data-ttu-id="d521f-1044">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="d521f-1044">GA release of Az.Advisor</span></span>
* <span data-ttu-id="d521f-1045">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1045">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d521f-1046">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d521f-1046">Az.ApiManagement</span></span>
* <span data-ttu-id="d521f-1047">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1047">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="d521f-1048">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d521f-1048">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="d521f-1049">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1049">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="d521f-1050">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1050">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="d521f-1051">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="d521f-1052">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d521f-1052">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="d521f-1053">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1053">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-1054">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-1054">Az.Automation</span></span>
* <span data-ttu-id="d521f-1055">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1055">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1056">Az.Compute</span></span>
* <span data-ttu-id="d521f-1057">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1057">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-1058">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-1058">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-1059">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1059">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d521f-1060">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d521f-1060">Az.EventGrid</span></span>
* <span data-ttu-id="d521f-1061">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1061">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d521f-1062">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d521f-1062">Az.IotHub</span></span>
* <span data-ttu-id="d521f-1063">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1063">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-1064">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1064">Az.Network</span></span>
* <span data-ttu-id="d521f-1065">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="d521f-1065">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="d521f-1066">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="d521f-1066">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d521f-1067">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-1067">Az.PolicyInsights</span></span>
* <span data-ttu-id="d521f-1068">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="d521f-1068">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="d521f-1069">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1069">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d521f-1070">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-1070">Az.OperationalInsights</span></span>
* <span data-ttu-id="d521f-1071">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1071">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-1073">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1073">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1074">Az.Resources</span></span>
    - <span data-ttu-id="d521f-1075">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1075">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="d521f-1076">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1076">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="d521f-1077">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1077">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="d521f-1078">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1078">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d521f-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d521f-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="d521f-1080">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="d521f-1080">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1081">Az.Sql</span></span>
* <span data-ttu-id="d521f-1082">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1082">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="d521f-1083">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1083">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="d521f-1084">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d521f-1084">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d521f-1085">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d521f-1085">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d521f-1086">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d521f-1086">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d521f-1087">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d521f-1087">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d521f-1088">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d521f-1088">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d521f-1089">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d521f-1089">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="d521f-1090">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-1090">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-1091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1091">Az.Storage</span></span>
* <span data-ttu-id="d521f-1092">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1092">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="d521f-1093">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d521f-1093">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="d521f-1094">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1094">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="d521f-1095">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="d521f-1095">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="d521f-1096">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1096">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="d521f-1097">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-1097">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d521f-1098">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-1098">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d521f-1099">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="d521f-1099">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="d521f-1100">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d521f-1100">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="d521f-1101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d521f-1101">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d521f-1102">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d521f-1102">Az.StorageSync</span></span>
* <span data-ttu-id="d521f-1103">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1103">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="d521f-1104">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="d521f-1104">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-1105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1105">Az.Accounts</span></span>
* <span data-ttu-id="d521f-1106">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1106">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="d521f-1107">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1107">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="d521f-1108">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="d521f-1108">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="d521f-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d521f-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="d521f-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="d521f-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1111">Az.Compute</span></span>
* <span data-ttu-id="d521f-1112">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1112">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="d521f-1113">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1113">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="d521f-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d521f-1114">Az.Dns</span></span>
* <span data-ttu-id="d521f-1115">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1115">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d521f-1116">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d521f-1116">Az.EventGrid</span></span>
* <span data-ttu-id="d521f-1117">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1117">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="d521f-1118">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d521f-1118">New cmdlets:</span></span>
    - <span data-ttu-id="d521f-1119">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d521f-1119">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d521f-1120">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1120">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d521f-1121">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d521f-1121">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d521f-1122">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1122">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="d521f-1123">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d521f-1123">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d521f-1124">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1124">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d521f-1125">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d521f-1125">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d521f-1126">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1126">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d521f-1127">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d521f-1127">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d521f-1128">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1128">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="d521f-1129">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d521f-1129">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d521f-1130">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1130">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="d521f-1131">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d521f-1131">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="d521f-1132">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1132">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="d521f-1133">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d521f-1133">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d521f-1134">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1134">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="d521f-1135">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1135">Updated cmdlets:</span></span>
    - <span data-ttu-id="d521f-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d521f-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="d521f-1137">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1137">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d521f-1138">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1138">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d521f-1139">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1139">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="d521f-1140">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1140">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="d521f-1141">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="d521f-1141">Event subscription expiration date,</span></span>
            - <span data-ttu-id="d521f-1142">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="d521f-1142">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="d521f-1143">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1143">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="d521f-1144">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="d521f-1144">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="d521f-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d521f-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="d521f-1146">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1146">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="d521f-1147">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d521f-1147">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="d521f-1148">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1148">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="d521f-1149">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1149">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d521f-1150">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d521f-1150">Az.FrontDoor</span></span>
* <span data-ttu-id="d521f-1151">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d521f-1151">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="d521f-1152">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1152">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="d521f-1153">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d521f-1153">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="d521f-1154">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1154">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-1155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1155">Az.Network</span></span>
* <span data-ttu-id="d521f-1156">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1156">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="d521f-1157">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-1157">New cmdlets</span></span>
        - <span data-ttu-id="d521f-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d521f-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="d521f-1159">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1159">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="d521f-1160">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-1160">New cmdlets</span></span>
        - <span data-ttu-id="d521f-1161">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d521f-1161">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="d521f-1162">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1162">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="d521f-1163">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-1163">New cmdlets</span></span>
        - <span data-ttu-id="d521f-1164">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d521f-1164">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d521f-1165">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d521f-1165">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d521f-1166">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d521f-1166">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d521f-1167">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-1167">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="d521f-1168">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-1168">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d521f-1169">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1169">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="d521f-1170">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-1170">New cmdlets</span></span>
        - <span data-ttu-id="d521f-1171">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d521f-1171">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d521f-1172">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d521f-1172">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d521f-1173">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d521f-1173">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d521f-1174">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d521f-1174">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="d521f-1175">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="d521f-1175">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="d521f-1176">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1176">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="d521f-1177">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1177">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="d521f-1178">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1178">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="d521f-1179">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1179">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="d521f-1180">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1180">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="d521f-1181">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1181">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="d521f-1182">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1182">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="d521f-1183">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1183">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="d521f-1184">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1184">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="d521f-1185">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1185">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="d521f-1186">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1186">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="d521f-1187">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1187">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="d521f-1188">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1188">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="d521f-1189">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="d521f-1189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d521f-1190">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1190">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="d521f-1191">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1191">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="d521f-1192">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="d521f-1192">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="d521f-1193">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="d521f-1193">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="d521f-1194">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1194">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="d521f-1195">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1195">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d521f-1196">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1196">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d521f-1197">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1197">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d521f-1198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-1198">Az.OperationalInsights</span></span>
* <span data-ttu-id="d521f-1199">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="d521f-1199">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1200">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1200">Az.Resources</span></span>
* <span data-ttu-id="d521f-1201">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1201">Support for additional Template Export options</span></span>
    - <span data-ttu-id="d521f-1202">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1202">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d521f-1203">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1203">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d521f-1204">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1204">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d521f-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d521f-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="d521f-1206">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1206">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1207">Az.Sql</span></span>
* <span data-ttu-id="d521f-1208">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1208">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="d521f-1209">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1209">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="d521f-1210">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1210">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="d521f-1211">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d521f-1211">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d521f-1212">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d521f-1212">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d521f-1213">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d521f-1213">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d521f-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d521f-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="d521f-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d521f-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-1216">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1216">Az.Storage</span></span>
* <span data-ttu-id="d521f-1217">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1217">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="d521f-1218">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-1218">New-AzStorageAccount</span></span>
* <span data-ttu-id="d521f-1219">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="d521f-1219">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="d521f-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d521f-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-1221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1221">Az.Websites</span></span>
* <span data-ttu-id="d521f-1222">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="d521f-1222">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="d521f-1223">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1223">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="d521f-1224">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="d521f-1224">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d521f-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d521f-1225">Az.Cdn</span></span>
* <span data-ttu-id="d521f-1226">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1226">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1227">Az.Compute</span></span>
* <span data-ttu-id="d521f-1228">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1228">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d521f-1229">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d521f-1229">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d521f-1230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d521f-1230">Az.EventHub</span></span>
* <span data-ttu-id="d521f-1231">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="d521f-1231">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d521f-1232">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="d521f-1232">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-1233">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1233">Az.Network</span></span>
* <span data-ttu-id="d521f-1234">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1234">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d521f-1235">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1235">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d521f-1236">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-1236">Az.PolicyInsights</span></span>
* <span data-ttu-id="d521f-1237">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="d521f-1237">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1238">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-1239">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1239">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d521f-1240">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d521f-1240">Az.ServiceBus</span></span>
* <span data-ttu-id="d521f-1241">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="d521f-1241">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d521f-1242">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d521f-1242">Az.ServiceFabric</span></span>
* <span data-ttu-id="d521f-1243">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1243">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d521f-1244">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1244">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1245">Az.Sql</span></span>
* <span data-ttu-id="d521f-1246">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1246">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d521f-1247">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="d521f-1247">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d521f-1248">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="d521f-1248">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d521f-1249">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1249">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-1250">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1250">Az.Websites</span></span>
* <span data-ttu-id="d521f-1251">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="d521f-1251">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d521f-1252">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="d521f-1252">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d521f-1253">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d521f-1253">Az.ApiManagement</span></span>
* <span data-ttu-id="d521f-1254">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1254">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d521f-1255">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="d521f-1255">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d521f-1256">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-1256">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d521f-1257">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-1257">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d521f-1258">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-1258">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d521f-1259">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-1259">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d521f-1260">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-1260">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d521f-1261">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1261">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d521f-1262">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1262">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d521f-1263">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d521f-1263">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d521f-1264">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-1264">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d521f-1265">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-1265">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d521f-1266">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1266">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d521f-1267">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1267">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d521f-1268">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-1268">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d521f-1269">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="d521f-1269">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d521f-1270">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-1270">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d521f-1271">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1271">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d521f-1272">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1272">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="d521f-1273">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1273">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d521f-1274">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1274">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d521f-1275">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1275">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d521f-1276">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1276">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d521f-1277">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1277">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="d521f-1278">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1278">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d521f-1279">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1279">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d521f-1280">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1280">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d521f-1281">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1281">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d521f-1282">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1282">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d521f-1283">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1283">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d521f-1284">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1284">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="d521f-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d521f-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d521f-1286">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1286">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d521f-1287">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1287">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d521f-1288">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="d521f-1288">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d521f-1289">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="d521f-1289">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d521f-1290">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="d521f-1290">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d521f-1291">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1291">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d521f-1292">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1292">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d521f-1293">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1293">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d521f-1294">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="d521f-1294">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d521f-1295">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="d521f-1295">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d521f-1296">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="d521f-1296">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d521f-1297">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="d521f-1297">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="d521f-1298">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1298">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d521f-1299">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="d521f-1299">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d521f-1300">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1300">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d521f-1301">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="d521f-1301">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="d521f-1302">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1302">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d521f-1303">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="d521f-1303">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d521f-1304">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1304">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d521f-1305">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="d521f-1305">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d521f-1306">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="d521f-1306">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d521f-1307">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1307">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d521f-1308">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="d521f-1308">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d521f-1309">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="d521f-1309">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d521f-1310">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1310">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d521f-1311">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="d521f-1311">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d521f-1312">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="d521f-1312">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d521f-1313">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1313">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d521f-1314">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1314">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d521f-1315">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="d521f-1315">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d521f-1316">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="d521f-1316">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d521f-1317">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1317">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d521f-1318">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="d521f-1318">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d521f-1319">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="d521f-1319">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d521f-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d521f-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d521f-1321">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="d521f-1321">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d521f-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d521f-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d521f-1323">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d521f-1323">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d521f-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d521f-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d521f-1325">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="d521f-1325">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d521f-1326">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="d521f-1326">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d521f-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d521f-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d521f-1328">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="d521f-1328">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="d521f-1329">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d521f-1329">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d521f-1330">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="d521f-1330">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-1331">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-1331">Az.Automation</span></span>
* <span data-ttu-id="d521f-1332">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1332">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d521f-1333">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1333">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d521f-1334">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d521f-1335">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1335">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d521f-1336">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1336">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d521f-1337">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="d521f-1337">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d521f-1338">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1338">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1339">Az.Compute</span></span>
* <span data-ttu-id="d521f-1340">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1340">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d521f-1341">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1341">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-1343">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1343">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d521f-1344">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-1344">Az.Monitor</span></span>
* <span data-ttu-id="d521f-1345">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1345">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-1346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1346">Az.Network</span></span>
* <span data-ttu-id="d521f-1347">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1347">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d521f-1348">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d521f-1348">Updated cmdlet:</span></span>
        - <span data-ttu-id="d521f-1349">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d521f-1349">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d521f-1350">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1350">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1351">Az.Resources</span></span>
* <span data-ttu-id="d521f-1352">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1352">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1353">Az.Sql</span></span>
* <span data-ttu-id="d521f-1354">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1354">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d521f-1355">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="d521f-1355">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-1356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1356">Az.Accounts</span></span>
* <span data-ttu-id="d521f-1357">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1357">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d521f-1358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1358">Az.CognitiveServices</span></span>
* <span data-ttu-id="d521f-1359">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1359">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d521f-1360">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="d521f-1360">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1361">Az.Compute</span></span>
* <span data-ttu-id="d521f-1362">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="d521f-1362">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d521f-1363">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d521f-1363">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d521f-1364">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-1364">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d521f-1365">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1365">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d521f-1366">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1366">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d521f-1367">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1367">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="d521f-1368">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="d521f-1368">Breaking changes</span></span>
    - <span data-ttu-id="d521f-1369">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1369">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d521f-1370">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1370">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d521f-1371">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d521f-1371">Az.DeploymentManager</span></span>
* <span data-ttu-id="d521f-1372">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="d521f-1372">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d521f-1373">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d521f-1373">Az.Dns</span></span>
* <span data-ttu-id="d521f-1374">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="d521f-1374">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d521f-1375">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1375">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d521f-1376">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1376">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d521f-1377">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d521f-1377">Az.FrontDoor</span></span>
* <span data-ttu-id="d521f-1378">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="d521f-1378">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d521f-1379">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="d521f-1379">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d521f-1380">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d521f-1380">Az.HDInsight</span></span>
* <span data-ttu-id="d521f-1381">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1381">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d521f-1382">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d521f-1382">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d521f-1383">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d521f-1383">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d521f-1384">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1384">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d521f-1385">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="d521f-1385">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d521f-1386">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1386">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d521f-1387">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1387">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d521f-1388">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-1388">Az.Monitor</span></span>
* <span data-ttu-id="d521f-1389">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-1389">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="d521f-1390">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d521f-1390">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d521f-1391">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d521f-1391">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d521f-1392">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d521f-1392">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d521f-1393">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d521f-1393">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d521f-1394">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d521f-1394">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d521f-1395">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d521f-1395">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d521f-1396">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d521f-1396">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d521f-1397">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d521f-1397">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d521f-1398">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d521f-1398">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d521f-1399">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d521f-1399">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d521f-1400">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d521f-1400">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d521f-1401">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="d521f-1401">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d521f-1402">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1402">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-1403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1403">Az.Network</span></span>
* <span data-ttu-id="d521f-1404">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1404">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d521f-1405">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-1405">New cmdlets</span></span>
        - <span data-ttu-id="d521f-1406">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d521f-1406">New-AzNatGateway</span></span>
        - <span data-ttu-id="d521f-1407">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d521f-1407">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d521f-1408">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d521f-1408">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d521f-1409">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d521f-1409">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d521f-1410">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1410">Updated cmdlets</span></span>
        - <span data-ttu-id="d521f-1411">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d521f-1411">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d521f-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d521f-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d521f-1413">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="d521f-1413">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d521f-1414">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1414">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d521f-1415">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1415">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d521f-1416">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-1416">Az.PolicyInsights</span></span>
* <span data-ttu-id="d521f-1417">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1417">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d521f-1418">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1418">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d521f-1419">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1419">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1420">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1420">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-1421">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1421">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d521f-1422">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="d521f-1422">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d521f-1423">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1423">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d521f-1424">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1424">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d521f-1425">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1425">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d521f-1426">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="d521f-1426">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d521f-1427">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d521f-1427">Az.Relay</span></span>
* <span data-ttu-id="d521f-1428">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1428">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d521f-1429">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d521f-1429">Az.ServiceBus</span></span>
* <span data-ttu-id="d521f-1430">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="d521f-1430">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1431">Az.Storage</span></span>
* <span data-ttu-id="d521f-1432">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="d521f-1432">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d521f-1433">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1433">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d521f-1434">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1434">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d521f-1435">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-1435">New-AzStorageAccount</span></span>
* <span data-ttu-id="d521f-1436">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1436">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d521f-1437">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-1437">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d521f-1438">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-1438">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d521f-1439">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d521f-1439">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-1440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1440">Az.Websites</span></span>
* <span data-ttu-id="d521f-1441">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1441">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d521f-1442">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1442">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d521f-1443">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="d521f-1443">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d521f-1444">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="d521f-1444">Highlights since the last major release</span></span>
* <span data-ttu-id="d521f-1445">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="d521f-1445">General availability of `Az` module</span></span>
* <span data-ttu-id="d521f-1446">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1446">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d521f-1447">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="d521f-1447">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d521f-1448">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1448">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d521f-1449">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1449">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d521f-1450">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1450">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d521f-1451">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1451">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d521f-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1452">Az.Accounts</span></span>
* <span data-ttu-id="d521f-1453">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1453">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d521f-1454">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d521f-1454">Az.Batch</span></span>
* <span data-ttu-id="d521f-1455">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1455">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d521f-1456">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d521f-1456">Az.Cdn</span></span>
* <span data-ttu-id="d521f-1457">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1457">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d521f-1458">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1458">Az.CognitiveServices</span></span>
* <span data-ttu-id="d521f-1459">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1459">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1460">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1460">Az.Compute</span></span>
* <span data-ttu-id="d521f-1461">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1461">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d521f-1462">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1462">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d521f-1463">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1463">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-1464">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-1464">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-1465">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1465">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-1466">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-1466">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-1467">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1467">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d521f-1468">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d521f-1468">Az.EventGrid</span></span>
* <span data-ttu-id="d521f-1469">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1469">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d521f-1470">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d521f-1470">Az.EventHub</span></span>
* <span data-ttu-id="d521f-1471">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="d521f-1471">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d521f-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d521f-1472">Az.HDInsight</span></span>
* <span data-ttu-id="d521f-1473">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d521f-1474">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d521f-1474">Az.IotHub</span></span>
* <span data-ttu-id="d521f-1475">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d521f-1476">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d521f-1476">Az.KeyVault</span></span>
* <span data-ttu-id="d521f-1477">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1477">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d521f-1478">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1478">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d521f-1479">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d521f-1479">Az.MachineLearning</span></span>
* <span data-ttu-id="d521f-1480">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d521f-1481">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d521f-1481">Az.Media</span></span>
* <span data-ttu-id="d521f-1482">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1482">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d521f-1483">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-1483">Az.Monitor</span></span>
  * <span data-ttu-id="d521f-1484">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-1484">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d521f-1485">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d521f-1485">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d521f-1486">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d521f-1486">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d521f-1487">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d521f-1487">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d521f-1488">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d521f-1488">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d521f-1489">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d521f-1489">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d521f-1490">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1490">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-1491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1491">Az.Network</span></span>
* <span data-ttu-id="d521f-1492">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1492">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d521f-1493">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1493">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d521f-1494">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d521f-1494">Az.NotificationHubs</span></span>
* <span data-ttu-id="d521f-1495">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1495">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d521f-1496">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-1496">Az.OperationalInsights</span></span>
* <span data-ttu-id="d521f-1497">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1497">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d521f-1498">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d521f-1498">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d521f-1499">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1499">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1500">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-1501">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1501">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d521f-1502">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1502">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d521f-1503">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1503">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d521f-1504">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1504">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d521f-1505">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d521f-1505">Az.RedisCache</span></span>
* <span data-ttu-id="d521f-1506">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1506">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1507">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1507">Az.Resources</span></span>
* <span data-ttu-id="d521f-1508">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1508">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1509">Az.Sql</span></span>
* <span data-ttu-id="d521f-1510">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1510">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d521f-1511">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1511">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d521f-1512">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1512">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d521f-1513">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1513">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d521f-1514">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1514">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d521f-1515">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1515">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d521f-1516">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1516">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-1517">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1517">Az.Websites</span></span>
* <span data-ttu-id="d521f-1518">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1518">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d521f-1519">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1519">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d521f-1520">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1520">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d521f-1521">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1521">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d521f-1522">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="d521f-1522">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d521f-1523">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="d521f-1523">Highlights since the last major release</span></span>
* <span data-ttu-id="d521f-1524">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="d521f-1524">General availability of `Az` module</span></span>
* <span data-ttu-id="d521f-1525">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1525">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d521f-1526">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="d521f-1526">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d521f-1527">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1527">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d521f-1528">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1528">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d521f-1529">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1529">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d521f-1530">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1530">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d521f-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1531">Az.Accounts</span></span>
* <span data-ttu-id="d521f-1532">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1532">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d521f-1533">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1533">Az.AnalysisServices</span></span>
* <span data-ttu-id="d521f-1534">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-1534">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d521f-1535">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="d521f-1535">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-1536">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-1536">Az.Automation</span></span>
* <span data-ttu-id="d521f-1537">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1537">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d521f-1538">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="d521f-1538">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d521f-1539">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1539">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1540">Az.Compute</span></span>
* <span data-ttu-id="d521f-1541">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1541">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d521f-1542">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="d521f-1542">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d521f-1543">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d521f-1543">Az.ContainerInstance</span></span>
* <span data-ttu-id="d521f-1544">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1544">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-1545">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-1546">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1546">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d521f-1547">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1547">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1548">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1548">Az.Resources</span></span>
* <span data-ttu-id="d521f-1549">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="d521f-1549">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d521f-1550">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="d521f-1550">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d521f-1551">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="d521f-1551">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d521f-1552">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1552">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d521f-1553">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1553">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d521f-1554">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1554">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1555">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1555">Az.Sql</span></span>
* <span data-ttu-id="d521f-1556">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1556">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-1557">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1557">Az.Storage</span></span>
* <span data-ttu-id="d521f-1558">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="d521f-1558">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d521f-1559">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d521f-1559">New-AzStorageContext</span></span>
* <span data-ttu-id="d521f-1560">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1560">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d521f-1561">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d521f-1561">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d521f-1562">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d521f-1562">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d521f-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d521f-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d521f-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d521f-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d521f-1565">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1565">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d521f-1566">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d521f-1566">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d521f-1567">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d521f-1567">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d521f-1568">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d521f-1568">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d521f-1569">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d521f-1569">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d521f-1570">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="d521f-1570">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d521f-1571">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="d521f-1571">Highlights since the last major release</span></span>
* <span data-ttu-id="d521f-1572">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="d521f-1572">General availability of `Az` module</span></span>
* <span data-ttu-id="d521f-1573">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1573">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d521f-1574">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="d521f-1574">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d521f-1575">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1575">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d521f-1576">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1576">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d521f-1577">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1577">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d521f-1578">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1578">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-1579">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-1579">Az.Automation</span></span>
* <span data-ttu-id="d521f-1580">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1580">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d521f-1581">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="d521f-1581">Dynamic grouping</span></span>
    * <span data-ttu-id="d521f-1582">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="d521f-1582">Pre-Post script</span></span>
    * <span data-ttu-id="d521f-1583">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="d521f-1583">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1584">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1584">Az.Compute</span></span>
* <span data-ttu-id="d521f-1585">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1585">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d521f-1586">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1586">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d521f-1587">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d521f-1587">Az.KeyVault</span></span>
* <span data-ttu-id="d521f-1588">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1588">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1589">Az.Network</span></span>
* <span data-ttu-id="d521f-1590">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1590">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d521f-1591">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1591">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-1593">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1593">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d521f-1594">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1594">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1595">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1595">Az.Resources</span></span>
* <span data-ttu-id="d521f-1596">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1596">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d521f-1597">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1597">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1598">Az.Sql</span></span>
* <span data-ttu-id="d521f-1599">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1599">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-1600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1600">Az.Storage</span></span>
* <span data-ttu-id="d521f-1601">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1601">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d521f-1602">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d521f-1602">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d521f-1603">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d521f-1603">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d521f-1604">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d521f-1604">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d521f-1605">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d521f-1605">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d521f-1606">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d521f-1606">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d521f-1607">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d521f-1607">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-1608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1608">Az.Websites</span></span>
* <span data-ttu-id="d521f-1609">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1609">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="d521f-1610">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="d521f-1610">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-1611">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1611">Az.Accounts</span></span>
* <span data-ttu-id="d521f-1612">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1612">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d521f-1613">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1613">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-1614">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-1614">Az.Automation</span></span>
* <span data-ttu-id="d521f-1615">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1615">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d521f-1616">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1616">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d521f-1617">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="d521f-1617">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d521f-1618">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d521f-1618">Az.Cdn</span></span>
* <span data-ttu-id="d521f-1619">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1619">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1620">Az.Compute</span></span>
* <span data-ttu-id="d521f-1621">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1621">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-1622">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-1622">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-1623">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1623">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d521f-1624">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d521f-1624">Az.LogicApp</span></span>
* <span data-ttu-id="d521f-1625">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1625">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-1626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1626">Az.Network</span></span>
* <span data-ttu-id="d521f-1627">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1627">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1628">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-1629">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1629">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d521f-1630">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1630">SDK Update</span></span>
* <span data-ttu-id="d521f-1631">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-1631">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d521f-1632">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1632">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1633">Az.Resources</span></span>
* <span data-ttu-id="d521f-1634">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="d521f-1634">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d521f-1635">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1635">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d521f-1636">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1636">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d521f-1637">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1637">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d521f-1638">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d521f-1638">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d521f-1639">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1639">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1640">Az.Sql</span></span>
* <span data-ttu-id="d521f-1641">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1641">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d521f-1642">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1642">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-1643">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1643">Az.Storage</span></span>
* <span data-ttu-id="d521f-1644">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1644">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d521f-1645">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="d521f-1645">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d521f-1646">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1646">Az.AnalysisServices</span></span>
* <span data-ttu-id="d521f-1647">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-1647">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-1648">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-1648">Az.Automation</span></span>
* <span data-ttu-id="d521f-1649">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1649">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d521f-1650">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1650">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d521f-1651">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="d521f-1651">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d521f-1652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1652">Az.CognitiveServices</span></span>
* <span data-ttu-id="d521f-1653">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1653">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1654">Az.Compute</span></span>
* <span data-ttu-id="d521f-1655">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="d521f-1655">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d521f-1656">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1656">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d521f-1657">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1657">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d521f-1658">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1658">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-1659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-1659">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-1660">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1660">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d521f-1661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d521f-1661">Az.EventHub</span></span>
* <span data-ttu-id="d521f-1662">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1662">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d521f-1663">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d521f-1663">Az.KeyVault</span></span>
* <span data-ttu-id="d521f-1664">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1664">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d521f-1665">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d521f-1665">Az.LogicApp</span></span>
* <span data-ttu-id="d521f-1666">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1666">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d521f-1667">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1667">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d521f-1668">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-1668">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d521f-1669">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d521f-1669">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d521f-1670">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d521f-1670">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d521f-1671">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d521f-1671">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d521f-1672">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d521f-1672">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d521f-1673">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-1673">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d521f-1674">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d521f-1674">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d521f-1675">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d521f-1675">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d521f-1676">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d521f-1676">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d521f-1677">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d521f-1677">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d521f-1678">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1678">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d521f-1679">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-1679">Az.Monitor</span></span>
* <span data-ttu-id="d521f-1680">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1680">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1681">Az.Network</span></span>
* <span data-ttu-id="d521f-1682">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1682">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d521f-1683">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-1683">Az.OperationalInsights</span></span>
* <span data-ttu-id="d521f-1684">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1684">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d521f-1685">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1685">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="d521f-1686">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1686">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1687">Az.Resources</span></span>
* <span data-ttu-id="d521f-1688">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1688">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d521f-1689">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d521f-1690">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d521f-1691">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1691">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1692">Az.Sql</span></span>
* <span data-ttu-id="d521f-1693">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1693">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d521f-1694">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1694">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-1695">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1695">Az.Websites</span></span>
* <span data-ttu-id="d521f-1696">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="d521f-1696">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d521f-1697">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="d521f-1697">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-1698">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1698">Az.Accounts</span></span>
* <span data-ttu-id="d521f-1699">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1699">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d521f-1700">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1700">Az.AnalysisServices</span></span>
<span data-ttu-id="d521f-1701">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="d521f-1701">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1702">Az.Compute</span></span>
* <span data-ttu-id="d521f-1703">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1703">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d521f-1704">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1704">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d521f-1705">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1705">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1706">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1706">Az.RecoveryServices</span></span>
<span data-ttu-id="d521f-1707">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="d521f-1707">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1708">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1708">Az.Resources</span></span>
* <span data-ttu-id="d521f-1709">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1709">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="d521f-1710">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1710">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d521f-1711">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1711">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="d521f-1712">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1712">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1713">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1713">Az.Sql</span></span>
* <span data-ttu-id="d521f-1714">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1714">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d521f-1715">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1715">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d521f-1716">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1716">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d521f-1717">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="d521f-1717">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-1718">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1718">Az.Accounts</span></span>
* <span data-ttu-id="d521f-1719">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="d521f-1719">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d521f-1720">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1720">Az.AnalysisServices</span></span>
* <span data-ttu-id="d521f-1721">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="d521f-1721">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1722">Az.RecoveryServices</span></span>
* <span data-ttu-id="d521f-1723">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="d521f-1723">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d521f-1724">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="d521f-1724">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-1725">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1725">Az.Accounts</span></span>
* <span data-ttu-id="d521f-1726">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1726">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d521f-1727">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1727">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d521f-1728">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1728">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d521f-1729">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d521f-1729">Az.Aks</span></span>
* <span data-ttu-id="d521f-1730">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1730">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d521f-1731">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-1731">Az.Automation</span></span>
* <span data-ttu-id="d521f-1732">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1732">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d521f-1733">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1733">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d521f-1734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d521f-1734">Az.Cdn</span></span>
* <span data-ttu-id="d521f-1735">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1735">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1736">Az.Compute</span></span>
* <span data-ttu-id="d521f-1737">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1737">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d521f-1738">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1738">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d521f-1739">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1739">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d521f-1740">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d521f-1740">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d521f-1741">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1741">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d521f-1742">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d521f-1742">Az.DataFactory</span></span>
* <span data-ttu-id="d521f-1743">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1743">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-1744">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-1744">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-1745">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1745">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d521f-1746">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1746">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d521f-1747">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1747">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d521f-1748">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d521f-1748">Az.IotHub</span></span>
* <span data-ttu-id="d521f-1749">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1749">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d521f-1750">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d521f-1750">Az.KeyVault</span></span>
* <span data-ttu-id="d521f-1751">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1751">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1752">Az.Network</span></span>
* <span data-ttu-id="d521f-1753">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1753">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1754">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1754">Az.Resources</span></span>
* <span data-ttu-id="d521f-1755">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1755">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d521f-1756">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1756">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d521f-1757">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="d521f-1757">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d521f-1758">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1758">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d521f-1759">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d521f-1760">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1760">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d521f-1761">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1761">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d521f-1762">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d521f-1762">Az.ServiceFabric</span></span>
* <span data-ttu-id="d521f-1763">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1763">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d521f-1764">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1764">Fix some error messages.</span></span>
* <span data-ttu-id="d521f-1765">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1765">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d521f-1766">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1766">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d521f-1767">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d521f-1767">Az.SignalR</span></span>
* <span data-ttu-id="d521f-1768">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1768">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1769">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1769">Az.Sql</span></span>
* <span data-ttu-id="d521f-1770">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1770">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d521f-1771">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1771">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d521f-1772">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1772">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d521f-1773">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1773">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-1774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1774">Az.Storage</span></span>
* <span data-ttu-id="d521f-1775">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1775">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d521f-1776">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1776">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d521f-1777">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d521f-1777">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d521f-1778">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d521f-1778">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d521f-1779">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d521f-1779">Az.TrafficManager</span></span>
* <span data-ttu-id="d521f-1780">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1780">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-1781">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1781">Az.Websites</span></span>
* <span data-ttu-id="d521f-1782">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1782">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d521f-1783">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1783">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d521f-1784">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1784">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d521f-1785">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="d521f-1785">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d521f-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1786">Az.Accounts</span></span>
* <span data-ttu-id="d521f-1787">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1787">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-1788">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1788">Az.Compute</span></span>
* <span data-ttu-id="d521f-1789">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1789">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d521f-1790">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1790">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d521f-1791">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1791">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-1792">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-1792">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-1793">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1793">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d521f-1794">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1794">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d521f-1795">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d521f-1795">Az.EventGrid</span></span>
* <span data-ttu-id="d521f-1796">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1796">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d521f-1797">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1797">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d521f-1798">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1798">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d521f-1799">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="d521f-1799">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d521f-1800">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="d521f-1800">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d521f-1801">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1801">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d521f-1802">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1802">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d521f-1803">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="d521f-1803">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d521f-1804">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="d521f-1804">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d521f-1805">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1805">Dead letter endpoint.</span></span>
* <span data-ttu-id="d521f-1806">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1806">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d521f-1807">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1807">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d521f-1808">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d521f-1808">Az.IotHub</span></span>
* <span data-ttu-id="d521f-1809">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1809">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d521f-1810">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d521f-1810">Az.LogicApp</span></span>
* <span data-ttu-id="d521f-1811">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="d521f-1811">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1812">Az.Resources</span></span>
* <span data-ttu-id="d521f-1813">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1813">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d521f-1814">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1814">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d521f-1815">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1815">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d521f-1816">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1816">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d521f-1817">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1817">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d521f-1818">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1818">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d521f-1819">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d521f-1819">Az.SignalR</span></span>
* <span data-ttu-id="d521f-1820">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1820">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1821">Az.Sql</span></span>
* <span data-ttu-id="d521f-1822">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1822">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d521f-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1823">Az.Storage</span></span>
* <span data-ttu-id="d521f-1824">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1824">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d521f-1825">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d521f-1825">New-AzStorageContext</span></span>
* <span data-ttu-id="d521f-1826">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1826">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d521f-1827">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d521f-1827">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1828">Az.Websites</span></span>
* <span data-ttu-id="d521f-1829">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1829">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d521f-1830">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1830">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d521f-1831">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="d521f-1831">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d521f-1832">일반</span><span class="sxs-lookup"><span data-stu-id="d521f-1832">General</span></span>

- <span data-ttu-id="d521f-1833">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="d521f-1833">General Availability of Az Module</span></span>
- <span data-ttu-id="d521f-1834">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="d521f-1834">Online help for each module</span></span>
- <span data-ttu-id="d521f-1835">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1835">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d521f-1836">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1836">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d521f-1837">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d521f-1837">Az.Accounts</span></span>
- <span data-ttu-id="d521f-1838">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="d521f-1838">Changed from Az.Profile</span></span>
- <span data-ttu-id="d521f-1839">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1839">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d521f-1840">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d521f-1840">Az.ApiManagement</span></span>
- <span data-ttu-id="d521f-1841">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1841">Fixes for #7002</span></span>
- <span data-ttu-id="d521f-1842">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1842">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d521f-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d521f-1843">Az.Batch</span></span>
- <span data-ttu-id="d521f-1844">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1844">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d521f-1845">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1845">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d521f-1846">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1846">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d521f-1847">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d521f-1847">Az.Billing</span></span>
- <span data-ttu-id="d521f-1848">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1848">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d521f-1849">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1849">Az.CognitivServices</span></span>
- <span data-ttu-id="d521f-1850">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1850">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d521f-1851">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-1851">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d521f-1852">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d521f-1852">Az.ContainerInstance</span></span>
- <span data-ttu-id="d521f-1853">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1853">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d521f-1854">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d521f-1854">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d521f-1855">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1855">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d521f-1856">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-1856">Az.DataLakeStore</span></span>
- <span data-ttu-id="d521f-1857">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1857">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d521f-1858">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d521f-1858">Az.Monitor</span></span>
- <span data-ttu-id="d521f-1859">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1859">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d521f-1860">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d521f-1860">Az.KeyVault</span></span>
- <span data-ttu-id="d521f-1861">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="d521f-1861">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d521f-1862">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d521f-1862">Az.MachineLearning</span></span>
- <span data-ttu-id="d521f-1863">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="d521f-1863">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d521f-1864">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d521f-1864">Az.Media</span></span>
- <span data-ttu-id="d521f-1865">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1865">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d521f-1866">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1866">Az.Network</span></span>
<span data-ttu-id="d521f-1867">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1867">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d521f-1868">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1868">New cmdlets added:</span></span>
        - <span data-ttu-id="d521f-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d521f-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d521f-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d521f-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d521f-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d521f-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d521f-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d521f-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d521f-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d521f-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d521f-1874">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d521f-1874">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d521f-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d521f-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d521f-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d521f-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d521f-1877">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d521f-1877">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d521f-1878">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d521f-1878">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d521f-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d521f-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d521f-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d521f-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d521f-1881">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-1881">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d521f-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d521f-1883">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1883">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d521f-1884">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d521f-1884">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d521f-1885">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d521f-1885">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d521f-1886">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d521f-1886">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d521f-1887">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d521f-1887">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d521f-1888">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d521f-1888">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d521f-1889">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1889">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d521f-1890">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-1890">Az.OperationalInsights</span></span>
- <span data-ttu-id="d521f-1891">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1891">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d521f-1892">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d521f-1892">Az.Profile</span></span>
- <span data-ttu-id="d521f-1893">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="d521f-1893">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1894">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1894">Az.RecoveryServices</span></span>
- <span data-ttu-id="d521f-1895">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1895">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d521f-1896">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1896">Az.Resources</span></span>
- <span data-ttu-id="d521f-1897">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1897">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d521f-1898">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d521f-1898">Az.ServiceFabric</span></span>
- <span data-ttu-id="d521f-1899">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1899">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d521f-1900">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1900">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d521f-1901">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d521f-1901">Az.SIgnalR</span></span>
- <span data-ttu-id="d521f-1902">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="d521f-1902">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d521f-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1903">Az.Sql</span></span>
- <span data-ttu-id="d521f-1904">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1904">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d521f-1905">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1905">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d521f-1906">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1906">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d521f-1907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1907">Az.Storage</span></span>
- <span data-ttu-id="d521f-1908">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1908">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d521f-1909">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1909">Az.Websites</span></span>
- <span data-ttu-id="d521f-1910">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d521f-1910">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d521f-1911">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="d521f-1911">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d521f-1912">일반</span><span class="sxs-lookup"><span data-stu-id="d521f-1912">General</span></span>

* <span data-ttu-id="d521f-1913">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="d521f-1913">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d521f-1914">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1914">Az.Compute</span></span>

* <span data-ttu-id="d521f-1915">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1915">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d521f-1916">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-1916">Az.DataLakeStore</span></span>

* <span data-ttu-id="d521f-1917">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1917">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d521f-1918">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d521f-1918">Az.FrontDoor</span></span>

* <span data-ttu-id="d521f-1919">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1919">Fixed some broken links</span></span>
    - <span data-ttu-id="d521f-1920">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1920">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d521f-1921">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1921">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d521f-1922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d521f-1922">Az.RecoveryServices</span></span>

* <span data-ttu-id="d521f-1923">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1923">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d521f-1924">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1924">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d521f-1925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1925">Az.Resources</span></span>

* <span data-ttu-id="d521f-1926">https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1926">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d521f-1927">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1927">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d521f-1928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1928">Az.Sql</span></span>

* <span data-ttu-id="d521f-1929">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="d521f-1929">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d521f-1930">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="d521f-1930">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d521f-1931">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1931">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d521f-1932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-1932">Az.Storage</span></span>

* <span data-ttu-id="d521f-1933">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1933">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d521f-1934">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1934">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d521f-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d521f-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d521f-1936">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="d521f-1936">Support Static Website configuration</span></span>
    - <span data-ttu-id="d521f-1937">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d521f-1937">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d521f-1938">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d521f-1938">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d521f-1939">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-1939">Az.Websites</span></span>

* <span data-ttu-id="d521f-1940">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d521f-1940">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="d521f-1941">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1941">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d521f-1942">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1942">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d521f-1943">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="d521f-1943">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d521f-1944">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d521f-1944">Az.ApiManagement</span></span>
* <span data-ttu-id="d521f-1945">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1945">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d521f-1946">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d521f-1946">Az.Automation</span></span>
* <span data-ttu-id="d521f-1947">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="d521f-1947">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d521f-1948">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1948">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d521f-1949">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1949">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d521f-1950">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1950">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d521f-1951">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1951">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d521f-1952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-1952">Az.Compute</span></span>
* <span data-ttu-id="d521f-1953">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-1953">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d521f-1954">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1954">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d521f-1955">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d521f-1955">Az.ContainerInstance</span></span>
* <span data-ttu-id="d521f-1956">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1956">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d521f-1957">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d521f-1957">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d521f-1958">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1958">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d521f-1959">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-1959">Az.Network</span></span>
* <span data-ttu-id="d521f-1960">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1960">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d521f-1961">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1961">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d521f-1962">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1962">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="d521f-1963">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="d521f-1963">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d521f-1964">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d521f-1964">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d521f-1965">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1965">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d521f-1966">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1966">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d521f-1967">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d521f-1967">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d521f-1968">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="d521f-1968">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d521f-1969">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-1969">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d521f-1970">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d521f-1970">Az.Relay</span></span>
* <span data-ttu-id="d521f-1971">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1971">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d521f-1972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-1972">Az.Resources</span></span>
* <span data-ttu-id="d521f-1973">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="d521f-1973">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d521f-1974">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1974">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d521f-1975">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="d521f-1975">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d521f-1976">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d521f-1976">Az.ServiceFabric</span></span>
* <span data-ttu-id="d521f-1977">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1977">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d521f-1978">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-1978">Az.Sql</span></span>
* <span data-ttu-id="d521f-1979">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-1979">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d521f-1980">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d521f-1980">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d521f-1981">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d521f-1981">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d521f-1982">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d521f-1982">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d521f-1983">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d521f-1983">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d521f-1984">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d521f-1984">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d521f-1985">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d521f-1985">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d521f-1986">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d521f-1986">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d521f-1987">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d521f-1987">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d521f-1988">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1988">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d521f-1989">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1989">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d521f-1990">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1990">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d521f-1991">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d521f-1991">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d521f-1992">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d521f-1992">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d521f-1993">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d521f-1993">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d521f-1994">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d521f-1994">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d521f-1995">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="d521f-1995">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d521f-1996">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="d521f-1996">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d521f-1997">일반</span><span class="sxs-lookup"><span data-stu-id="d521f-1997">General</span></span>
* <span data-ttu-id="d521f-1998">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-1998">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d521f-1999">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d521f-1999">Az.Profile</span></span>
* <span data-ttu-id="d521f-2000">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2000">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d521f-2001">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="d521f-2001">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d521f-2002">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="d521f-2002">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d521f-2003">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-2003">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d521f-2004">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-2004">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d521f-2005">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-2005">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d521f-2006">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-2006">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d521f-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d521f-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="d521f-2008">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2008">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-2009">Az.Compute</span></span>
* <span data-ttu-id="d521f-2010">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="d521f-2010">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d521f-2011">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="d521f-2011">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d521f-2012">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2012">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-2013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-2013">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-2014">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2014">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d521f-2015">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2015">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d521f-2016">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d521f-2016">Az.Insights</span></span>
* <span data-ttu-id="d521f-2017">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="d521f-2017">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d521f-2018">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="d521f-2018">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d521f-2019">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="d521f-2019">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d521f-2020">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="d521f-2020">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-2021">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-2021">Az.Network</span></span>
* <span data-ttu-id="d521f-2022">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2022">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d521f-2023">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d521f-2023">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d521f-2024">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d521f-2024">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d521f-2025">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d521f-2025">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d521f-2026">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d521f-2026">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d521f-2027">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d521f-2027">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d521f-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d521f-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d521f-2029">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d521f-2029">Az.PolicyInsights</span></span>
* <span data-ttu-id="d521f-2030">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d521f-2030">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-2031">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-2031">Az.Resources</span></span>
* <span data-ttu-id="d521f-2032">https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-2032">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d521f-2033">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="d521f-2033">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d521f-2034">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d521f-2034">Az.ServiceBus</span></span>
* <span data-ttu-id="d521f-2035">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="d521f-2035">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d521f-2036">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d521f-2036">Az.ServiceFabric</span></span>
* <span data-ttu-id="d521f-2037">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="d521f-2037">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d521f-2038">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-2038">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d521f-2039">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="d521f-2039">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d521f-2040">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d521f-2040">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d521f-2041">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="d521f-2041">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d521f-2042">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="d521f-2042">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d521f-2043">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d521f-2043">Az.Profile</span></span>
* <span data-ttu-id="d521f-2044">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2044">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d521f-2045">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2045">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-2046">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-2046">Az.Compute</span></span>
* <span data-ttu-id="d521f-2047">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2047">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d521f-2048">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2048">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d521f-2049">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d521f-2049">Az.DataLakeStore</span></span>
* <span data-ttu-id="d521f-2050">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-2050">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d521f-2051">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2051">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d521f-2052">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2052">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d521f-2053">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2053">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d521f-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-2055">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-2055">Az.Network</span></span>
* <span data-ttu-id="d521f-2056">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2056">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d521f-2057">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2057">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-2058">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-2058">Az.Resources</span></span>
* <span data-ttu-id="d521f-2059">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2059">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d521f-2060">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2060">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d521f-2061">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="d521f-2061">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d521f-2062">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d521f-2062">Azure.Storage</span></span>
* <span data-ttu-id="d521f-2063">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-2063">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d521f-2064">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d521f-2064">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d521f-2065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d521f-2065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d521f-2066">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2066">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d521f-2067">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d521f-2067">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d521f-2068">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d521f-2068">Az.CognitiveServices</span></span>
* <span data-ttu-id="d521f-2069">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2069">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d521f-2070">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d521f-2070">Az.Compute</span></span>
* <span data-ttu-id="d521f-2071">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-2071">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d521f-2072">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="d521f-2072">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d521f-2073">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-2073">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d521f-2074">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d521f-2074">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d521f-2075">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="d521f-2075">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d521f-2076">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d521f-2076">Az.Network</span></span>
* <span data-ttu-id="d521f-2077">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-2077">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d521f-2078">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2078">new cmdlets added</span></span>
    - <span data-ttu-id="d521f-2079">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d521f-2079">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d521f-2080">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d521f-2080">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d521f-2081">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d521f-2081">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d521f-2082">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d521f-2082">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d521f-2083">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-2083">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d521f-2084">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d521f-2084">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d521f-2085">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-2085">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d521f-2086">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-2086">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d521f-2087">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-2087">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d521f-2088">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d521f-2088">Az.RedisCache</span></span>
* <span data-ttu-id="d521f-2089">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="d521f-2089">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d521f-2090">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-2090">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d521f-2091">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d521f-2091">Az.Resources</span></span>
* <span data-ttu-id="d521f-2092">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="d521f-2092">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d521f-2093">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="d521f-2093">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d521f-2094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d521f-2094">Az.Sql</span></span>
* <span data-ttu-id="d521f-2095">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="d521f-2095">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d521f-2096">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d521f-2096">Az.Websites</span></span>
* <span data-ttu-id="d521f-2097">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2097">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d521f-2098">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d521f-2098">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d521f-2099">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="d521f-2099">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d521f-2100">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="d521f-2100">Initial Release</span></span>
