---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 60827fe7b4f8c351655046e3711660cdf7ce0513
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/19/2020
ms.locfileid: "83631067"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="865fa-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="865fa-103">Azure PowerShell release notes</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="865fa-104">4.1.0 - 2020년 5월</span><span class="sxs-lookup"><span data-stu-id="865fa-104">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="865fa-105">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="865fa-105">Highlights since the last release</span></span>
* <span data-ttu-id="865fa-106">지원되는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="865fa-106">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="865fa-107">Az.Functions 일반 공급</span><span class="sxs-lookup"><span data-stu-id="865fa-107">General availability of Az.Functions</span></span> 
* <span data-ttu-id="865fa-108">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources 및 Az.Storage의 주요 릴리스 출시</span><span class="sxs-lookup"><span data-stu-id="865fa-108">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="865fa-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-109">Az.Accounts</span></span>
* <span data-ttu-id="865fa-110">'AzureSynapseAnalyticsEndpointResourceId' 및 'AzureSynapseAnalyticsEndpointSuffix' 매개 변수를 허용하도록 'Add-AzEnvironment' 및 'Set-AzEnvironment' 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-110">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="865fa-111">Az.Accounts에 Azure.Core 관련 어셈블리가 추가되었으며 지원되는 PowerShell 플랫폼은 Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-111">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="865fa-112">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="865fa-112">Az.Aks</span></span>
* <span data-ttu-id="865fa-113">API 버전을 2019-10-01로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="865fa-113">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="865fa-114">Windows 컨테이너를 사용하여 AKS 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-114">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="865fa-115">새 cmdlet 추가: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool', 'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="865fa-115">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="865fa-116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-116">Az.ApiManagement</span></span>
* <span data-ttu-id="865fa-117">'New-AzApiManagement' 및 'Set-AzApiManagement': [-AssignIdentity] 매개 변수 이름을 [-SystemAssignedIdentity]로 변경</span><span class="sxs-lookup"><span data-stu-id="865fa-117">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="865fa-118">'New-AzApiManagement' 및 'Set-AzApiManagement': 새 매개 변수 추가: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="865fa-118">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="865fa-119">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="865fa-119">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="865fa-120">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="865fa-120">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="865fa-121">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="865fa-121">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="865fa-122">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="865fa-122">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="865fa-123">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="865fa-123">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="865fa-124">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="865fa-124">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="865fa-125">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="865fa-125">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="865fa-126">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="865fa-126">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="865fa-127">새 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementAuthorizationServer'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-127">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="865fa-128">새 'Get-AzApiManagementNamedValueSecretValue' cmdlet이 추가되었으며 'Get-AzApiManagementNamedValue'는 더 이상 비밀 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-128">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="865fa-129">새 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementOpenIdConnectProvider'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-129">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="865fa-130">새 'Get-AzApiManagementSubscriptionKey' cmdlet이 추가되었으며 'Get-AzApiManagementSubscription'은 더 이상 구독 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-130">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="865fa-131">새 'Get-AzApiManagementTenantAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-131">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="865fa-132">새 'Get-AzApiManagementTenantGitAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantGitAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-132">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="865fa-133">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-133">Az.ApplicationInsights</span></span>
* <span data-ttu-id="865fa-134">매개 변수 추가: 'New-AzApplicationInsights'에 대한 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="865fa-134">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="865fa-135">'Update-AzApplicationInsights' cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="865fa-135">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="865fa-136">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="865fa-136">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="865fa-137">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="865fa-137">Az.Batch</span></span>
* <span data-ttu-id="865fa-138">'Microsoft.Azure.Batch' SDK 버전 13.0.0 및 'Microsoft.Azure.Management.Batch' SDK 버전 9.0.0을 사용하도록 Az.Batch가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-138">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="865fa-139">새 '-CertificateKind' 매개 변수를 사용하여 'AzBatchCertificate'에 추가할 인증서 종류를 선택하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-139">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="865fa-140">이전에 항상 ''였던 'ApplicationPackages' 속성이 'PSApplication'에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-140">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="865fa-141">이제 'Get-AzBatchApplicationPackage'를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-141">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="865fa-142">예: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="865fa-142">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="865fa-143">'New-AzBatchPool'을 사용하여 풀을 만들 때 'PSImageReference'의 'VirtualMachineImageId' 속성은 이제 Shared Image Gallery 이미지만 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-143">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="865fa-144">'New-AzBatchPool'을 사용하여 풀을 만들 때 공용 IP 없이 'PSNetworkConfiguration'의 새 'PublicIPAddressConfiguration'을 사용하여 풀을 프로비저닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-144">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="865fa-145">'PSNetworkConfiguration'의 'PublicIPs' 속성도 'PSPublicIPAddressConfiguration'으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-145">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="865fa-146">이 속성은 'IPAddressProvisioningType'이 'UserManaged'인 경우에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-146">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-147">Az.Compute</span></span>
* <span data-ttu-id="865fa-148">'Update-AzVM' cmdlet에 HostId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-148">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="865fa-149">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' 및 'Set-AzVmssOsProfile' cmdlet의 도움말 문서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-149">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="865fa-150">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="865fa-150">Breaking changes</span></span>
    - <span data-ttu-id="865fa-151">'Get-AzVMImage' cmdlet에서 FilterExpression 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-151">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="865fa-152">'New-AzVmssConfig', 'New-AzVMConfig' 및 'Update-AzVM' cmdlet에서 AssignIdentity 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-152">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="865fa-153">'New-AzVmssConfig' 및 'Update-AzVmss' cmdlet에서 AutomaticRepairMaxInstanceRepairsPercent가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-153">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="865fa-154">ProximityPlacementGroup에서 AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus 및 VirtualMachineScaleSetsColocationStatus 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-154">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="865fa-155">AutomaticRepairsPolicy에서 MaxInstanceRepairsPercent 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-155">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="865fa-156">AvailabilitySets, VirtualMachines 및 VirtualMachineScaleSets 형식이 IList<SubResource>에서 IList<SubResourceWithColocationStatus>로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-156">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="865fa-157">'Get-AzVM' cmdlet에 대한 설명이 보다 정확하게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-157">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-158">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-158">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-159">Managed IR에서 데이터 흐름 런타임 속성의 CRUD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-159">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="865fa-160">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="865fa-160">Az.FrontDoor</span></span>
* <span data-ttu-id="865fa-161">Front Door 규칙 엔진 개체를 생성, 업데이트, 검색 및 삭제할 수 있는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-161">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="865fa-162">Front Door 규칙 엔진 개체를 작성할 수 있는 도우미 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-162">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="865fa-163">Front Door 회람 규칙 개체에 대한 규칙 엔진 참조 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-163">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="865fa-164">Front Door 백 엔드 개체에 Private Link 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-164">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="865fa-165">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="865fa-165">Az.Functions</span></span>
* <span data-ttu-id="865fa-166">''Az.Functions'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="865fa-166">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="865fa-167">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="865fa-167">Az.HDInsight</span></span>
* <span data-ttu-id="865fa-168">고객 관리형 키 디스크 암호화 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-168">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="865fa-169">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="865fa-169">Az.HealthcareApis</span></span>
* <span data-ttu-id="865fa-170">더 이상 액세스 정책이 기본적으로 현재 보안 주체로 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-170">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-171">Az.IotHub</span></span>
* <span data-ttu-id="865fa-172">SQL과 비슷한 언어를 사용하여 정보를 검색하기 위해 IoT 허브에서 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-172">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="865fa-173">'Add-AzIotHubDevice'가 자식 디바이스 없는 에지 지원 디바이스를 만들 수 없는 문제 해결 [#11597]</span><span class="sxs-lookup"><span data-stu-id="865fa-173">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="865fa-174">IoT Hub, 디바이스 또는 모듈에 대한 SAS 토큰을 생성하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-174">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="865fa-175">구성 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-175">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="865fa-176">IoT Edge 자동 배포를 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-176">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="865fa-177">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-177">New cmdlets are:</span></span>
    - <span data-ttu-id="865fa-178">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="865fa-178">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="865fa-179">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="865fa-179">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="865fa-180">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="865fa-180">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="865fa-181">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="865fa-181">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="865fa-182">IoT Edge 배포 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-182">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="865fa-183">지정된 에지 디바이스에 구성 콘텐츠를 적용하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-183">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-184">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-185">다음 별칭 제거: 'New-AzKeyVaultCertificateAdministratorDetails' 및 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="865fa-185">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="865fa-186">키 자격 증명 모음을 만들 때 기본적으로 일시 삭제 사용</span><span class="sxs-lookup"><span data-stu-id="865fa-186">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="865fa-187">키 자격 증명 모음을 만들 때 특정 네트워크 위치의 액세스를 제어하도록 네트워크 규칙을 설정할 수 있음</span><span class="sxs-lookup"><span data-stu-id="865fa-187">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="865fa-188">BYOK(Bring Your Own Key) 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-188">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="865fa-189">'Add-AzKeyVaultKey'가 키 교환 키 생성 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-189">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="865fa-190">'Get-AzKeyVaultKey'가 PEM 형식의 공개 키 다운로드 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-190">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="865fa-191">'AzKeyVaultKey' 도움말 문서의 'KeyOps' 부분 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-191">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-192">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-192">Az.Monitor</span></span>
* <span data-ttu-id="865fa-193">'Set-AzDiagnosticSettings'의 버그 수정, 일부 범주에는 보존 정책이 적용되지 않음 [#11589]</span><span class="sxs-lookup"><span data-stu-id="865fa-193">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="865fa-194">메트릭 경고 V2에 WebTest를 사용하기 위한 조건 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-194">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="865fa-195">'New-AzMetricAlertRuleV2Criteria': webtest 사용 조건을 만드는 옵션 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-195">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="865fa-196">'Add-AzMetricAlertRuleV2': 새 webtest 사용 조건 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-196">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="865fa-197">PSLogProfile에서 RetentionPolicy에 대한 중복 정의 제거 [#7608]</span><span class="sxs-lookup"><span data-stu-id="865fa-197">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="865fa-198">PSEventData에 정의된 중복 속성 제거 [#11353]</span><span class="sxs-lookup"><span data-stu-id="865fa-198">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="865fa-199">'Get-AzLog'를 'Get-AzActivityLog'로 이름 변경</span><span class="sxs-lookup"><span data-stu-id="865fa-199">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-200">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-200">Az.Network</span></span>
* <span data-ttu-id="865fa-201">영역 기본 동작이 변경된다는 것을 알리기 위해 주요 변경 특성을 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-201">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="865fa-202">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="865fa-202">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="865fa-203">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="865fa-203">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="865fa-204">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="865fa-204">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="865fa-205">새로운 최상위 리소스 SecurityPartnerProvider에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-205">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="865fa-206">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-206">New cmdlets added:</span></span>
        - <span data-ttu-id="865fa-207">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="865fa-207">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="865fa-208">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="865fa-208">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="865fa-209">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="865fa-209">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="865fa-210">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="865fa-210">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="865fa-211">'PSPrivateEndpointConnection'의 'PSPrivateLinkResource' 및 'GroupId'에서 'RequiredZoneNames' 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-211">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="865fa-212">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject에 대한 잘못된 형식의 SuccessThresholdRoundTripTimeMs 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-212">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="865fa-213">AllowVnetToVnetTraffic 인수의 기본값을 True로 설정하도록 VirtualWan cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-213">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="865fa-214">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="865fa-214">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="865fa-215">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="865fa-215">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="865fa-216">프라이빗 엔드포인트에 대한 DNS 영역 그룹을 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-216">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="865fa-217">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="865fa-217">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="865fa-218">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="865fa-218">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="865fa-219">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="865fa-219">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="865fa-220">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="865fa-220">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="865fa-221">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="865fa-221">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="865fa-222">'AzureFirewall'에 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' 및 'DNSServers' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-222">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="865fa-223">'AzureFirewall'에 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' 및 'DnsServer' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-223">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="865fa-224">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="865fa-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="865fa-225">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="865fa-225">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="865fa-226">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-226">Az.OperationalInsights</span></span>
* <span data-ttu-id="865fa-227">새로 생성된 SDK를 적용하도록 레거시 코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-227">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="865fa-228">사용되지 않는 API 때문에 cmdlet 삭제</span><span class="sxs-lookup"><span data-stu-id="865fa-228">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="865fa-229">'Get-AzOperationalInsightsSavedSearchResult'(별칭 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="865fa-229">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="865fa-230">'Get-AzOperationalInsightsSearchResult'(별칭 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="865fa-230">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="865fa-231">'Get-AzOperationalInsightsLinkTarget'(별칭 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="865fa-231">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="865fa-232">'Set-AzOperationalInsightsWorkspace' 및 'New-AzOperationalInsightsWorkspace'에 대한 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-232">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="865fa-233">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="865fa-233">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="865fa-234">클러스터 및 연결된 서비스에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="865fa-234">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-235">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-235">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-236">Azure Site Recovery - Azure와 Azure 공급자 간 근접 배치 그룹 가상 머신을 보호하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-236">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="865fa-237">Azure Site Recovery - 영역 간 복제에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-237">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="865fa-238">Azure Backup - Azure 파일 공유 복구 지점의 장기 보존 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-238">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="865fa-239">Azure Backup - 'Get-AzRecoveryServicesBackupItem' cmdlet 출력에 디스크 제외 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-239">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="865fa-240">사이트 복구 서비스용 Vault 자격 증명 파일에 대한 프라이빗 엔드포인트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-240">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-241">Az.Resources</span></span>
* <span data-ttu-id="865fa-242">새 역할 정의를 만들 때 보기 지연에 대한 메시지 경고 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-242">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="865fa-243">강력한 형식의 개체를 출력하도록 정책 cmdlet 변경</span><span class="sxs-lookup"><span data-stu-id="865fa-243">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="865fa-244">'Get-AzResourceLock' cmdlet에 사용되는 '-TenantLevel' 매개 변수 제거 [#11335]</span><span class="sxs-lookup"><span data-stu-id="865fa-244">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="865fa-245">'Remove-AzResourceGroup -Id ResourceId' 수정[#9882]</span><span class="sxs-lookup"><span data-stu-id="865fa-245">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="865fa-246">리소스 그룹 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="865fa-246">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="865fa-247">구독 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="865fa-247">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="865fa-248">별칭: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="865fa-248">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="865fa-249">ARM 템플릿 가상 시나리오 결과를 사용하도록 'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 대한 '-WhatIf' 및 '-Confirm' 매개 변수 재정의</span><span class="sxs-lookup"><span data-stu-id="865fa-249">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="865fa-250">배포 cmdlet에서 'ApiVersion' 매개 변수의 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-250">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="865fa-251">배포 오류에 대한 향상된 오류 메시지를 표시하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-251">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="865fa-252">배포 오류에 대한 correlationId 로깅 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-252">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="865fa-253">배포 스크립트 출력에 'error' 속성 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-253">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="865fa-254">nuget Microsoft.Azure.Management.ResourceManager를 '3.7.1-preview'로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-254">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="865fa-255">nuget 3.7.1-preview에서 DeploymentValidateResult의 Error 속성이 readonly로 변경되어 특정 테스트 사례를 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-255">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="865fa-256">SDK ResourceManager 3.7.1-preview의 GenericResourceExpanded 도입</span><span class="sxs-lookup"><span data-stu-id="865fa-256">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="865fa-257">모든 배포용 Get cmdlet에 대한 태그 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-257">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="865fa-258">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="865fa-258">'New-AzDeployment'</span></span>
    - <span data-ttu-id="865fa-259">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="865fa-259">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="865fa-260">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="865fa-260">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="865fa-261">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="865fa-261">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="865fa-262">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-262">Az.ServiceFabric</span></span>
* <span data-ttu-id="865fa-263">잘못된 인증서 지문을 가져오는 --SecretIdentifier를 사용한 인증서 추가의 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-263">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-264">Az.Sql</span></span>
* <span data-ttu-id="865fa-265">성능 강화:</span><span class="sxs-lookup"><span data-stu-id="865fa-265">Enhance performance of:</span></span>
    - <span data-ttu-id="865fa-266">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="865fa-266">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="865fa-267">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="865fa-267">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="865fa-268">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="865fa-268">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="865fa-269">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="865fa-269">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="865fa-270">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="865fa-270">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="865fa-271">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="865fa-271">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="865fa-272">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="865fa-272">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="865fa-273">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="865fa-273">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="865fa-274">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet에서 'RetentionDays' 매개 변수의 클라이언트 쪽 유효성 검사 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-274">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="865fa-275">Vnet에서 스토리지 계정을 감사하고, Storage Blob 데이터 기여자 역할을 만들 때 발생하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-275">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-276">Az.Storage</span></span>
* <span data-ttu-id="865fa-277">get/list account cmdlet 'Get-AzStorageAccount'에 '-AsJob' 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-277">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="865fa-278">키 자동 회전을 지원하기 위해 스토리지 계정을 KeyvaultEncryption으로 업데이트할 때 KeyVersion을 선택 사항으로 지정</span><span class="sxs-lookup"><span data-stu-id="865fa-278">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="865fa-279">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="865fa-279">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="865fa-280">파이프라인을 사용하여 Azure 파일 디렉터리 제거 오류 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-280">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="865fa-281">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="865fa-281">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="865fa-282">수정 [#9880]: Swagger에 맞게 NetWorkRule DefaultAction 값 정의 변경</span><span class="sxs-lookup"><span data-stu-id="865fa-282">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="865fa-283">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="865fa-283">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="865fa-284">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="865fa-284">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="865fa-285">수정 [#11624]: 서버 오류를 방지하기 위해 NetworkRules를 추가할 때 중복 규칙 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="865fa-285">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="865fa-286">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="865fa-286">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="865fa-287">Microsoft.Azure.Cosmos.Table SDK를 1.0.7로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="865fa-287">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="865fa-288">DataLake Gen2 항목 목록에 부품 항목만 반환되는 경우 ContinuationToken을 사용하여 다시 나열하라고 사용자에게 알리는 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-288">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="865fa-289">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="865fa-289">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="865fa-290">Azure Files Active Directory 도메인 서비스 인증을 사용하여 스토리지 계정을 만들거나 업데이트하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-290">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="865fa-291">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="865fa-291">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="865fa-292">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="865fa-292">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="865fa-293">스토리지 계정의 Kerberos 키 새로 만들기 또는 나열 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-293">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="865fa-294">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="865fa-294">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="865fa-295">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="865fa-295">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="865fa-296">스토리지 계정 장애 조치(failover) 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-296">Supported failover Storage account</span></span>
    - <span data-ttu-id="865fa-297">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="865fa-297">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="865fa-298">'Get-AzStorageBlobCopyState'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-298">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="865fa-299">'Get-AzStorageFileCopyState' 및 'Start-AzStorageBlobCopy'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-299">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="865fa-300">스토리지 클라이언트 라이브러리 v12를 큐 및 파일 cmdlet에 통합</span><span class="sxs-lookup"><span data-stu-id="865fa-300">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="865fa-301">출력 형식을 CloudFile에서 AzureStorageFile로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-301">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="865fa-302">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="865fa-302">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="865fa-303">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="865fa-303">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="865fa-304">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="865fa-304">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="865fa-305">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="865fa-305">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="865fa-306">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="865fa-306">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="865fa-307">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-307">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="865fa-308">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="865fa-308">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="865fa-309">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="865fa-309">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="865fa-310">출력 형식을 CloudFileShare에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-310">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="865fa-311">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="865fa-311">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="865fa-312">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="865fa-312">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="865fa-313">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="865fa-313">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="865fa-314">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 하위 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-314">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="865fa-315">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="865fa-315">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="865fa-316">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="865fa-316">Az.TrafficManager</span></span>
* <span data-ttu-id="865fa-317">'DisableAzureTrafficManagerEndpoint' 자세한 정보 출력에서 잘못된 프로필 이름 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-317">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-318">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-318">Az.Websites</span></span>
* <span data-ttu-id="865fa-319">'Update-AzWebAppAccessRestrictionConfig'의 도움말에서 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-319">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="865fa-320">3.8.0 - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="865fa-320">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="865fa-321">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="865fa-321">Highlights since the last release</span></span>
* <span data-ttu-id="865fa-322">Az.Storage에서 지원하는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="865fa-322">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="865fa-323">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-323">Az.Accounts</span></span>
* <span data-ttu-id="865fa-324">'Resolve-AzError'에서 Azure PowerShell 설문 조사 URL이 업데이트되었습니다. [#11507]</span><span class="sxs-lookup"><span data-stu-id="865fa-324">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="865fa-325">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-325">Az.ApiManagement</span></span>
* <span data-ttu-id="865fa-326">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-326">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="865fa-327">'Set-AzApiManagementGroup' - GroupId 매개 변수를 지정하도록 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-327">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="865fa-328">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="865fa-328">Az.Cdn</span></span>
* <span data-ttu-id="865fa-329">ChinaCDN 관련 가격 책정 SKU 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-329">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="865fa-330">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="865fa-330">Az.CognitiveServices</span></span>
* <span data-ttu-id="865fa-331">Identity, Encryption, UserOwnedStorage가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-331">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-332">Az.Compute</span></span>
* <span data-ttu-id="865fa-333">'Set-AzVmssOrchestrationServiceState' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-333">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="865fa-334">-InstanceView가 있는 'Get-AzVmss'는 OrchestrationService 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-334">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-335">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-335">Az.IotHub</span></span>
* <span data-ttu-id="865fa-336">IoT 디바이스 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-336">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="865fa-337">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="865fa-337">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="865fa-338">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="865fa-338">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="865fa-339">IoT Hub에서 디바이스에 대한 직접 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-339">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="865fa-340">IoT 디바이스 모듈 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-340">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="865fa-341">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="865fa-341">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="865fa-342">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="865fa-342">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="865fa-343">IoT 자동 디바이스 관리 구성을 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-343">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="865fa-344">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-344">New cmdlets are:</span></span>
    - <span data-ttu-id="865fa-345">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="865fa-345">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="865fa-346">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="865fa-346">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="865fa-347">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="865fa-347">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="865fa-348">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="865fa-348">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="865fa-349">Iot Hub에서 에지 모듈 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-349">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-350">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-351">자격 증명 모음에서 일시 삭제 및 제거 보호를 사용하도록 설정할 수 있는 새 cmdlet 'Update-AzKeyVault'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-351">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="865fa-352">Microsoft.PowerShell.SecretManagement에 대한 지원이 추가되었습니다. [#11178]</span><span class="sxs-lookup"><span data-stu-id="865fa-352">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="865fa-353">'Remove-AzKeyVaultManagedStorageSasDefinition' 예제의 오류가 해결되었습니다. [#11479]</span><span class="sxs-lookup"><span data-stu-id="865fa-353">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="865fa-354">프라이빗 엔드포인트에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-354">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="865fa-355">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="865fa-355">Az.Maintenance</span></span>
* <span data-ttu-id="865fa-356">GA용 유지 관리 cmdlet의 릴리스 버전 게시</span><span class="sxs-lookup"><span data-stu-id="865fa-356">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-357">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-357">Az.Monitor</span></span>
* <span data-ttu-id="865fa-358">프라이빗 링크 범위용 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-358">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="865fa-359">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="865fa-359">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="865fa-360">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="865fa-360">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="865fa-361">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="865fa-361">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="865fa-362">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="865fa-362">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="865fa-363">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="865fa-363">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="865fa-364">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="865fa-364">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="865fa-365">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="865fa-365">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-366">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-366">Az.Network</span></span>
* <span data-ttu-id="865fa-367">Virtual Network 게이트웨이의 개인 IP에 대한 연결을 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-367">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="865fa-368">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="865fa-368">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="865fa-369">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="865fa-369">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="865fa-370">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="865fa-370">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="865fa-371">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="865fa-371">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="865fa-372">FQDN 기반 LocalNetworkGateways 및 VpnSites를 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-372">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="865fa-373">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="865fa-373">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="865fa-374">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="865fa-374">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="865fa-375">ExpressRouteCircuitConnectionConfig(Global Reach)의 IPv6 주소 패밀리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-375">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="865fa-376">'Set-AzExpressRouteCircuitConnectionConfig'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-376">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="865fa-377">IPv6CircuitConnectionProperties를 포함한 모든 기존 속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-377">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="865fa-378">'Add-AzExpressRouteCircuitConnectionConfig'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-378">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="865fa-379">주소 접두사의 주소 패밀리를 지정하는 또 다른 선택적 매개 변수 AddressPrefixType이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-379">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="865fa-380">Virtual Network 게이트웨이 연결에서 DPD 시간 제한 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-380">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="865fa-381">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-381">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="865fa-382">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-382">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="865fa-383">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-383">Az.PolicyInsights</span></span>
* <span data-ttu-id="865fa-384">정책 준수 검사를 트리거하기 위한 'Start-AzPolicyComplianceScan' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-384">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="865fa-385">'Get-AzPolicyState' 출력에 정책 정의, 집합 정의 및 할당 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-385">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="865fa-386">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-386">Az.ServiceFabric</span></span>
* <span data-ttu-id="865fa-387">'New-AzServiceFabricCluster' 예제의 코드 서식 및 사용 편의성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-387">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-388">Az.Sql</span></span>
* <span data-ttu-id="865fa-389">'Get-AzSqlInstanceOperation' 및 'Stop-AzSqlInstanceOperation' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-389">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="865fa-390">VNet에서 스토리지 계정에 대한 감사가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-390">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-391">Az.Storage</span></span>
* <span data-ttu-id="865fa-392">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-392">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="865fa-393">스토리지 계정 생성/업데이트 시 새로운 SkuName StandardGZRS, StandardRAGZRS가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-393">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="865fa-394">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="865fa-394">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="865fa-395">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="865fa-395">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="865fa-396">DataLake Gen2가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-396">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="865fa-397">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="865fa-397">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="865fa-398">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="865fa-398">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="865fa-399">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="865fa-399">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="865fa-400">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="865fa-400">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="865fa-401">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="865fa-401">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="865fa-402">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="865fa-402">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="865fa-403">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="865fa-403">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="865fa-404">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="865fa-404">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="865fa-405">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="865fa-405">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="865fa-406">일반</span><span class="sxs-lookup"><span data-stu-id="865fa-406">General</span></span>
* <span data-ttu-id="865fa-407">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-407">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="865fa-408">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-408">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="865fa-409">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](https://aka.ms/az4AzureStack)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-409">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="865fa-410">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-410">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="865fa-411">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="865fa-411">Az.Billing</span></span>
  - <span data-ttu-id="865fa-412">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-412">Az.Compute</span></span>
  - <span data-ttu-id="865fa-413">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="865fa-413">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="865fa-414">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="865fa-414">Az.EventHub</span></span>
  - <span data-ttu-id="865fa-415">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-415">Az.IotHub</span></span>
  - <span data-ttu-id="865fa-416">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-416">Az.KeyVault</span></span>
  - <span data-ttu-id="865fa-417">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-417">Az.Monitor</span></span>
  - <span data-ttu-id="865fa-418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-418">Az.Network</span></span>
  - <span data-ttu-id="865fa-419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-419">Az.Resources</span></span>
  - <span data-ttu-id="865fa-420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-420">Az.Storage</span></span>
  - <span data-ttu-id="865fa-421">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-421">Az.Websites</span></span>
* <span data-ttu-id="865fa-422">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-422">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="865fa-423">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-423">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="865fa-424">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](https://aka.ms/InstallASHPowerShell)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-424">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="865fa-425">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="865fa-425">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-426">Az.Accounts</span></span>
* <span data-ttu-id="865fa-427">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="865fa-427">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-428">Az.Compute</span></span>
* <span data-ttu-id="865fa-429">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-429">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="865fa-430">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="865fa-430">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="865fa-431">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-431">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="865fa-432">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-432">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="865fa-433">[#11354]</span><span class="sxs-lookup"><span data-stu-id="865fa-433">[#11354]</span></span>
* <span data-ttu-id="865fa-434">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-434">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="865fa-435">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="865fa-435">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="865fa-436">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="865fa-436">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="865fa-437">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="865fa-437">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="865fa-438">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="865fa-438">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="865fa-439">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-439">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="865fa-440">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-440">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="865fa-441">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-441">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="865fa-442">[#11257]</span><span class="sxs-lookup"><span data-stu-id="865fa-442">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-443">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-443">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-444">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-444">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="865fa-445">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-445">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-446">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-446">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-447">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-447">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="865fa-448">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-448">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="865fa-449">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="865fa-449">Az.HDInsight</span></span>
* <span data-ttu-id="865fa-450">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-450">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-451">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-451">Az.IotHub</span></span>
* <span data-ttu-id="865fa-452">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-452">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="865fa-453">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-453">New Cmdlets are:</span></span>
    - <span data-ttu-id="865fa-454">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="865fa-454">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="865fa-455">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="865fa-455">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-456">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-457">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-457">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-458">Az.Monitor</span></span>
* <span data-ttu-id="865fa-459">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-459">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-460">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-460">Az.Network</span></span>
* <span data-ttu-id="865fa-461">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-461">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="865fa-462">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="865fa-462">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="865fa-463">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="865fa-463">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="865fa-464">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="865fa-464">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="865fa-465">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="865fa-465">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="865fa-466">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-466">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="865fa-467">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-467">Az.PolicyInsights</span></span>
* <span data-ttu-id="865fa-468">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-468">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-470">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-470">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="865fa-471">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-471">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="865fa-472">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-472">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="865fa-473">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-473">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="865fa-474">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-474">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="865fa-475">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-475">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-476">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-476">Az.Resources</span></span>
* <span data-ttu-id="865fa-477">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="865fa-477">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="865fa-478">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-478">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="865fa-479">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-479">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="865fa-480">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-480">Added example.</span></span>
* <span data-ttu-id="865fa-481">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="865fa-481">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="865fa-482">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-482">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-483">Az.Sql</span></span>
* <span data-ttu-id="865fa-484">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-484">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="865fa-485">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-485">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="865fa-486">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-486">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="865fa-487">Az.Support</span><span class="sxs-lookup"><span data-stu-id="865fa-487">Az.Support</span></span>
* <span data-ttu-id="865fa-488">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="865fa-488">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-489">Az.Websites</span></span>
* <span data-ttu-id="865fa-490">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-490">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="865fa-491">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="865fa-491">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="865fa-492">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="865fa-492">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="865fa-493">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="865fa-493">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="865fa-494">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="865fa-494">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="865fa-495">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="865fa-495">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-496">Az.Accounts</span></span>
* <span data-ttu-id="865fa-497">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="865fa-497">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="865fa-498">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="865fa-498">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="865fa-499">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-499">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="865fa-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-500">Az.ApiManagement</span></span>
* <span data-ttu-id="865fa-501">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="865fa-501">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="865fa-502">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="865fa-502">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="865fa-503">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-503">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="865fa-504">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="865fa-504">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-506">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-506">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-507">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-507">Az.IotHub</span></span>
* <span data-ttu-id="865fa-508">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-508">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="865fa-509">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-509">New Cmdlets are:</span></span>
    - <span data-ttu-id="865fa-510">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="865fa-510">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="865fa-511">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="865fa-511">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="865fa-512">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="865fa-512">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="865fa-513">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="865fa-513">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="865fa-514">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-514">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="865fa-515">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-515">New Cmdlets are:</span></span>
    - <span data-ttu-id="865fa-516">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="865fa-516">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="865fa-517">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="865fa-517">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="865fa-518">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="865fa-518">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="865fa-519">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="865fa-519">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="865fa-520">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-520">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="865fa-521">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-521">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="865fa-522">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-522">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="865fa-523">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-523">New Cmdlets are:</span></span>
    - <span data-ttu-id="865fa-524">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="865fa-524">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="865fa-525">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="865fa-525">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="865fa-526">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-526">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-527">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-527">Az.Monitor</span></span>
* <span data-ttu-id="865fa-528">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="865fa-528">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-529">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-529">Az.Network</span></span>
* <span data-ttu-id="865fa-530">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-530">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="865fa-531">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-531">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="865fa-532">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-532">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="865fa-533">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-533">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-534">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-534">Az.Resources</span></span>
* <span data-ttu-id="865fa-535">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-535">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="865fa-536">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="865fa-536">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="865fa-537">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="865fa-537">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="865fa-538">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="865fa-538">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="865fa-539">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-539">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="865fa-540">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-540">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="865fa-541">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-541">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="865fa-542">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-542">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="865fa-543">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="865fa-543">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="865fa-544">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="865fa-544">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="865fa-545">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="865fa-545">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="865fa-546">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-546">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="865fa-547">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="865fa-547">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="865fa-548">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-548">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-549">Az.Sql</span></span>
* <span data-ttu-id="865fa-550">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-550">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="865fa-551">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-551">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="865fa-552">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-552">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="865fa-553">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-553">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="865fa-554">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-554">Remove an LTR backup</span></span>
    - <span data-ttu-id="865fa-555">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-555">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="865fa-556">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-556">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="865fa-557">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-557">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="865fa-558">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-558">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-559">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-559">Az.Storage</span></span>
* <span data-ttu-id="865fa-560">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-560">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="865fa-561">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="865fa-561">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="865fa-562">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-562">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="865fa-563">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="865fa-563">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="865fa-564">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="865fa-564">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-565">Az.Websites</span></span>
* <span data-ttu-id="865fa-566">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-566">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="865fa-567">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-567">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="865fa-568">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-568">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="865fa-569">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-569">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="865fa-570">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-570">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="865fa-571">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="865fa-571">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="865fa-572">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="865fa-572">Highlights since the last major release</span></span>
* <span data-ttu-id="865fa-573">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-573">Updated client side telemetry.</span></span>
* <span data-ttu-id="865fa-574">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-574">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="865fa-575">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-575">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="865fa-576">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-576">Az.Accounts</span></span>
* <span data-ttu-id="865fa-577">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-577">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-578">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-578">Az.Automation</span></span>
* <span data-ttu-id="865fa-579">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-579">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="865fa-580">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="865fa-580">Az.CognitiveServices</span></span>
* <span data-ttu-id="865fa-581">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-581">Updated SDK to 7.0</span></span>
* <span data-ttu-id="865fa-582">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-582">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-583">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-583">Az.Compute</span></span>
* <span data-ttu-id="865fa-584">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-584">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="865fa-585">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="865fa-585">Az.FrontDoor</span></span>
* <span data-ttu-id="865fa-586">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-586">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-587">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-587">Az.IotHub</span></span>
* <span data-ttu-id="865fa-588">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-588">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="865fa-589">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-589">New Cmdlets are:</span></span>
    - <span data-ttu-id="865fa-590">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="865fa-590">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="865fa-591">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="865fa-591">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="865fa-592">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="865fa-592">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="865fa-593">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="865fa-593">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-594">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-594">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-595">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-595">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-596">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-596">Az.Monitor</span></span>
* <span data-ttu-id="865fa-597">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-597">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="865fa-598">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-598">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="865fa-599">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-599">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-600">Az.Network</span></span>
* <span data-ttu-id="865fa-601">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-601">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="865fa-602">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-602">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="865fa-603">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-603">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="865fa-604">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="865fa-604">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="865fa-605">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-605">No new cmdlets are added.</span></span> <span data-ttu-id="865fa-606">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-606">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-608">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-608">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-609">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-609">Az.Resources</span></span>
* <span data-ttu-id="865fa-610">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-610">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="865fa-611">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-611">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="865fa-612">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-612">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="865fa-613">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-613">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="865fa-614">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-614">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="865fa-615">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-615">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="865fa-616">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-616">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="865fa-617">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-617">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-618">Az.Sql</span></span>
* <span data-ttu-id="865fa-619">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-619">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="865fa-620">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-620">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="865fa-621">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-621">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="865fa-622">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="865fa-622">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="865fa-623">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-623">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="865fa-624">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="865fa-624">Az.StorageSync</span></span>
* <span data-ttu-id="865fa-625">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-625">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="865fa-626">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="865fa-626">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="865fa-627">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="865fa-627">Highlights since the last major release</span></span>
* <span data-ttu-id="865fa-628">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="865fa-628">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="865fa-629">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-629">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="865fa-630">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-630">Az.Accounts</span></span>
* <span data-ttu-id="865fa-631">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="865fa-631">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="865fa-632">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-632">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="865fa-633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-633">Az.ApiManagement</span></span>
* <span data-ttu-id="865fa-634">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="865fa-634">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="865fa-635">**New-AzApiManagementProduct**\* 및 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="865fa-635">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="865fa-636">https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-636">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="865fa-637">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-637">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-638">Az.Compute</span></span>
* <span data-ttu-id="865fa-639">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="865fa-639">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="865fa-640">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-640">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="865fa-641">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="865fa-641">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="865fa-642">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-642">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="865fa-643">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-643">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-644">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-644">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-645">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-645">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="865fa-646">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="865fa-646">Az.DeploymentManager</span></span>
* <span data-ttu-id="865fa-647">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-647">Adds LIST operations for resources</span></span>
* <span data-ttu-id="865fa-648">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-648">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="865fa-649">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="865fa-649">Az.HDInsight</span></span>
* <span data-ttu-id="865fa-650">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-650">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-651">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-652">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-652">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-653">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-653">Az.Network</span></span>
* <span data-ttu-id="865fa-654">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-654">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="865fa-655">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="865fa-655">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="865fa-656">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="865fa-656">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="865fa-657">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-657">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="865fa-658">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="865fa-658">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="865fa-659">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-659">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="865fa-660">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-660">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="865fa-661">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-661">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="865fa-662">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-662">New cmdlets added:</span></span>
        - <span data-ttu-id="865fa-663">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="865fa-663">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="865fa-664">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="865fa-664">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="865fa-665">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="865fa-665">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="865fa-666">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-666">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="865fa-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="865fa-668">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-668">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="865fa-669">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-669">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="865fa-670">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-670">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="865fa-671">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-671">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-673">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-673">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="865fa-674">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-674">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-675">Az.Resources</span></span>
* <span data-ttu-id="865fa-676">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="865fa-676">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="865fa-677">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-677">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-678">Az.Sql</span></span>
<span data-ttu-id="865fa-679">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-679">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-680">Az.Storage</span></span>
* <span data-ttu-id="865fa-681">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-681">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="865fa-682">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-682">New-AzStorageAccount</span></span>
* <span data-ttu-id="865fa-683">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="865fa-683">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="865fa-684">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-684">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-685">Az.Websites</span></span>
* <span data-ttu-id="865fa-686">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-686">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="865fa-687">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-687">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="865fa-688">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="865fa-688">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-689">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-689">Az.Accounts</span></span>
* <span data-ttu-id="865fa-690">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-690">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="865fa-691">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="865fa-691">Az.Cdn</span></span>
* <span data-ttu-id="865fa-692">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="865fa-692">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-693">Az.Compute</span></span>
* <span data-ttu-id="865fa-694">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-694">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="865fa-695">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="865fa-695">Az.ContainerInstance</span></span>
* <span data-ttu-id="865fa-696">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="865fa-696">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="865fa-697">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="865fa-697">Az.DataBoxEdge</span></span>
* <span data-ttu-id="865fa-698">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-698">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="865fa-699">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="865fa-699">Get the Edge Storage Container</span></span>
* <span data-ttu-id="865fa-700">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-700">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="865fa-701">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-701">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="865fa-702">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-702">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="865fa-703">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-703">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="865fa-704">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-704">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="865fa-705">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="865fa-705">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="865fa-706">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-706">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="865fa-707">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="865fa-707">Get the Edge Storage Account</span></span>
* <span data-ttu-id="865fa-708">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-708">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="865fa-709">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-709">Create new Edge Storage Account</span></span>
* <span data-ttu-id="865fa-710">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-710">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="865fa-711">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-711">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="865fa-712">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="865fa-712">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="865fa-713">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="865fa-713">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="865fa-714">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-714">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="865fa-715">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="865fa-715">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-716">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-717">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-717">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="865fa-718">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-718">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="865fa-719">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-719">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="865fa-720">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="865fa-720">Az.DevTestLabs</span></span>
* <span data-ttu-id="865fa-721">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-721">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="865fa-722">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="865fa-722">Az.EventHub</span></span>
* <span data-ttu-id="865fa-723">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-723">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="865fa-724">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="865fa-724">Az.HDInsight</span></span>
* <span data-ttu-id="865fa-725">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-725">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="865fa-726">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="865fa-726">Az.MachineLearning</span></span>
* <span data-ttu-id="865fa-727">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-727">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="865fa-728">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="865fa-728">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="865fa-729">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="865fa-729">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="865fa-730">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="865fa-730">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="865fa-731">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="865fa-731">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="865fa-732">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="865fa-732">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="865fa-733">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="865fa-733">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="865fa-734">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="865fa-734">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-735">Az.Network</span></span>
* <span data-ttu-id="865fa-736">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="865fa-736">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-737">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-737">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-738">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-738">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="865fa-739">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-739">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="865fa-740">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-740">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="865fa-741">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-741">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-742">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-742">Az.Resources</span></span>
* <span data-ttu-id="865fa-743">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-743">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-744">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-744">Az.Sql</span></span>
* <span data-ttu-id="865fa-745">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-745">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="865fa-746">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-746">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="865fa-747">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="865fa-747">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="865fa-748">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-748">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-749">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-749">Az.Storage</span></span>
* <span data-ttu-id="865fa-750">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-750">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="865fa-751">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="865fa-751">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="865fa-752">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-752">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="865fa-753">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-753">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="865fa-754">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="865fa-754">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="865fa-755">일반</span><span class="sxs-lookup"><span data-stu-id="865fa-755">General</span></span>
* <span data-ttu-id="865fa-756">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-756">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="865fa-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-757">Az.Accounts</span></span>
* <span data-ttu-id="865fa-758">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="865fa-758">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="865fa-759">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="865fa-759">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="865fa-760">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="865fa-760">Az.Batch</span></span>
* <span data-ttu-id="865fa-761">**New-AzBatchPool**이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-761">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-762">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-763">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-763">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="865fa-764">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="865fa-764">Az.FrontDoor</span></span>
* <span data-ttu-id="865fa-765">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-765">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="865fa-766">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-766">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="865fa-767">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="865fa-767">Az.HealthcareApis</span></span>
* <span data-ttu-id="865fa-768">예외 처리</span><span class="sxs-lookup"><span data-stu-id="865fa-768">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-769">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-769">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-770">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-770">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="865fa-771">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="865fa-771">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="865fa-772">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-772">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-773">Az.Monitor</span></span>
* <span data-ttu-id="865fa-774">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-774">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="865fa-775">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="865fa-775">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="865fa-776">나타냄</span><span class="sxs-lookup"><span data-stu-id="865fa-776">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-777">Az.Network</span></span>
* <span data-ttu-id="865fa-778">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="865fa-778">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-779">Az.Resources</span></span>
* <span data-ttu-id="865fa-780">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="865fa-780">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="865fa-781">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="865fa-781">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-782">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-782">Az.Sql</span></span>
* <span data-ttu-id="865fa-783">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="865fa-783">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-784">Az.Storage</span></span>
* <span data-ttu-id="865fa-785">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-785">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="865fa-786">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="865fa-786">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="865fa-787">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="865fa-787">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="865fa-788">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-788">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="865fa-789">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="865fa-789">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="865fa-790">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="865fa-790">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="865fa-791">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-791">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="865fa-792">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="865fa-792">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="865fa-793">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="865fa-793">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="865fa-794">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-794">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="865fa-795">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="865fa-795">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="865fa-796">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-796">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="865fa-797">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="865fa-797">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="865fa-798">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="865fa-798">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="865fa-799">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="865fa-799">Highlights since the last major release</span></span>
* <span data-ttu-id="865fa-800">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="865fa-800">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="865fa-801">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="865fa-801">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-802">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-802">Az.Compute</span></span>
* <span data-ttu-id="865fa-803">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="865fa-803">VM Reapply feature</span></span>
    - <span data-ttu-id="865fa-804">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-804">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="865fa-805">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="865fa-805">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="865fa-806">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="865fa-806">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="865fa-807">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-807">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="865fa-808">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-808">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="865fa-809">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-809">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="865fa-810">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="865fa-810">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="865fa-811">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-811">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="865fa-812">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-812">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="865fa-813">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-813">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="865fa-814">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="865fa-814">Az.DataBoxEdge</span></span>
* <span data-ttu-id="865fa-815">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-815">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="865fa-816">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="865fa-816">Get the Order</span></span>
* <span data-ttu-id="865fa-817">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-817">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="865fa-818">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-818">Create new Order</span></span>
* <span data-ttu-id="865fa-819">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-819">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="865fa-820">주문 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-820">Remove the Order</span></span>
* <span data-ttu-id="865fa-821">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="865fa-821">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="865fa-822">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="865fa-822">Now creates Local Share</span></span>
* <span data-ttu-id="865fa-823">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-823">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="865fa-824">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="865fa-824">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="865fa-825">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-825">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="865fa-826">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="865fa-826">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="865fa-827">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-827">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="865fa-828">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="865fa-828">Gets the information about Triggers</span></span>
* <span data-ttu-id="865fa-829">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-829">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="865fa-830">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-830">Create new Triggers</span></span>
* <span data-ttu-id="865fa-831">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-831">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="865fa-832">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-832">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-833">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-833">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-834">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-834">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="865fa-835">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-835">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-836">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-837">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-837">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="865fa-838">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="865fa-838">Az.EventHub</span></span>
* <span data-ttu-id="865fa-839">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-839">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="865fa-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="865fa-840">Az.FrontDoor</span></span>
* <span data-ttu-id="865fa-841">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-841">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="865fa-842">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-842">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="865fa-843">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-843">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="865fa-844">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="865fa-844">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-845">Az.Network</span></span>
* <span data-ttu-id="865fa-846">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-846">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="865fa-847">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="865fa-847">Az.PrivateDns</span></span>
* <span data-ttu-id="865fa-848">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="865fa-848">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-849">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-849">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-850">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-850">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="865fa-851">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-851">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="865fa-852">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-852">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="865fa-853">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="865fa-853">Az.RedisCache</span></span>
* <span data-ttu-id="865fa-854">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-854">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="865fa-855">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-855">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="865fa-856">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-856">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-857">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-857">Az.Resources</span></span>
- <span data-ttu-id="865fa-858">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-858">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="865fa-859">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-859">Updated create policy definition help example</span></span>
- <span data-ttu-id="865fa-860">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-860">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="865fa-861">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-861">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="865fa-862">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-862">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-863">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-863">Az.Sql</span></span>
* <span data-ttu-id="865fa-864">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-864">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="865fa-865">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-865">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="865fa-866">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="865fa-866">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="865fa-867">일반</span><span class="sxs-lookup"><span data-stu-id="865fa-867">General</span></span>
* <span data-ttu-id="865fa-868">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="865fa-868">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="865fa-869">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-869">Az.Accounts</span></span>
* <span data-ttu-id="865fa-870">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-870">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="865fa-871">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="865fa-871">Az.Advisor</span></span>
* <span data-ttu-id="865fa-872">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-872">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="865fa-873">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="865fa-873">Az.Batch</span></span>
* <span data-ttu-id="865fa-874">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-874">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="865fa-875">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-875">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="865fa-876">이 변경 사항은 **Get-AzBatchAccount**에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-876">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="865fa-877">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-877">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="865fa-878">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-878">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="865fa-879">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask**에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-879">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="865fa-880">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-880">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="865fa-881">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-881">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="865fa-882">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-882">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="865fa-883">**Get-AzBatchApplication**으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-883">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="865fa-884">이제 **Get-AzBatchApplicationPackage**를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-884">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="865fa-885">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="865fa-885">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="865fa-886">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication**에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-886">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="865fa-887">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-887">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="865fa-888">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-888">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="865fa-889">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-889">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="865fa-890">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-890">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="865fa-891">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-891">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="865fa-892">**Set-AzBatchPoolOSVersion**이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-892">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="865fa-893">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-893">This operation is no longer supported.</span></span>
* <span data-ttu-id="865fa-894">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-894">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="865fa-895">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-895">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="865fa-896">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-896">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="865fa-897">**Get-AzBatchNodeAgentSku**가 제거되고 **Get-AzBatchSupportedImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-897">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="865fa-898">**Get-AzBatchSupportedImage**가 **Get-AzBatchNodeAgentSku**와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-898">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="865fa-899">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-899">New non-verified images are also now returned.</span></span> <span data-ttu-id="865fa-900">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-900">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="865fa-901">**New-AzBatchPool**의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-901">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="865fa-902">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-902">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="865fa-903">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-903">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="865fa-904">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-904">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="865fa-905">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-905">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="865fa-906">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-906">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="865fa-907">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-907">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="865fa-908">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="865fa-908">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="865fa-909">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="865fa-909">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="865fa-910">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="865fa-910">Az.Cdn</span></span>
* <span data-ttu-id="865fa-911">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-911">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="865fa-912">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-912">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-913">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-913">Az.Compute</span></span>
* <span data-ttu-id="865fa-914">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="865fa-914">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="865fa-915">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="865fa-915">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="865fa-916">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="865fa-916">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="865fa-917">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-917">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="865fa-918">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-918">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="865fa-919">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="865fa-919">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="865fa-920">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-920">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="865fa-921">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="865fa-921">Breaking changes</span></span>
    - <span data-ttu-id="865fa-922">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-922">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="865fa-923">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-923">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-924">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-924">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-925">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-925">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-927">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="865fa-927">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="865fa-928">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-928">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="865fa-929">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="865fa-929">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="865fa-930">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-930">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="865fa-931">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-931">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="865fa-932">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-932">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="865fa-933">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="865fa-933">Az.FrontDoor</span></span>
* <span data-ttu-id="865fa-934">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-934">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="865fa-935">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="865fa-935">Az.HDInsight</span></span>
* <span data-ttu-id="865fa-936">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-936">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="865fa-937">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-937">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="865fa-938">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="865fa-938">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="865fa-939">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-939">Removed five cmdlets:</span></span>
    - <span data-ttu-id="865fa-940">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="865fa-940">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="865fa-941">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="865fa-941">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="865fa-942">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="865fa-942">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="865fa-943">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="865fa-943">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="865fa-944">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="865fa-944">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="865fa-945">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-945">Added three cmdlets:</span></span>
    - <span data-ttu-id="865fa-946">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="865fa-946">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="865fa-947">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="865fa-947">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="865fa-948">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="865fa-948">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="865fa-949">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-949">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="865fa-950">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-950">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="865fa-951">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-951">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="865fa-952">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-952">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="865fa-953">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-953">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="865fa-954">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-954">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="865fa-955">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-955">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="865fa-956">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-956">Added some scenario test cases.</span></span>
* <span data-ttu-id="865fa-957">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="865fa-957">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-958">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-958">Az.IotHub</span></span>
* <span data-ttu-id="865fa-959">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="865fa-959">Breaking changes:</span></span>
    - <span data-ttu-id="865fa-960">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-960">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="865fa-961">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-961">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="865fa-962">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-962">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="865fa-963">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-963">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="865fa-964">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-964">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="865fa-965">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-965">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="865fa-966">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-966">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="865fa-967">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-967">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="865fa-968">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-968">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="865fa-969">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-969">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="865fa-970">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-970">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="865fa-971">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-971">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-972">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-972">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-973">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-973">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="865fa-974">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-974">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="865fa-975">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-975">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="865fa-976">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-976">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="865fa-977">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-977">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="865fa-978">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-978">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="865fa-979">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-979">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="865fa-980">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-980">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="865fa-981">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-981">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-982">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-982">Az.Resources</span></span>
* <span data-ttu-id="865fa-983">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-983">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-984">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-984">Az.Network</span></span>
* <span data-ttu-id="865fa-985">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-985">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="865fa-986">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="865fa-986">Updated cmdlet:</span></span>
        - <span data-ttu-id="865fa-987">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-987">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="865fa-988">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-988">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="865fa-989">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-989">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="865fa-990">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-990">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="865fa-991">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-991">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="865fa-992">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-992">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="865fa-993">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="865fa-993">New cmdlet:</span></span>
        - <span data-ttu-id="865fa-994">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="865fa-994">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="865fa-995">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-995">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="865fa-996">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-996">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="865fa-997">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-997">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="865fa-998">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-998">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="865fa-999">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-999">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="865fa-1000">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-1000">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="865fa-1001">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1001">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="865fa-1002">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1002">New cmdlets added:</span></span>
        - <span data-ttu-id="865fa-1003">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="865fa-1003">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="865fa-1004">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="865fa-1004">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="865fa-1005">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="865fa-1005">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="865fa-1006">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="865fa-1006">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="865fa-1007">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="865fa-1007">Set-AzVirtualHub</span></span>
* <span data-ttu-id="865fa-1008">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1008">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="865fa-1009">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1009">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="865fa-1010">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="865fa-1010">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="865fa-1011">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="865fa-1011">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="865fa-1012">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="865fa-1012">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="865fa-1013">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="865fa-1013">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="865fa-1014">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1014">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="865fa-1015">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1015">New cmdlets added:</span></span>
        - <span data-ttu-id="865fa-1016">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-1016">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="865fa-1017">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1017">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="865fa-1018">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="865fa-1018">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="865fa-1019">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="865fa-1019">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="865fa-1020">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="865fa-1020">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="865fa-1021">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="865fa-1021">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="865fa-1022">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="865fa-1022">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="865fa-1023">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1023">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="865fa-1024">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1024">New cmdlets added:</span></span>
        - <span data-ttu-id="865fa-1025">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="865fa-1025">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="865fa-1026">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="865fa-1026">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="865fa-1027">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="865fa-1027">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="865fa-1028">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="865fa-1028">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="865fa-1029">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="865fa-1029">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="865fa-1030">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="865fa-1030">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="865fa-1031">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1031">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="865fa-1032">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="865fa-1032">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="865fa-1033">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1033">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="865fa-1034">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1034">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="865fa-1035">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1035">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="865fa-1036">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1036">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="865fa-1037">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="865fa-1037">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="865fa-1038">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="865fa-1038">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="865fa-1039">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1039">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="865fa-1040">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1040">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="865fa-1041">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1041">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="865fa-1042">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1042">New cmdlets added:</span></span>
        - <span data-ttu-id="865fa-1043">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="865fa-1043">New-AzIpGroup</span></span>
        - <span data-ttu-id="865fa-1044">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="865fa-1044">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="865fa-1045">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="865fa-1045">Get-AzIpGroup</span></span>
        - <span data-ttu-id="865fa-1046">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="865fa-1046">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="865fa-1047">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-1047">Az.ServiceFabric</span></span>
* <span data-ttu-id="865fa-1048">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1048">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1049">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1049">Az.Sql</span></span>
* <span data-ttu-id="865fa-1050">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1050">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="865fa-1051">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1051">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="865fa-1052">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1052">Removed deprecated aliases:</span></span>
* <span data-ttu-id="865fa-1053">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="865fa-1053">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="865fa-1054">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="865fa-1054">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="865fa-1055">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-1055">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="865fa-1056">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-1056">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="865fa-1057">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="865fa-1057">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="865fa-1058">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1058">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-1059">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-1059">Az.Storage</span></span>
* <span data-ttu-id="865fa-1060">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1060">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="865fa-1061">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-1061">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="865fa-1062">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-1062">Set-AzStorageAccount</span></span>
* <span data-ttu-id="865fa-1063">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1063">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="865fa-1064">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="865fa-1064">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="865fa-1065">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="865fa-1065">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="865fa-1066">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="865fa-1066">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="865fa-1067">일반</span><span class="sxs-lookup"><span data-stu-id="865fa-1067">General</span></span>
* <span data-ttu-id="865fa-1068">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="865fa-1068">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="865fa-1069">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-1069">Az.Accounts</span></span>
* <span data-ttu-id="865fa-1070">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1070">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="865fa-1071">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-1071">Az.ApiManagement</span></span>
* <span data-ttu-id="865fa-1072">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1072">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="865fa-1073">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1073">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-1074">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-1074">Az.Automation</span></span>
* <span data-ttu-id="865fa-1075">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1075">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="865fa-1076">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="865fa-1076">Az.Batch</span></span>
* <span data-ttu-id="865fa-1077">**Get-AzBatchNodeAgentSku**가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1077">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1078">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1078">Az.Compute</span></span>
* <span data-ttu-id="865fa-1079">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1079">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="865fa-1080">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1080">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="865fa-1081">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1081">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="865fa-1082">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1082">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-1083">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-1083">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-1084">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1084">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="865fa-1085">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1085">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="865fa-1086">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1086">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-1088">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1088">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="865fa-1089">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="865fa-1089">Az.HealthcareApis</span></span>
* <span data-ttu-id="865fa-1090">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1090">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="865fa-1091">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1091">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="865fa-1092">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1092">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="865fa-1093">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1093">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-1094">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-1094">Az.IotHub</span></span>
* <span data-ttu-id="865fa-1095">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="865fa-1095">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="865fa-1096">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1096">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-1097">Az.Monitor</span></span>
* <span data-ttu-id="865fa-1098">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1098">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="865fa-1099">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1099">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="865fa-1100">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1100">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="865fa-1101">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1101">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1102">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1102">Az.Network</span></span>
* <span data-ttu-id="865fa-1103">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1103">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="865fa-1104">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1104">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="865fa-1105">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1105">New cmdlets added:</span></span>
        - <span data-ttu-id="865fa-1106">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="865fa-1106">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="865fa-1107">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1107">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="865fa-1108">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1108">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="865fa-1109">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1109">Updated cmdlets:</span></span>
        - <span data-ttu-id="865fa-1110">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1110">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="865fa-1111">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1111">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="865fa-1112">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1112">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="865fa-1113">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1113">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="865fa-1114">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="865fa-1114">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="865fa-1115">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1115">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="865fa-1116">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1116">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="865fa-1117">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="865fa-1117">Az.RedisCache</span></span>
* <span data-ttu-id="865fa-1118">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1118">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1119">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1119">Az.Sql</span></span>
* <span data-ttu-id="865fa-1120">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1120">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-1121">Az.Storage</span></span>
* <span data-ttu-id="865fa-1122">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1122">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="865fa-1123">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1123">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="865fa-1124">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="865fa-1124">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="865fa-1125">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1125">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="865fa-1126">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-1126">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="865fa-1127">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="865fa-1127">Az.StorageSync</span></span>
* <span data-ttu-id="865fa-1128">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1128">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-1129">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-1129">Az.Websites</span></span>
* <span data-ttu-id="865fa-1130">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1130">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="865fa-1131">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="865fa-1131">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="865fa-1132">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-1132">Az.ApiManagement</span></span>
* <span data-ttu-id="865fa-1133">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1133">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="865fa-1134">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1134">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="865fa-1135">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1135">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-1136">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-1136">Az.Automation</span></span>
* <span data-ttu-id="865fa-1137">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1137">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="865fa-1138">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1138">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="865fa-1139">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1139">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1140">Az.Compute</span></span>
* <span data-ttu-id="865fa-1141">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1141">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="865fa-1142">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1142">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="865fa-1143">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1143">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="865fa-1144">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1144">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="865fa-1145">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1145">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="865fa-1146">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1146">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="865fa-1147">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1147">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="865fa-1148">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1148">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="865fa-1149">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1149">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-1150">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-1151">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1151">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="865fa-1152">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1152">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="865fa-1153">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="865fa-1153">Az.HDInsight</span></span>
* <span data-ttu-id="865fa-1154">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="865fa-1154">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-1155">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-1155">Az.IotHub</span></span>
* <span data-ttu-id="865fa-1156">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1156">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="865fa-1157">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1157">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="865fa-1158">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1158">New cmdlets are:</span></span>
    - <span data-ttu-id="865fa-1159">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="865fa-1159">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="865fa-1160">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="865fa-1160">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="865fa-1161">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="865fa-1161">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="865fa-1162">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="865fa-1162">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-1163">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-1163">Az.Monitor</span></span>
* <span data-ttu-id="865fa-1164">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1164">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="865fa-1165">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1165">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="865fa-1166">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1166">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="865fa-1167">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1167">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="865fa-1168">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1168">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="865fa-1169">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1169">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="865fa-1170">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1170">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="865fa-1171">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1171">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="865fa-1172">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1172">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="865fa-1173">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1173">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="865fa-1174">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1174">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="865fa-1175">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1175">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="865fa-1176">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1176">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="865fa-1177">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1177">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="865fa-1178">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1178">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="865fa-1179">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="865fa-1179">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="865fa-1180">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1180">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="865fa-1181">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="865fa-1181">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="865fa-1182">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1182">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="865fa-1183">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1183">Overall improved help files</span></span>
* <span data-ttu-id="865fa-1184">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1184">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1185">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1185">Az.Network</span></span>
* <span data-ttu-id="865fa-1186">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1186">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="865fa-1187">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1187">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="865fa-1188">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1188">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="865fa-1189">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1189">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="865fa-1190">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1190">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="865fa-1191">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1191">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="865fa-1192">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1192">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="865fa-1193">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1193">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="865fa-1194">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1194">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="865fa-1195">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1195">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="865fa-1196">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1196">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="865fa-1197">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1197">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="865fa-1198">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-1198">New cmdlets</span></span>
        - <span data-ttu-id="865fa-1199">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="865fa-1199">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="865fa-1200">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-1200">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="865fa-1201">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="865fa-1201">Updated cmdlet:</span></span>
        - <span data-ttu-id="865fa-1202">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="865fa-1202">New-VpnSite</span></span>
        - <span data-ttu-id="865fa-1203">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="865fa-1203">Update-VpnSite</span></span>
        - <span data-ttu-id="865fa-1204">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-1204">New-VpnConnection</span></span>
        - <span data-ttu-id="865fa-1205">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-1205">Update-VpnConnection</span></span>
* <span data-ttu-id="865fa-1206">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1206">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-1207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1207">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-1208">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1208">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="865fa-1209">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1209">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-1210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-1210">Az.Resources</span></span>
* <span data-ttu-id="865fa-1211">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1211">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="865fa-1212">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-1212">Az.ServiceFabric</span></span>
* <span data-ttu-id="865fa-1213">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1213">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="865fa-1214">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1214">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="865fa-1215">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="865fa-1215">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="865fa-1216">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="865fa-1216">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="865fa-1217">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="865fa-1217">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="865fa-1218">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="865fa-1218">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="865fa-1219">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="865fa-1219">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="865fa-1220">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="865fa-1220">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="865fa-1221">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="865fa-1221">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="865fa-1222">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="865fa-1222">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="865fa-1223">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="865fa-1223">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="865fa-1224">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="865fa-1224">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="865fa-1225">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="865fa-1225">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="865fa-1226">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="865fa-1226">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="865fa-1227">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="865fa-1227">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="865fa-1228">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1228">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="865fa-1229">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="865fa-1229">Az.SignalR</span></span>
* <span data-ttu-id="865fa-1230">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1230">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1231">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1231">Az.Sql</span></span>
* <span data-ttu-id="865fa-1232">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1232">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="865fa-1233">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="865fa-1233">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="865fa-1234">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1234">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="865fa-1235">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1235">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="865fa-1236">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="865fa-1236">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-1237">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-1237">Az.Storage</span></span>
* <span data-ttu-id="865fa-1238">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1238">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="865fa-1239">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1239">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="865fa-1240">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="865fa-1240">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="865fa-1241">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="865fa-1241">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="865fa-1242">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1242">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="865fa-1243">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="865fa-1243">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="865fa-1244">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1244">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="865fa-1245">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="865fa-1245">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="865fa-1246">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="865fa-1246">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="865fa-1247">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="865fa-1247">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="865fa-1248">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="865fa-1248">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-1249">Az.Websites</span></span>
* <span data-ttu-id="865fa-1250">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1250">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="865fa-1251">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1251">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="865fa-1252">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1252">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="865fa-1253">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="865fa-1253">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="865fa-1254">일반</span><span class="sxs-lookup"><span data-stu-id="865fa-1254">General</span></span>
* <span data-ttu-id="865fa-1255">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1255">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="865fa-1256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-1256">Az.Accounts</span></span>
* <span data-ttu-id="865fa-1257">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="865fa-1257">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="865fa-1258">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="865fa-1258">Az.Aks</span></span>
* <span data-ttu-id="865fa-1259">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1259">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="865fa-1260">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1260">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="865fa-1261">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-1261">Az.ApiManagement</span></span>
* <span data-ttu-id="865fa-1262">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1262">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="865fa-1263">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1263">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="865fa-1264">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1264">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="865fa-1265">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1265">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="865fa-1266">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1266">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="865fa-1267">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="865fa-1267">Az.Batch</span></span>
* <span data-ttu-id="865fa-1268">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1268">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="865fa-1269">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="865fa-1269">Az.Cdn</span></span>
* <span data-ttu-id="865fa-1270">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1270">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1271">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1271">Az.Compute</span></span>
* <span data-ttu-id="865fa-1272">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1272">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="865fa-1273">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1273">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="865fa-1274">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1274">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="865fa-1275">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1275">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="865fa-1276">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="865fa-1276">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="865fa-1277">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1277">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="865fa-1278">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1278">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="865fa-1279">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1279">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-1280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-1280">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-1281">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1281">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="865fa-1282">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1282">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="865fa-1283">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1283">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="865fa-1284">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1284">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-1285">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-1285">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-1286">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1286">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="865fa-1287">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="865fa-1287">Az.EventHub</span></span>
* <span data-ttu-id="865fa-1288">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="865fa-1288">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="865fa-1289">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1289">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="865fa-1290">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1290">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="865fa-1291">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="865fa-1291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="865fa-1292">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="865fa-1292">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="865fa-1293">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1293">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-1294">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-1294">Az.Monitor</span></span>
* <span data-ttu-id="865fa-1295">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1295">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1296">Az.Network</span></span>
* <span data-ttu-id="865fa-1297">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1297">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="865fa-1298">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="865fa-1298">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="865fa-1299">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1299">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="865fa-1300">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1300">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="865fa-1301">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1301">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="865fa-1302">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1302">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="865fa-1303">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1303">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="865fa-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="865fa-1305">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1305">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="865fa-1306">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1306">Added example</span></span>
    - <span data-ttu-id="865fa-1307">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1307">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="865fa-1308">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1308">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="865fa-1309">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1309">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-1310">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1310">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-1311">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1311">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-1312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-1312">Az.Resources</span></span>
* <span data-ttu-id="865fa-1313">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1313">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="865fa-1314">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1314">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="865fa-1315">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1315">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="865fa-1316">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1316">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="865fa-1317">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="865fa-1317">Az.ServiceBus</span></span>
* <span data-ttu-id="865fa-1318">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="865fa-1318">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="865fa-1319">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="865fa-1319">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="865fa-1320">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1320">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="865fa-1321">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-1321">Az.ServiceFabric</span></span>
* <span data-ttu-id="865fa-1322">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="865fa-1322">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="865fa-1323">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="865fa-1323">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="865fa-1324">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="865fa-1324">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="865fa-1325">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1325">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="865fa-1326">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="865fa-1326">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="865fa-1327">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="865fa-1327">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1328">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1328">Az.Sql</span></span>
* <span data-ttu-id="865fa-1329">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1329">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-1330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-1330">Az.Storage</span></span>
* <span data-ttu-id="865fa-1331">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1331">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="865fa-1332">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1332">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="865fa-1333">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="865fa-1333">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="865fa-1334">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="865fa-1334">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="865fa-1335">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1335">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="865fa-1336">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="865fa-1336">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-1337">Az.Websites</span></span>
* <span data-ttu-id="865fa-1338">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1338">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="865fa-1339">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="865fa-1339">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-1340">Az.Accounts</span></span>
* <span data-ttu-id="865fa-1341">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1341">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="865fa-1342">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-1342">Az.ApplicationInsights</span></span>
* <span data-ttu-id="865fa-1343">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1343">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-1344">Az.Automation</span></span>
* <span data-ttu-id="865fa-1345">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1345">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="865fa-1346">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1346">Az.CognitiveServices</span></span>
* <span data-ttu-id="865fa-1347">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1347">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1348">Az.Compute</span></span>
* <span data-ttu-id="865fa-1349">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1349">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="865fa-1350">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="865fa-1350">Az.ContainerRegistry</span></span>
* <span data-ttu-id="865fa-1351">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1351">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="865fa-1352">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1352">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-1353">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-1354">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1354">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="865fa-1355">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1355">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="865fa-1356">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="865fa-1356">Az.EventHub</span></span>
* <span data-ttu-id="865fa-1357">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="865fa-1357">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="865fa-1358">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1358">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-1359">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-1359">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-1360">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1360">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="865fa-1361">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="865fa-1361">Az.LogicApp</span></span>
* <span data-ttu-id="865fa-1362">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1362">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="865fa-1363">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1363">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="865fa-1364">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1364">Az.ManagedServices</span></span>
* <span data-ttu-id="865fa-1365">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1365">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1366">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1366">Az.Network</span></span>
* <span data-ttu-id="865fa-1367">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1367">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="865fa-1368">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-1368">New cmdlets</span></span>
        - <span data-ttu-id="865fa-1369">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="865fa-1369">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="865fa-1370">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="865fa-1370">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="865fa-1371">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-1371">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="865fa-1372">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-1372">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="865fa-1373">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-1373">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="865fa-1374">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-1374">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="865fa-1375">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="865fa-1375">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="865fa-1376">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="865fa-1376">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="865fa-1377">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="865fa-1377">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="865fa-1378">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1378">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="865fa-1379">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1379">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="865fa-1380">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1380">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="865fa-1381">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1381">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="865fa-1382">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="865fa-1382">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="865fa-1383">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1383">Updated cmdlets</span></span>
        - <span data-ttu-id="865fa-1384">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1384">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="865fa-1385">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1385">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="865fa-1386">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1386">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="865fa-1387">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1387">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="865fa-1388">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1388">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="865fa-1389">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="865fa-1389">Updated cmdlet:</span></span>
        - <span data-ttu-id="865fa-1390">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1390">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="865fa-1391">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1391">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="865fa-1392">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1392">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="865fa-1393">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1393">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="865fa-1394">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1394">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="865fa-1395">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1395">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="865fa-1396">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-1396">Az.OperationalInsights</span></span>
* <span data-ttu-id="865fa-1397">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1397">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="865fa-1398">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1398">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-1399">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1399">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-1400">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1400">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="865fa-1401">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1401">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="865fa-1402">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1402">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="865fa-1403">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1403">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="865fa-1404">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1404">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="865fa-1405">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1405">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="865fa-1406">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1406">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="865fa-1407">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1407">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="865fa-1408">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1408">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="865fa-1409">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1409">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-1410">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-1410">Az.Resources</span></span>
- <span data-ttu-id="865fa-1411">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-1411">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="865fa-1412">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1412">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="865fa-1413">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="865fa-1413">Az.ServiceBus</span></span>
* <span data-ttu-id="865fa-1414">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="865fa-1414">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="865fa-1415">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1415">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1416">Az.Sql</span></span>
* <span data-ttu-id="865fa-1417">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1417">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="865fa-1418">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1418">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="865fa-1419">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1419">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-1420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-1420">Az.Storage</span></span>
* <span data-ttu-id="865fa-1421">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="865fa-1421">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="865fa-1422">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="865fa-1422">Az.StorageSync</span></span>
* <span data-ttu-id="865fa-1423">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1423">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="865fa-1424">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1424">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-1425">Az.Websites</span></span>
* <span data-ttu-id="865fa-1426">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1426">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="865fa-1427">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1427">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="865fa-1428">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1428">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="865fa-1429">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="865fa-1429">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-1430">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-1430">Az.Accounts</span></span>
* <span data-ttu-id="865fa-1431">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1431">Add support for profile cmdlets</span></span>
* <span data-ttu-id="865fa-1432">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1432">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="865fa-1433">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1433">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="865fa-1434">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="865fa-1434">Az.Advisor</span></span>
* <span data-ttu-id="865fa-1435">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="865fa-1435">GA release of Az.Advisor</span></span>
* <span data-ttu-id="865fa-1436">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1436">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="865fa-1437">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-1437">Az.ApiManagement</span></span>
* <span data-ttu-id="865fa-1438">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1438">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="865fa-1439">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="865fa-1439">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="865fa-1440">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1440">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="865fa-1441">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1441">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="865fa-1442">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="865fa-1443">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="865fa-1443">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="865fa-1444">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1444">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-1445">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-1445">Az.Automation</span></span>
* <span data-ttu-id="865fa-1446">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1446">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1447">Az.Compute</span></span>
* <span data-ttu-id="865fa-1448">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1448">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-1449">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-1449">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-1450">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1450">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="865fa-1451">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="865fa-1451">Az.EventGrid</span></span>
* <span data-ttu-id="865fa-1452">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1452">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-1453">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-1453">Az.IotHub</span></span>
* <span data-ttu-id="865fa-1454">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1454">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1455">Az.Network</span></span>
* <span data-ttu-id="865fa-1456">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="865fa-1456">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="865fa-1457">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="865fa-1457">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="865fa-1458">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-1458">Az.PolicyInsights</span></span>
* <span data-ttu-id="865fa-1459">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="865fa-1459">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="865fa-1460">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1460">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="865fa-1461">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-1461">Az.OperationalInsights</span></span>
* <span data-ttu-id="865fa-1462">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1462">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-1464">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1464">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-1465">Az.Resources</span></span>
    - <span data-ttu-id="865fa-1466">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1466">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="865fa-1467">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1467">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="865fa-1468">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1468">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="865fa-1469">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1469">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="865fa-1470">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="865fa-1470">Az.ServiceBus</span></span>
* <span data-ttu-id="865fa-1471">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="865fa-1471">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1472">Az.Sql</span></span>
* <span data-ttu-id="865fa-1473">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1473">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="865fa-1474">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1474">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="865fa-1475">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="865fa-1475">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="865fa-1476">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="865fa-1476">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="865fa-1477">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="865fa-1477">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="865fa-1478">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="865fa-1478">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="865fa-1479">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="865fa-1479">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="865fa-1480">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="865fa-1480">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="865fa-1481">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-1481">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-1482">Az.Storage</span></span>
* <span data-ttu-id="865fa-1483">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1483">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="865fa-1484">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="865fa-1484">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="865fa-1485">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1485">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="865fa-1486">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="865fa-1486">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="865fa-1487">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1487">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="865fa-1488">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-1488">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="865fa-1489">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-1489">Set-AzStorageAccount</span></span>
* <span data-ttu-id="865fa-1490">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="865fa-1490">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="865fa-1491">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="865fa-1491">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="865fa-1492">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="865fa-1492">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="865fa-1493">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="865fa-1493">Az.StorageSync</span></span>
* <span data-ttu-id="865fa-1494">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1494">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="865fa-1495">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="865fa-1495">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-1496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-1496">Az.Accounts</span></span>
* <span data-ttu-id="865fa-1497">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1497">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="865fa-1498">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1498">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="865fa-1499">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="865fa-1499">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="865fa-1500">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="865fa-1500">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="865fa-1501">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="865fa-1501">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1502">Az.Compute</span></span>
* <span data-ttu-id="865fa-1503">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1503">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="865fa-1504">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1504">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="865fa-1505">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="865fa-1505">Az.Dns</span></span>
* <span data-ttu-id="865fa-1506">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1506">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="865fa-1507">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="865fa-1507">Az.EventGrid</span></span>
* <span data-ttu-id="865fa-1508">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1508">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="865fa-1509">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="865fa-1509">New cmdlets:</span></span>
    - <span data-ttu-id="865fa-1510">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="865fa-1510">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="865fa-1511">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1511">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="865fa-1512">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="865fa-1512">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="865fa-1513">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1513">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="865fa-1514">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="865fa-1514">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="865fa-1515">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1515">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="865fa-1516">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="865fa-1516">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="865fa-1517">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1517">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="865fa-1518">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="865fa-1518">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="865fa-1519">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1519">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="865fa-1520">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="865fa-1520">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="865fa-1521">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1521">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="865fa-1522">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="865fa-1522">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="865fa-1523">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1523">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="865fa-1524">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="865fa-1524">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="865fa-1525">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1525">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="865fa-1526">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1526">Updated cmdlets:</span></span>
    - <span data-ttu-id="865fa-1527">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="865fa-1527">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="865fa-1528">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1528">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="865fa-1529">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1529">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="865fa-1530">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1530">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="865fa-1531">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1531">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="865fa-1532">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="865fa-1532">Event subscription expiration date,</span></span>
            - <span data-ttu-id="865fa-1533">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="865fa-1533">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="865fa-1534">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1534">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="865fa-1535">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="865fa-1535">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="865fa-1536">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="865fa-1536">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="865fa-1537">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1537">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="865fa-1538">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="865fa-1538">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="865fa-1539">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1539">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="865fa-1540">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1540">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="865fa-1541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="865fa-1541">Az.FrontDoor</span></span>
* <span data-ttu-id="865fa-1542">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="865fa-1542">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="865fa-1543">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1543">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="865fa-1544">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="865fa-1544">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="865fa-1545">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1545">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1546">Az.Network</span></span>
* <span data-ttu-id="865fa-1547">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1547">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="865fa-1548">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-1548">New cmdlets</span></span>
        - <span data-ttu-id="865fa-1549">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="865fa-1549">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="865fa-1550">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1550">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="865fa-1551">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-1551">New cmdlets</span></span>
        - <span data-ttu-id="865fa-1552">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="865fa-1552">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="865fa-1553">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1553">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="865fa-1554">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-1554">New cmdlets</span></span>
        - <span data-ttu-id="865fa-1555">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="865fa-1555">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="865fa-1556">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="865fa-1556">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="865fa-1557">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="865fa-1557">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="865fa-1558">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1558">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="865fa-1559">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-1559">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="865fa-1560">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1560">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="865fa-1561">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-1561">New cmdlets</span></span>
        - <span data-ttu-id="865fa-1562">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="865fa-1562">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="865fa-1563">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="865fa-1563">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="865fa-1564">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="865fa-1564">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="865fa-1565">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="865fa-1565">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="865fa-1566">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="865fa-1566">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="865fa-1567">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1567">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="865fa-1568">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1568">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="865fa-1569">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1569">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="865fa-1570">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1570">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="865fa-1571">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1571">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="865fa-1572">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1572">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="865fa-1573">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1573">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="865fa-1574">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1574">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="865fa-1575">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1575">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="865fa-1576">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1576">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="865fa-1577">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1577">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="865fa-1578">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1578">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="865fa-1579">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1579">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="865fa-1580">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="865fa-1580">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="865fa-1581">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1581">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="865fa-1582">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1582">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="865fa-1583">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="865fa-1583">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="865fa-1584">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="865fa-1584">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="865fa-1585">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1585">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="865fa-1586">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1586">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="865fa-1587">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1587">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="865fa-1588">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1588">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="865fa-1589">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-1589">Az.OperationalInsights</span></span>
* <span data-ttu-id="865fa-1590">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="865fa-1590">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-1591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-1591">Az.Resources</span></span>
* <span data-ttu-id="865fa-1592">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1592">Support for additional Template Export options</span></span>
    - <span data-ttu-id="865fa-1593">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1593">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="865fa-1594">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1594">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="865fa-1595">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1595">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="865fa-1596">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-1596">Az.ServiceFabric</span></span>
* <span data-ttu-id="865fa-1597">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1597">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1598">Az.Sql</span></span>
* <span data-ttu-id="865fa-1599">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1599">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="865fa-1600">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1600">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="865fa-1601">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1601">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="865fa-1602">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="865fa-1602">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="865fa-1603">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="865fa-1603">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="865fa-1604">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="865fa-1604">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="865fa-1605">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="865fa-1605">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="865fa-1606">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="865fa-1606">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-1607">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-1607">Az.Storage</span></span>
* <span data-ttu-id="865fa-1608">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1608">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="865fa-1609">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-1609">New-AzStorageAccount</span></span>
* <span data-ttu-id="865fa-1610">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="865fa-1610">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="865fa-1611">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="865fa-1611">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-1612">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-1612">Az.Websites</span></span>
* <span data-ttu-id="865fa-1613">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="865fa-1613">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="865fa-1614">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1614">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="865fa-1615">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="865fa-1615">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="865fa-1616">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="865fa-1616">Az.Cdn</span></span>
* <span data-ttu-id="865fa-1617">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1617">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1618">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1618">Az.Compute</span></span>
* <span data-ttu-id="865fa-1619">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1619">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="865fa-1620">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="865fa-1620">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="865fa-1621">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="865fa-1621">Az.EventHub</span></span>
* <span data-ttu-id="865fa-1622">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="865fa-1622">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="865fa-1623">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="865fa-1623">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1624">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1624">Az.Network</span></span>
* <span data-ttu-id="865fa-1625">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1625">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="865fa-1626">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1626">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="865fa-1627">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-1627">Az.PolicyInsights</span></span>
* <span data-ttu-id="865fa-1628">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="865fa-1628">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-1630">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1630">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="865fa-1631">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="865fa-1631">Az.ServiceBus</span></span>
* <span data-ttu-id="865fa-1632">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="865fa-1632">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="865fa-1633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-1633">Az.ServiceFabric</span></span>
* <span data-ttu-id="865fa-1634">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1634">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="865fa-1635">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1635">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1636">Az.Sql</span></span>
* <span data-ttu-id="865fa-1637">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1637">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="865fa-1638">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="865fa-1638">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="865fa-1639">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="865fa-1639">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="865fa-1640">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1640">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-1641">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-1641">Az.Websites</span></span>
* <span data-ttu-id="865fa-1642">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="865fa-1642">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="865fa-1643">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="865fa-1643">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="865fa-1644">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-1644">Az.ApiManagement</span></span>
* <span data-ttu-id="865fa-1645">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1645">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="865fa-1646">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="865fa-1646">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="865fa-1647">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-1647">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="865fa-1648">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-1648">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="865fa-1649">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-1649">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="865fa-1650">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-1650">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="865fa-1651">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-1651">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="865fa-1652">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1652">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="865fa-1653">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1653">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="865fa-1654">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="865fa-1654">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="865fa-1655">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-1655">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="865fa-1656">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-1656">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="865fa-1657">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1657">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="865fa-1658">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1658">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="865fa-1659">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-1659">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="865fa-1660">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="865fa-1660">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="865fa-1661">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-1661">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="865fa-1662">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1662">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="865fa-1663">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1663">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="865fa-1664">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1664">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="865fa-1665">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1665">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="865fa-1666">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1666">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="865fa-1667">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1667">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="865fa-1668">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1668">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="865fa-1669">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1669">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="865fa-1670">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1670">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="865fa-1671">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1671">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="865fa-1672">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1672">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="865fa-1673">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1673">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="865fa-1674">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1674">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="865fa-1675">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1675">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="865fa-1676">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="865fa-1676">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="865fa-1677">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1677">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="865fa-1678">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1678">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="865fa-1679">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="865fa-1679">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="865fa-1680">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="865fa-1680">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="865fa-1681">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="865fa-1681">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="865fa-1682">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1682">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="865fa-1683">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1683">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="865fa-1684">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1684">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="865fa-1685">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="865fa-1685">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="865fa-1686">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="865fa-1686">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="865fa-1687">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="865fa-1687">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="865fa-1688">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="865fa-1688">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="865fa-1689">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1689">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="865fa-1690">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="865fa-1690">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="865fa-1691">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1691">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="865fa-1692">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="865fa-1692">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="865fa-1693">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1693">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="865fa-1694">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="865fa-1694">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="865fa-1695">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1695">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="865fa-1696">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="865fa-1696">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="865fa-1697">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="865fa-1697">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="865fa-1698">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1698">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="865fa-1699">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="865fa-1699">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="865fa-1700">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="865fa-1700">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="865fa-1701">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1701">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="865fa-1702">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="865fa-1702">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="865fa-1703">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="865fa-1703">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="865fa-1704">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1704">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="865fa-1705">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1705">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="865fa-1706">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="865fa-1706">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="865fa-1707">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="865fa-1707">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="865fa-1708">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1708">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="865fa-1709">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="865fa-1709">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="865fa-1710">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="865fa-1710">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="865fa-1711">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="865fa-1711">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="865fa-1712">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="865fa-1712">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="865fa-1713">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="865fa-1713">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="865fa-1714">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="865fa-1714">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="865fa-1715">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="865fa-1715">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="865fa-1716">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="865fa-1716">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="865fa-1717">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="865fa-1717">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="865fa-1718">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="865fa-1718">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="865fa-1719">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="865fa-1719">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="865fa-1720">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="865fa-1720">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="865fa-1721">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="865fa-1721">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-1722">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-1722">Az.Automation</span></span>
* <span data-ttu-id="865fa-1723">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1723">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="865fa-1724">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1724">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="865fa-1725">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1725">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="865fa-1726">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1726">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="865fa-1727">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1727">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="865fa-1728">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="865fa-1728">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="865fa-1729">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1729">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1730">Az.Compute</span></span>
* <span data-ttu-id="865fa-1731">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1731">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="865fa-1732">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1732">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-1733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-1733">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-1734">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1734">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-1735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-1735">Az.Monitor</span></span>
* <span data-ttu-id="865fa-1736">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1736">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1737">Az.Network</span></span>
* <span data-ttu-id="865fa-1738">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1738">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="865fa-1739">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="865fa-1739">Updated cmdlet:</span></span>
        - <span data-ttu-id="865fa-1740">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="865fa-1740">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="865fa-1741">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1741">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-1742">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-1742">Az.Resources</span></span>
* <span data-ttu-id="865fa-1743">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1743">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1744">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1744">Az.Sql</span></span>
* <span data-ttu-id="865fa-1745">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1745">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="865fa-1746">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="865fa-1746">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-1747">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-1747">Az.Accounts</span></span>
* <span data-ttu-id="865fa-1748">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1748">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="865fa-1749">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1749">Az.CognitiveServices</span></span>
* <span data-ttu-id="865fa-1750">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1750">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="865fa-1751">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="865fa-1751">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1752">Az.Compute</span></span>
* <span data-ttu-id="865fa-1753">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="865fa-1753">Proximity placement group feature.</span></span>
    - <span data-ttu-id="865fa-1754">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="865fa-1754">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="865fa-1755">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-1755">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="865fa-1756">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1756">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="865fa-1757">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1757">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="865fa-1758">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1758">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="865fa-1759">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="865fa-1759">Breaking changes</span></span>
    - <span data-ttu-id="865fa-1760">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1760">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="865fa-1761">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1761">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="865fa-1762">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="865fa-1762">Az.DeploymentManager</span></span>
* <span data-ttu-id="865fa-1763">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="865fa-1763">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="865fa-1764">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="865fa-1764">Az.Dns</span></span>
* <span data-ttu-id="865fa-1765">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="865fa-1765">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="865fa-1766">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1766">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="865fa-1767">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1767">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="865fa-1768">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="865fa-1768">Az.FrontDoor</span></span>
* <span data-ttu-id="865fa-1769">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="865fa-1769">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="865fa-1770">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="865fa-1770">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="865fa-1771">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="865fa-1771">Az.HDInsight</span></span>
* <span data-ttu-id="865fa-1772">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1772">Removed two cmdlets:</span></span>
    - <span data-ttu-id="865fa-1773">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="865fa-1773">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="865fa-1774">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="865fa-1774">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="865fa-1775">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1775">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="865fa-1776">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="865fa-1776">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="865fa-1777">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1777">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="865fa-1778">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1778">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-1779">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-1779">Az.Monitor</span></span>
* <span data-ttu-id="865fa-1780">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-1780">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="865fa-1781">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="865fa-1781">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="865fa-1782">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="865fa-1782">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="865fa-1783">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="865fa-1783">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="865fa-1784">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="865fa-1784">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="865fa-1785">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="865fa-1785">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="865fa-1786">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="865fa-1786">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="865fa-1787">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="865fa-1787">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="865fa-1788">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="865fa-1788">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="865fa-1789">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="865fa-1789">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="865fa-1790">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="865fa-1790">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="865fa-1791">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="865fa-1791">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="865fa-1792">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="865fa-1792">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="865fa-1793">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-1793">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1794">Az.Network</span></span>
* <span data-ttu-id="865fa-1795">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1795">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="865fa-1796">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-1796">New cmdlets</span></span>
        - <span data-ttu-id="865fa-1797">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="865fa-1797">New-AzNatGateway</span></span>
        - <span data-ttu-id="865fa-1798">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="865fa-1798">Get-AzNatGateway</span></span>
        - <span data-ttu-id="865fa-1799">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="865fa-1799">Set-AzNatGateway</span></span>
        - <span data-ttu-id="865fa-1800">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="865fa-1800">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="865fa-1801">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1801">Updated cmdlets</span></span>
        - <span data-ttu-id="865fa-1802">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="865fa-1802">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="865fa-1803">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="865fa-1803">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="865fa-1804">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="865fa-1804">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="865fa-1805">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1805">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="865fa-1806">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1806">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="865fa-1807">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-1807">Az.PolicyInsights</span></span>
* <span data-ttu-id="865fa-1808">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1808">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="865fa-1809">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1809">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="865fa-1810">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1810">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-1811">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1811">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-1812">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1812">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="865fa-1813">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="865fa-1813">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="865fa-1814">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1814">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="865fa-1815">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1815">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="865fa-1816">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1816">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="865fa-1817">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="865fa-1817">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="865fa-1818">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="865fa-1818">Az.Relay</span></span>
* <span data-ttu-id="865fa-1819">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1819">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="865fa-1820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="865fa-1820">Az.ServiceBus</span></span>
* <span data-ttu-id="865fa-1821">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="865fa-1821">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-1822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-1822">Az.Storage</span></span>
* <span data-ttu-id="865fa-1823">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="865fa-1823">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="865fa-1824">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1824">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="865fa-1825">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1825">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="865fa-1826">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-1826">New-AzStorageAccount</span></span>
* <span data-ttu-id="865fa-1827">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1827">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="865fa-1828">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-1828">New-AzStorageAccount</span></span>
    - <span data-ttu-id="865fa-1829">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-1829">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="865fa-1830">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="865fa-1830">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-1831">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-1831">Az.Websites</span></span>
* <span data-ttu-id="865fa-1832">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1832">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="865fa-1833">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1833">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="865fa-1834">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="865fa-1834">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="865fa-1835">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="865fa-1835">Highlights since the last major release</span></span>
* <span data-ttu-id="865fa-1836">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="865fa-1836">General availability of `Az` module</span></span>
* <span data-ttu-id="865fa-1837">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1837">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="865fa-1838">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="865fa-1838">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="865fa-1839">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1839">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="865fa-1840">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1840">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="865fa-1841">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1841">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="865fa-1842">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1842">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="865fa-1843">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-1843">Az.Accounts</span></span>
* <span data-ttu-id="865fa-1844">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1844">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="865fa-1845">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="865fa-1845">Az.Batch</span></span>
* <span data-ttu-id="865fa-1846">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1846">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="865fa-1847">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="865fa-1847">Az.Cdn</span></span>
* <span data-ttu-id="865fa-1848">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1848">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="865fa-1849">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1849">Az.CognitiveServices</span></span>
* <span data-ttu-id="865fa-1850">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1850">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1851">Az.Compute</span></span>
* <span data-ttu-id="865fa-1852">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1852">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="865fa-1853">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="865fa-1854">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1854">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-1855">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-1855">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-1856">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1856">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-1858">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="865fa-1859">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="865fa-1859">Az.EventGrid</span></span>
* <span data-ttu-id="865fa-1860">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1860">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="865fa-1861">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="865fa-1861">Az.EventHub</span></span>
* <span data-ttu-id="865fa-1862">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="865fa-1862">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="865fa-1863">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="865fa-1863">Az.HDInsight</span></span>
* <span data-ttu-id="865fa-1864">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-1865">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-1865">Az.IotHub</span></span>
* <span data-ttu-id="865fa-1866">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1866">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-1867">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-1867">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-1868">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1868">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="865fa-1869">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1869">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="865fa-1870">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="865fa-1870">Az.MachineLearning</span></span>
* <span data-ttu-id="865fa-1871">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1871">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="865fa-1872">Az.Media</span><span class="sxs-lookup"><span data-stu-id="865fa-1872">Az.Media</span></span>
* <span data-ttu-id="865fa-1873">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1873">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-1874">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-1874">Az.Monitor</span></span>
  * <span data-ttu-id="865fa-1875">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-1875">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="865fa-1876">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="865fa-1876">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="865fa-1877">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="865fa-1877">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="865fa-1878">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="865fa-1878">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="865fa-1879">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="865fa-1879">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="865fa-1880">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="865fa-1880">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="865fa-1881">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1881">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1882">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1882">Az.Network</span></span>
* <span data-ttu-id="865fa-1883">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="865fa-1884">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1884">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="865fa-1885">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="865fa-1885">Az.NotificationHubs</span></span>
* <span data-ttu-id="865fa-1886">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="865fa-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="865fa-1888">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="865fa-1889">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="865fa-1889">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="865fa-1890">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-1891">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1891">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-1892">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="865fa-1893">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1893">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="865fa-1894">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1894">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="865fa-1895">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1895">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="865fa-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="865fa-1896">Az.RedisCache</span></span>
* <span data-ttu-id="865fa-1897">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-1898">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-1898">Az.Resources</span></span>
* <span data-ttu-id="865fa-1899">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1899">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1900">Az.Sql</span></span>
* <span data-ttu-id="865fa-1901">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1901">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="865fa-1902">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1902">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="865fa-1903">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1903">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="865fa-1904">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1904">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="865fa-1905">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1905">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="865fa-1906">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1906">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="865fa-1907">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1907">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-1908">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-1908">Az.Websites</span></span>
* <span data-ttu-id="865fa-1909">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1909">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="865fa-1910">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="865fa-1911">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1911">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="865fa-1912">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1912">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="865fa-1913">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="865fa-1913">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="865fa-1914">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="865fa-1914">Highlights since the last major release</span></span>
* <span data-ttu-id="865fa-1915">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="865fa-1915">General availability of `Az` module</span></span>
* <span data-ttu-id="865fa-1916">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1916">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="865fa-1917">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="865fa-1917">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="865fa-1918">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1918">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="865fa-1919">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1919">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="865fa-1920">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1920">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="865fa-1921">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1921">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="865fa-1922">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-1922">Az.Accounts</span></span>
* <span data-ttu-id="865fa-1923">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1923">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="865fa-1924">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1924">Az.AnalysisServices</span></span>
* <span data-ttu-id="865fa-1925">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-1925">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="865fa-1926">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="865fa-1926">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-1927">Az.Automation</span></span>
* <span data-ttu-id="865fa-1928">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1928">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="865fa-1929">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="865fa-1929">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="865fa-1930">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1930">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1931">Az.Compute</span></span>
* <span data-ttu-id="865fa-1932">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1932">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="865fa-1933">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="865fa-1933">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="865fa-1934">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="865fa-1934">Az.ContainerInstance</span></span>
* <span data-ttu-id="865fa-1935">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-1935">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-1936">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-1937">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1937">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="865fa-1938">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-1938">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-1939">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-1939">Az.Resources</span></span>
* <span data-ttu-id="865fa-1940">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="865fa-1940">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="865fa-1941">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="865fa-1941">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="865fa-1942">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="865fa-1942">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="865fa-1943">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1943">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="865fa-1944">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-1944">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="865fa-1945">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1945">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1946">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1946">Az.Sql</span></span>
* <span data-ttu-id="865fa-1947">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1947">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-1948">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-1948">Az.Storage</span></span>
* <span data-ttu-id="865fa-1949">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="865fa-1949">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="865fa-1950">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="865fa-1950">New-AzStorageContext</span></span>
* <span data-ttu-id="865fa-1951">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1951">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="865fa-1952">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="865fa-1952">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="865fa-1953">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="865fa-1953">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="865fa-1954">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="865fa-1954">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="865fa-1955">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="865fa-1955">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="865fa-1956">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-1956">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="865fa-1957">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="865fa-1957">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="865fa-1958">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="865fa-1958">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="865fa-1959">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="865fa-1959">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="865fa-1960">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="865fa-1960">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="865fa-1961">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="865fa-1961">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="865fa-1962">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="865fa-1962">Highlights since the last major release</span></span>
* <span data-ttu-id="865fa-1963">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="865fa-1963">General availability of `Az` module</span></span>
* <span data-ttu-id="865fa-1964">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-1964">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="865fa-1965">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="865fa-1965">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="865fa-1966">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1966">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="865fa-1967">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1967">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="865fa-1968">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1968">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="865fa-1969">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1969">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-1970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-1970">Az.Automation</span></span>
* <span data-ttu-id="865fa-1971">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1971">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="865fa-1972">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="865fa-1972">Dynamic grouping</span></span>
    * <span data-ttu-id="865fa-1973">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="865fa-1973">Pre-Post script</span></span>
    * <span data-ttu-id="865fa-1974">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="865fa-1974">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-1975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-1975">Az.Compute</span></span>
* <span data-ttu-id="865fa-1976">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1976">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="865fa-1977">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1977">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-1978">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-1978">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-1979">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1979">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-1980">Az.Network</span></span>
* <span data-ttu-id="865fa-1981">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1981">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="865fa-1982">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1982">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-1983">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-1983">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-1984">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1984">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="865fa-1985">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1985">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-1986">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-1986">Az.Resources</span></span>
* <span data-ttu-id="865fa-1987">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1987">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="865fa-1988">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1988">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-1989">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-1989">Az.Sql</span></span>
* <span data-ttu-id="865fa-1990">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1990">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-1991">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-1991">Az.Storage</span></span>
* <span data-ttu-id="865fa-1992">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-1992">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="865fa-1993">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="865fa-1993">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="865fa-1994">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="865fa-1994">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="865fa-1995">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="865fa-1995">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="865fa-1996">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="865fa-1996">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="865fa-1997">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="865fa-1997">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="865fa-1998">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="865fa-1998">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-1999">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-1999">Az.Websites</span></span>
* <span data-ttu-id="865fa-2000">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2000">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="865fa-2001">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="865fa-2001">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-2002">Az.Accounts</span></span>
* <span data-ttu-id="865fa-2003">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-2003">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="865fa-2004">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2004">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-2005">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-2005">Az.Automation</span></span>
* <span data-ttu-id="865fa-2006">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2006">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="865fa-2007">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2007">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="865fa-2008">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="865fa-2008">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="865fa-2009">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="865fa-2009">Az.Cdn</span></span>
* <span data-ttu-id="865fa-2010">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2010">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-2011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-2011">Az.Compute</span></span>
* <span data-ttu-id="865fa-2012">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2012">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-2013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-2013">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-2014">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2014">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="865fa-2015">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="865fa-2015">Az.LogicApp</span></span>
* <span data-ttu-id="865fa-2016">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2016">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-2017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-2017">Az.Network</span></span>
* <span data-ttu-id="865fa-2018">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2018">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-2019">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2019">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-2020">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2020">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="865fa-2021">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2021">SDK Update</span></span>
* <span data-ttu-id="865fa-2022">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-2022">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="865fa-2023">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2023">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-2024">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2024">Az.Resources</span></span>
* <span data-ttu-id="865fa-2025">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="865fa-2025">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="865fa-2026">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2026">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="865fa-2027">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2027">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="865fa-2028">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2028">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="865fa-2029">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="865fa-2029">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="865fa-2030">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2030">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-2031">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-2031">Az.Sql</span></span>
* <span data-ttu-id="865fa-2032">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2032">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="865fa-2033">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2033">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-2034">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-2034">Az.Storage</span></span>
* <span data-ttu-id="865fa-2035">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-2035">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="865fa-2036">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="865fa-2036">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="865fa-2037">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2037">Az.AnalysisServices</span></span>
* <span data-ttu-id="865fa-2038">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-2038">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-2039">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-2039">Az.Automation</span></span>
* <span data-ttu-id="865fa-2040">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2040">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="865fa-2041">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2041">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="865fa-2042">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="865fa-2042">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="865fa-2043">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2043">Az.CognitiveServices</span></span>
* <span data-ttu-id="865fa-2044">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2044">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-2045">Az.Compute</span></span>
* <span data-ttu-id="865fa-2046">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="865fa-2046">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="865fa-2047">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2047">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="865fa-2048">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2048">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="865fa-2049">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2049">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-2051">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2051">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="865fa-2052">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="865fa-2052">Az.EventHub</span></span>
* <span data-ttu-id="865fa-2053">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2053">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-2054">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-2054">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-2055">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2055">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="865fa-2056">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="865fa-2056">Az.LogicApp</span></span>
* <span data-ttu-id="865fa-2057">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2057">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="865fa-2058">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2058">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="865fa-2059">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-2059">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="865fa-2060">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="865fa-2060">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="865fa-2061">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="865fa-2061">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="865fa-2062">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="865fa-2062">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="865fa-2063">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="865fa-2063">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="865fa-2064">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-2064">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="865fa-2065">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="865fa-2065">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="865fa-2066">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="865fa-2066">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="865fa-2067">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="865fa-2067">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="865fa-2068">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="865fa-2068">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="865fa-2069">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2069">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="865fa-2070">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-2070">Az.Monitor</span></span>
* <span data-ttu-id="865fa-2071">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2071">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-2072">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-2072">Az.Network</span></span>
* <span data-ttu-id="865fa-2073">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2073">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="865fa-2074">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-2074">Az.OperationalInsights</span></span>
* <span data-ttu-id="865fa-2075">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2075">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="865fa-2076">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2076">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="865fa-2077">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2077">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2078">Az.Resources</span></span>
* <span data-ttu-id="865fa-2079">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2079">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="865fa-2080">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2080">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="865fa-2081">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2081">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="865fa-2082">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2082">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-2083">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-2083">Az.Sql</span></span>
* <span data-ttu-id="865fa-2084">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2084">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="865fa-2085">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2085">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-2086">Az.Websites</span></span>
* <span data-ttu-id="865fa-2087">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="865fa-2087">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="865fa-2088">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="865fa-2088">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-2089">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-2089">Az.Accounts</span></span>
* <span data-ttu-id="865fa-2090">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2090">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="865fa-2091">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2091">Az.AnalysisServices</span></span>
<span data-ttu-id="865fa-2092">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="865fa-2092">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-2093">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-2093">Az.Compute</span></span>
* <span data-ttu-id="865fa-2094">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2094">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="865fa-2095">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2095">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="865fa-2096">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2096">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2097">Az.RecoveryServices</span></span>
<span data-ttu-id="865fa-2098">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="865fa-2098">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-2099">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2099">Az.Resources</span></span>
* <span data-ttu-id="865fa-2100">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2100">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="865fa-2101">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2101">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="865fa-2102">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2102">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="865fa-2103">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2103">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-2104">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-2104">Az.Sql</span></span>
* <span data-ttu-id="865fa-2105">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2105">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="865fa-2106">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2106">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="865fa-2107">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2107">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="865fa-2108">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="865fa-2108">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-2109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-2109">Az.Accounts</span></span>
* <span data-ttu-id="865fa-2110">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="865fa-2110">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="865fa-2111">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2111">Az.AnalysisServices</span></span>
* <span data-ttu-id="865fa-2112">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="865fa-2112">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-2113">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2113">Az.RecoveryServices</span></span>
* <span data-ttu-id="865fa-2114">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="865fa-2114">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="865fa-2115">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="865fa-2115">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-2116">Az.Accounts</span></span>
* <span data-ttu-id="865fa-2117">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2117">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="865fa-2118">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2118">Update incorrect online help URLs</span></span>
* <span data-ttu-id="865fa-2119">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2119">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="865fa-2120">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="865fa-2120">Az.Aks</span></span>
* <span data-ttu-id="865fa-2121">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2121">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="865fa-2122">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-2122">Az.Automation</span></span>
* <span data-ttu-id="865fa-2123">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2123">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="865fa-2124">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2124">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="865fa-2125">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="865fa-2125">Az.Cdn</span></span>
* <span data-ttu-id="865fa-2126">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2126">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-2127">Az.Compute</span></span>
* <span data-ttu-id="865fa-2128">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2128">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="865fa-2129">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2129">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="865fa-2130">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2130">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="865fa-2131">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="865fa-2131">Az.ContainerRegistry</span></span>
* <span data-ttu-id="865fa-2132">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2132">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="865fa-2133">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="865fa-2133">Az.DataFactory</span></span>
* <span data-ttu-id="865fa-2134">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2134">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-2135">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-2135">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-2136">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2136">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="865fa-2137">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2137">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="865fa-2138">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2138">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-2139">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-2139">Az.IotHub</span></span>
* <span data-ttu-id="865fa-2140">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2140">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="865fa-2141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-2141">Az.KeyVault</span></span>
* <span data-ttu-id="865fa-2142">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2142">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-2143">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-2143">Az.Network</span></span>
* <span data-ttu-id="865fa-2144">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2144">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-2145">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2145">Az.Resources</span></span>
* <span data-ttu-id="865fa-2146">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2146">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="865fa-2147">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2147">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="865fa-2148">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="865fa-2148">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="865fa-2149">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2149">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="865fa-2150">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2150">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="865fa-2151">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2151">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="865fa-2152">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2152">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="865fa-2153">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-2153">Az.ServiceFabric</span></span>
* <span data-ttu-id="865fa-2154">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2154">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="865fa-2155">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2155">Fix some error messages.</span></span>
* <span data-ttu-id="865fa-2156">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2156">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="865fa-2157">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2157">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="865fa-2158">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="865fa-2158">Az.SignalR</span></span>
* <span data-ttu-id="865fa-2159">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2159">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-2160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-2160">Az.Sql</span></span>
* <span data-ttu-id="865fa-2161">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2161">Update incorrect online help URLs</span></span>
* <span data-ttu-id="865fa-2162">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2162">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="865fa-2163">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2163">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="865fa-2164">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-2164">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-2165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-2165">Az.Storage</span></span>
* <span data-ttu-id="865fa-2166">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2166">Update incorrect online help URLs</span></span>
* <span data-ttu-id="865fa-2167">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2167">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="865fa-2168">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="865fa-2168">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="865fa-2169">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="865fa-2169">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="865fa-2170">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="865fa-2170">Az.TrafficManager</span></span>
* <span data-ttu-id="865fa-2171">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2171">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-2172">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-2172">Az.Websites</span></span>
* <span data-ttu-id="865fa-2173">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2173">Update incorrect online help URLs</span></span>
* <span data-ttu-id="865fa-2174">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2174">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="865fa-2175">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2175">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="865fa-2176">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="865fa-2176">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="865fa-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-2177">Az.Accounts</span></span>
* <span data-ttu-id="865fa-2178">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2178">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-2179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-2179">Az.Compute</span></span>
* <span data-ttu-id="865fa-2180">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2180">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="865fa-2181">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2181">Updated the description of ID in help files</span></span>
* <span data-ttu-id="865fa-2182">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2182">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-2183">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-2183">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-2184">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2184">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="865fa-2185">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2185">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="865fa-2186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="865fa-2186">Az.EventGrid</span></span>
* <span data-ttu-id="865fa-2187">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2187">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="865fa-2188">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2188">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="865fa-2189">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2189">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="865fa-2190">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="865fa-2190">Event Time-To-Live,</span></span>
        - <span data-ttu-id="865fa-2191">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="865fa-2191">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="865fa-2192">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2192">Dead letter endpoint.</span></span>
    - <span data-ttu-id="865fa-2193">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2193">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="865fa-2194">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="865fa-2194">Event Time-To-Live,</span></span>
        - <span data-ttu-id="865fa-2195">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="865fa-2195">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="865fa-2196">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2196">Dead letter endpoint.</span></span>
* <span data-ttu-id="865fa-2197">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2197">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="865fa-2198">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2198">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="865fa-2199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="865fa-2199">Az.IotHub</span></span>
* <span data-ttu-id="865fa-2200">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="865fa-2200">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="865fa-2201">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="865fa-2201">Az.LogicApp</span></span>
* <span data-ttu-id="865fa-2202">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="865fa-2202">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-2203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2203">Az.Resources</span></span>
* <span data-ttu-id="865fa-2204">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2204">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="865fa-2205">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2205">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="865fa-2206">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2206">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="865fa-2207">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2207">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="865fa-2208">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="865fa-2208">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="865fa-2209">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2209">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="865fa-2210">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="865fa-2210">Az.SignalR</span></span>
* <span data-ttu-id="865fa-2211">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2211">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-2212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-2212">Az.Sql</span></span>
* <span data-ttu-id="865fa-2213">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2213">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="865fa-2214">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-2214">Az.Storage</span></span>
* <span data-ttu-id="865fa-2215">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2215">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="865fa-2216">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="865fa-2216">New-AzStorageContext</span></span>
* <span data-ttu-id="865fa-2217">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2217">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="865fa-2218">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="865fa-2218">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-2219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-2219">Az.Websites</span></span>
* <span data-ttu-id="865fa-2220">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2220">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="865fa-2221">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2221">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="865fa-2222">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="865fa-2222">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="865fa-2223">일반</span><span class="sxs-lookup"><span data-stu-id="865fa-2223">General</span></span>

- <span data-ttu-id="865fa-2224">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="865fa-2224">General Availability of Az Module</span></span>
- <span data-ttu-id="865fa-2225">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="865fa-2225">Online help for each module</span></span>
- <span data-ttu-id="865fa-2226">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2226">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="865fa-2227">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2227">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="865fa-2228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="865fa-2228">Az.Accounts</span></span>
- <span data-ttu-id="865fa-2229">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="865fa-2229">Changed from Az.Profile</span></span>
- <span data-ttu-id="865fa-2230">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2230">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="865fa-2231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-2231">Az.ApiManagement</span></span>
- <span data-ttu-id="865fa-2232">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2232">Fixes for #7002</span></span>
- <span data-ttu-id="865fa-2233">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2233">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="865fa-2234">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="865fa-2234">Az.Batch</span></span>
- <span data-ttu-id="865fa-2235">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2235">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="865fa-2236">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2236">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="865fa-2237">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2237">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="865fa-2238">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="865fa-2238">Az.Billing</span></span>
- <span data-ttu-id="865fa-2239">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2239">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="865fa-2240">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2240">Az.CognitivServices</span></span>
- <span data-ttu-id="865fa-2241">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2241">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="865fa-2242">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-2242">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="865fa-2243">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="865fa-2243">Az.ContainerInstance</span></span>
- <span data-ttu-id="865fa-2244">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-2244">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="865fa-2245">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="865fa-2245">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="865fa-2246">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2246">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="865fa-2247">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-2247">Az.DataLakeStore</span></span>
- <span data-ttu-id="865fa-2248">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2248">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="865fa-2249">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="865fa-2249">Az.Monitor</span></span>
- <span data-ttu-id="865fa-2250">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2250">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="865fa-2251">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="865fa-2251">Az.KeyVault</span></span>
- <span data-ttu-id="865fa-2252">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="865fa-2252">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="865fa-2253">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="865fa-2253">Az.MachineLearning</span></span>
- <span data-ttu-id="865fa-2254">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="865fa-2254">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="865fa-2255">Az.Media</span><span class="sxs-lookup"><span data-stu-id="865fa-2255">Az.Media</span></span>
- <span data-ttu-id="865fa-2256">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="865fa-2256">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="865fa-2257">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-2257">Az.Network</span></span>
<span data-ttu-id="865fa-2258">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-2258">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="865fa-2259">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2259">New cmdlets added:</span></span>
        - <span data-ttu-id="865fa-2260">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="865fa-2260">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="865fa-2261">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="865fa-2261">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="865fa-2262">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="865fa-2262">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="865fa-2263">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="865fa-2263">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="865fa-2264">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="865fa-2264">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="865fa-2265">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="865fa-2265">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="865fa-2266">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="865fa-2266">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="865fa-2267">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="865fa-2267">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="865fa-2268">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="865fa-2268">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="865fa-2269">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="865fa-2269">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="865fa-2270">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="865fa-2270">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="865fa-2271">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="865fa-2271">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="865fa-2272">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-2272">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="865fa-2273">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-2273">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="865fa-2274">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2274">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="865fa-2275">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="865fa-2275">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="865fa-2276">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="865fa-2276">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="865fa-2277">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="865fa-2277">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="865fa-2278">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="865fa-2278">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="865fa-2279">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="865fa-2279">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="865fa-2280">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2280">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="865fa-2281">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-2281">Az.OperationalInsights</span></span>
- <span data-ttu-id="865fa-2282">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2282">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="865fa-2283">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="865fa-2283">Az.Profile</span></span>
- <span data-ttu-id="865fa-2284">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="865fa-2284">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-2285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2285">Az.RecoveryServices</span></span>
- <span data-ttu-id="865fa-2286">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="865fa-2287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2287">Az.Resources</span></span>
- <span data-ttu-id="865fa-2288">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="865fa-2289">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-2289">Az.ServiceFabric</span></span>
- <span data-ttu-id="865fa-2290">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-2290">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="865fa-2291">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2291">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="865fa-2292">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="865fa-2292">Az.SIgnalR</span></span>
- <span data-ttu-id="865fa-2293">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="865fa-2293">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="865fa-2294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-2294">Az.Sql</span></span>
- <span data-ttu-id="865fa-2295">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2295">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="865fa-2296">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2296">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="865fa-2297">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2297">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="865fa-2298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-2298">Az.Storage</span></span>
- <span data-ttu-id="865fa-2299">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2299">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="865fa-2300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-2300">Az.Websites</span></span>
- <span data-ttu-id="865fa-2301">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="865fa-2301">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="865fa-2302">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="865fa-2302">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="865fa-2303">일반</span><span class="sxs-lookup"><span data-stu-id="865fa-2303">General</span></span>

* <span data-ttu-id="865fa-2304">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="865fa-2304">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="865fa-2305">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-2305">Az.Compute</span></span>

* <span data-ttu-id="865fa-2306">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2306">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="865fa-2307">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-2307">Az.DataLakeStore</span></span>

* <span data-ttu-id="865fa-2308">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2308">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="865fa-2309">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="865fa-2309">Az.FrontDoor</span></span>

* <span data-ttu-id="865fa-2310">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2310">Fixed some broken links</span></span>
    - <span data-ttu-id="865fa-2311">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2311">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="865fa-2312">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2312">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="865fa-2313">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2313">Az.RecoveryServices</span></span>

* <span data-ttu-id="865fa-2314">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2314">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="865fa-2315">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2315">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="865fa-2316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2316">Az.Resources</span></span>

* <span data-ttu-id="865fa-2317">https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2317">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="865fa-2318">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2318">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="865fa-2319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-2319">Az.Sql</span></span>

* <span data-ttu-id="865fa-2320">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="865fa-2320">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="865fa-2321">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="865fa-2321">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="865fa-2322">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2322">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="865fa-2323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-2323">Az.Storage</span></span>

* <span data-ttu-id="865fa-2324">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2324">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="865fa-2325">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2325">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="865fa-2326">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="865fa-2326">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="865fa-2327">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="865fa-2327">Support Static Website configuration</span></span>
    - <span data-ttu-id="865fa-2328">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="865fa-2328">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="865fa-2329">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="865fa-2329">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="865fa-2330">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-2330">Az.Websites</span></span>

* <span data-ttu-id="865fa-2331">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="865fa-2331">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="865fa-2332">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2332">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="865fa-2333">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2333">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="865fa-2334">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="865fa-2334">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="865fa-2335">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="865fa-2335">Az.ApiManagement</span></span>
* <span data-ttu-id="865fa-2336">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2336">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="865fa-2337">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="865fa-2337">Az.Automation</span></span>
* <span data-ttu-id="865fa-2338">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="865fa-2338">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="865fa-2339">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2339">Added Update Management cmdlets</span></span>
* <span data-ttu-id="865fa-2340">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2340">Added Source Control cmdlets</span></span>
* <span data-ttu-id="865fa-2341">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2341">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="865fa-2342">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2342">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="865fa-2343">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-2343">Az.Compute</span></span>
* <span data-ttu-id="865fa-2344">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2344">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="865fa-2345">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2345">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="865fa-2346">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="865fa-2346">Az.ContainerInstance</span></span>
* <span data-ttu-id="865fa-2347">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2347">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="865fa-2348">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="865fa-2348">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="865fa-2349">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2349">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="865fa-2350">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-2350">Az.Network</span></span>
* <span data-ttu-id="865fa-2351">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2351">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="865fa-2352">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2352">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="865fa-2353">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2353">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="865fa-2354">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="865fa-2354">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="865fa-2355">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="865fa-2355">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="865fa-2356">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2356">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="865fa-2357">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2357">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="865fa-2358">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="865fa-2358">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="865fa-2359">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="865fa-2359">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="865fa-2360">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2360">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="865fa-2361">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="865fa-2361">Az.Relay</span></span>
* <span data-ttu-id="865fa-2362">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2362">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="865fa-2363">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2363">Az.Resources</span></span>
* <span data-ttu-id="865fa-2364">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="865fa-2364">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="865fa-2365">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2365">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="865fa-2366">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="865fa-2366">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="865fa-2367">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-2367">Az.ServiceFabric</span></span>
* <span data-ttu-id="865fa-2368">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2368">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="865fa-2369">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-2369">Az.Sql</span></span>
* <span data-ttu-id="865fa-2370">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2370">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="865fa-2371">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="865fa-2371">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="865fa-2372">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="865fa-2372">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="865fa-2373">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="865fa-2373">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="865fa-2374">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="865fa-2374">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="865fa-2375">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="865fa-2375">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="865fa-2376">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="865fa-2376">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="865fa-2377">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="865fa-2377">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="865fa-2378">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="865fa-2378">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="865fa-2379">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2379">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="865fa-2380">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2380">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="865fa-2381">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2381">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="865fa-2382">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="865fa-2382">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="865fa-2383">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="865fa-2383">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="865fa-2384">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="865fa-2384">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="865fa-2385">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="865fa-2385">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="865fa-2386">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="865fa-2386">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="865fa-2387">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="865fa-2387">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="865fa-2388">일반</span><span class="sxs-lookup"><span data-stu-id="865fa-2388">General</span></span>
* <span data-ttu-id="865fa-2389">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2389">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="865fa-2390">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="865fa-2390">Az.Profile</span></span>
* <span data-ttu-id="865fa-2391">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2391">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="865fa-2392">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="865fa-2392">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="865fa-2393">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="865fa-2393">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="865fa-2394">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2394">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="865fa-2395">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2395">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="865fa-2396">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2396">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="865fa-2397">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2397">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="865fa-2398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2398">Az.CognitiveServices</span></span>
* <span data-ttu-id="865fa-2399">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2399">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-2400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-2400">Az.Compute</span></span>
* <span data-ttu-id="865fa-2401">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="865fa-2401">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="865fa-2402">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="865fa-2402">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="865fa-2403">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2403">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-2404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-2404">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-2405">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2405">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="865fa-2406">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2406">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="865fa-2407">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="865fa-2407">Az.Insights</span></span>
* <span data-ttu-id="865fa-2408">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="865fa-2408">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="865fa-2409">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="865fa-2409">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="865fa-2410">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="865fa-2410">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="865fa-2411">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="865fa-2411">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-2412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-2412">Az.Network</span></span>
* <span data-ttu-id="865fa-2413">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2413">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="865fa-2414">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="865fa-2414">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="865fa-2415">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="865fa-2415">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="865fa-2416">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="865fa-2416">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="865fa-2417">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="865fa-2417">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="865fa-2418">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="865fa-2418">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="865fa-2419">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="865fa-2419">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="865fa-2420">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="865fa-2420">Az.PolicyInsights</span></span>
* <span data-ttu-id="865fa-2421">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="865fa-2421">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-2422">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2422">Az.Resources</span></span>
* <span data-ttu-id="865fa-2423">https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2423">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="865fa-2424">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="865fa-2424">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="865fa-2425">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="865fa-2425">Az.ServiceBus</span></span>
* <span data-ttu-id="865fa-2426">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="865fa-2426">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="865fa-2427">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="865fa-2427">Az.ServiceFabric</span></span>
* <span data-ttu-id="865fa-2428">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="865fa-2428">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="865fa-2429">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2429">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="865fa-2430">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="865fa-2430">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="865fa-2431">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="865fa-2431">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="865fa-2432">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="865fa-2432">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="865fa-2433">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="865fa-2433">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="865fa-2434">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="865fa-2434">Az.Profile</span></span>
* <span data-ttu-id="865fa-2435">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2435">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="865fa-2436">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2436">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-2437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-2437">Az.Compute</span></span>
* <span data-ttu-id="865fa-2438">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2438">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="865fa-2439">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2439">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="865fa-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="865fa-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="865fa-2441">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2441">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="865fa-2442">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2442">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="865fa-2443">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2443">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="865fa-2444">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2444">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="865fa-2445">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2445">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-2446">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-2446">Az.Network</span></span>
* <span data-ttu-id="865fa-2447">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2447">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="865fa-2448">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2448">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-2449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2449">Az.Resources</span></span>
* <span data-ttu-id="865fa-2450">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2450">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="865fa-2451">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2451">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="865fa-2452">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="865fa-2452">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="865fa-2453">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="865fa-2453">Azure.Storage</span></span>
* <span data-ttu-id="865fa-2454">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2454">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="865fa-2455">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="865fa-2455">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="865fa-2456">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="865fa-2456">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="865fa-2457">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2457">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="865fa-2458">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="865fa-2458">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="865fa-2459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="865fa-2459">Az.CognitiveServices</span></span>
* <span data-ttu-id="865fa-2460">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2460">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="865fa-2461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="865fa-2461">Az.Compute</span></span>
* <span data-ttu-id="865fa-2462">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2462">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="865fa-2463">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="865fa-2463">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="865fa-2464">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2464">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="865fa-2465">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="865fa-2465">Az.DataFactoryV2</span></span>
* <span data-ttu-id="865fa-2466">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="865fa-2466">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="865fa-2467">Az.Network</span><span class="sxs-lookup"><span data-stu-id="865fa-2467">Az.Network</span></span>
* <span data-ttu-id="865fa-2468">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2468">Added NetworkProfile functionality.</span></span> <span data-ttu-id="865fa-2469">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2469">new cmdlets added</span></span>
    - <span data-ttu-id="865fa-2470">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="865fa-2470">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="865fa-2471">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="865fa-2471">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="865fa-2472">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="865fa-2472">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="865fa-2473">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="865fa-2473">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="865fa-2474">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-2474">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="865fa-2475">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="865fa-2475">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="865fa-2476">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2476">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="865fa-2477">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2477">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="865fa-2478">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2478">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="865fa-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="865fa-2479">Az.RedisCache</span></span>
* <span data-ttu-id="865fa-2480">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="865fa-2480">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="865fa-2481">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2481">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="865fa-2482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="865fa-2482">Az.Resources</span></span>
* <span data-ttu-id="865fa-2483">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="865fa-2483">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="865fa-2484">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="865fa-2484">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="865fa-2485">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="865fa-2485">Az.Sql</span></span>
* <span data-ttu-id="865fa-2486">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="865fa-2486">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="865fa-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="865fa-2487">Az.Websites</span></span>
* <span data-ttu-id="865fa-2488">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2488">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="865fa-2489">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="865fa-2489">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="865fa-2490">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="865fa-2490">0.2.0 - September 2018</span></span>
 <span data-ttu-id="865fa-2491">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="865fa-2491">Initial Release</span></span>
