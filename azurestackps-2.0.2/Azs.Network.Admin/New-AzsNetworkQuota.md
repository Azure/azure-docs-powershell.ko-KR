---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046870"
---
# <span data-ttu-id="d8c44-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="d8c44-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="d8c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8c44-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c44-103">할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-103">Create or update a quota.</span></span>

## <span data-ttu-id="d8c44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8c44-104">SYNTAX</span></span>

### <span data-ttu-id="d8c44-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="d8c44-105">CreateExpanded (Default)</span></span>
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8c44-106">만드는</span><span class="sxs-lookup"><span data-stu-id="d8c44-106">Create</span></span>
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8c44-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8c44-107">CreateViaIdentity</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8c44-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d8c44-108">CreateViaIdentityExpanded</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8c44-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d8c44-109">DESCRIPTION</span></span>
<span data-ttu-id="d8c44-110">할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-110">Create or update a quota.</span></span>

## <span data-ttu-id="d8c44-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d8c44-111">EXAMPLES</span></span>

### <span data-ttu-id="d8c44-112">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8c44-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="d8c44-113">모든 기본값을 사용 하 여 새 네트워크 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-113">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="d8c44-114">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8c44-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
<span data-ttu-id="d8c44-115">할당량 값이 아닌 새 네트워크 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-115">Create a new network quota with non default values for quota.</span></span>



## <span data-ttu-id="d8c44-116">변수</span><span class="sxs-lookup"><span data-stu-id="d8c44-116">PARAMETERS</span></span>

### <span data-ttu-id="d8c44-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c44-117">-DefaultProfile</span></span>
<span data-ttu-id="d8c44-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8c44-119">-InputObject</span></span>
<span data-ttu-id="d8c44-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-121">-위치</span><span class="sxs-lookup"><span data-stu-id="d8c44-121">-Location</span></span>
<span data-ttu-id="d8c44-122">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-123">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d8c44-123">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="d8c44-124">테 넌 트 구독이 프로 비전 할 수 있는 최대 부하 분산 장치 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-124">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-125">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d8c44-125">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="d8c44-126">테 넌 트 구독이 프로 비전 할 수 있는 최대 Nic 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-126">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-127">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d8c44-127">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="d8c44-128">테 넌 트 구독이 프로 비전 할 수 있는 최대 공용 IP 주소 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-128">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-129">-Maxsecurity그룹 Persubscription</span><span class="sxs-lookup"><span data-stu-id="d8c44-129">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="d8c44-130">테 넌 트 구독이 프로 비전 할 수 있는 최대 보안 그룹 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-130">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d8c44-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="d8c44-132">테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이 연결의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-132">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-133">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d8c44-133">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="d8c44-134">테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-134">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-135">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="d8c44-135">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="d8c44-136">테 넌 트 구독이 프로 비전 할 수 있는 최대 가상 네트워크 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-136">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-137">-이름</span><span class="sxs-lookup"><span data-stu-id="d8c44-137">-Name</span></span>
<span data-ttu-id="d8c44-138">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-138">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-139">-할당량</span><span class="sxs-lookup"><span data-stu-id="d8c44-139">-Quota</span></span>
<span data-ttu-id="d8c44-140">네트워크 할당량 리소스.</span><span class="sxs-lookup"><span data-stu-id="d8c44-140">Network quota resource.</span></span>
<span data-ttu-id="d8c44-141">생성 하려면 할당량 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-141">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8c44-142">-SubscriptionId</span></span>
<span data-ttu-id="d8c44-143">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-143">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d8c44-144">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-145">태그</span><span class="sxs-lookup"><span data-stu-id="d8c44-145">-Tag</span></span>
<span data-ttu-id="d8c44-146">키 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-146">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-147">-확인</span><span class="sxs-lookup"><span data-stu-id="d8c44-147">-Confirm</span></span>
<span data-ttu-id="d8c44-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c44-149">-WhatIf</span></span>
<span data-ttu-id="d8c44-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8c44-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8c44-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c44-152">CommonParameters</span></span>
<span data-ttu-id="d8c44-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c44-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8c44-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c44-155">입력</span><span class="sxs-lookup"><span data-stu-id="d8c44-155">INPUTS</span></span>

### <span data-ttu-id="d8c44-156">Api20150615 (Microsoft. PowerShell. i N.exe 할당량</span><span class="sxs-lookup"><span data-stu-id="d8c44-156">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

### <span data-ttu-id="d8c44-157">INetworkAdminIdentity (Microsoft. PowerShell. 관리자.</span><span class="sxs-lookup"><span data-stu-id="d8c44-157">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="d8c44-158">출력</span><span class="sxs-lookup"><span data-stu-id="d8c44-158">OUTPUTS</span></span>

### <span data-ttu-id="d8c44-159">Api20150615 (Microsoft. PowerShell. i N.exe 할당량</span><span class="sxs-lookup"><span data-stu-id="d8c44-159">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="d8c44-160">상속자</span><span class="sxs-lookup"><span data-stu-id="d8c44-160">NOTES</span></span>

<span data-ttu-id="d8c44-161">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-161">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8c44-162">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d8c44-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d8c44-163">INPUTOBJECT <INetworkAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d8c44-163">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8c44-164">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="d8c44-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8c44-165">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-165">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d8c44-166">`[ResourceName <String>]`: 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-166">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="d8c44-167">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-167">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d8c44-168">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-168">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="d8c44-169">할당량 <IQuota> : 네트워크 할당량 리소스.</span><span class="sxs-lookup"><span data-stu-id="d8c44-169">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="d8c44-170">`[Tag <IResourceTags>]`: 키 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-170">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="d8c44-171">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d8c44-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 최대 부하 분산 장치 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d8c44-173">`[MaxNicsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 최대 Nic 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-173">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d8c44-174">`[MaxPublicIpsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 공용 IP 주소의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d8c44-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 최대 보안 그룹 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d8c44-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이 연결의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d8c44-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="d8c44-178">`[MaxVnetsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c44-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="d8c44-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8c44-179">RELATED LINKS</span></span>

