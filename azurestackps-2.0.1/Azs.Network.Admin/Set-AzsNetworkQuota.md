---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045262"
---
# <span data-ttu-id="ab1e6-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="ab1e6-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="ab1e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1e6-103">할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-103">Create or update a quota.</span></span>

## <span data-ttu-id="ab1e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab1e6-104">SYNTAX</span></span>

### <span data-ttu-id="ab1e6-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ab1e6-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ab1e6-106">Update</span><span class="sxs-lookup"><span data-stu-id="ab1e6-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ab1e6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ab1e6-107">DESCRIPTION</span></span>
<span data-ttu-id="ab1e6-108">할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-108">Create or update a quota.</span></span>

## <span data-ttu-id="ab1e6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ab1e6-109">EXAMPLES</span></span>

### <span data-ttu-id="ab1e6-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ab1e6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="ab1e6-111">이름으로 네트워크 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-111">Update a network quota by name.</span></span>

### <span data-ttu-id="ab1e6-112">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ab1e6-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="ab1e6-113">이름으로 네트워크 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-113">Update a network quota by name.</span></span>

## <span data-ttu-id="ab1e6-114">변수</span><span class="sxs-lookup"><span data-stu-id="ab1e6-114">PARAMETERS</span></span>

### <span data-ttu-id="ab1e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab1e6-115">-DefaultProfile</span></span>
<span data-ttu-id="ab1e6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab1e6-117">-위치</span><span class="sxs-lookup"><span data-stu-id="ab1e6-117">-Location</span></span>
<span data-ttu-id="ab1e6-118">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1e6-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="ab1e6-120">테 넌 트 구독이 프로 비전 할 수 있는 최대 부하 분산 장치 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1e6-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="ab1e6-122">테 넌 트 구독이 프로 비전 할 수 있는 최대 Nic 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-122">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-123">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1e6-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="ab1e6-124">테 넌 트 구독이 프로 비전 할 수 있는 최대 공용 IP 주소 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-125">-Maxsecurity그룹 Persubscription</span><span class="sxs-lookup"><span data-stu-id="ab1e6-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="ab1e6-126">테 넌 트 구독이 프로 비전 할 수 있는 최대 보안 그룹 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-126">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1e6-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="ab1e6-128">테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이 연결의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1e6-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="ab1e6-130">테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1e6-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="ab1e6-132">테 넌 트 구독이 프로 비전 할 수 있는 최대 가상 네트워크 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-133">-이름</span><span class="sxs-lookup"><span data-stu-id="ab1e6-133">-Name</span></span>
<span data-ttu-id="ab1e6-134">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-134">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-135">-할당량</span><span class="sxs-lookup"><span data-stu-id="ab1e6-135">-Quota</span></span>
<span data-ttu-id="ab1e6-136">네트워크 할당량 리소스.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-136">Network quota resource.</span></span>
<span data-ttu-id="ab1e6-137">생성 하려면 할당량 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab1e6-138">-SubscriptionId</span></span>
<span data-ttu-id="ab1e6-139">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ab1e6-140">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-141">태그</span><span class="sxs-lookup"><span data-stu-id="ab1e6-141">-Tag</span></span>
<span data-ttu-id="ab1e6-142">키 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab1e6-143">-확인</span><span class="sxs-lookup"><span data-stu-id="ab1e6-143">-Confirm</span></span>
<span data-ttu-id="ab1e6-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab1e6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab1e6-145">-WhatIf</span></span>
<span data-ttu-id="ab1e6-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab1e6-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab1e6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1e6-148">CommonParameters</span></span>
<span data-ttu-id="ab1e6-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1e6-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1e6-151">입력</span><span class="sxs-lookup"><span data-stu-id="ab1e6-151">INPUTS</span></span>

### <span data-ttu-id="ab1e6-152">Api20150615 (Microsoft. PowerShell. i N.exe 할당량</span><span class="sxs-lookup"><span data-stu-id="ab1e6-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="ab1e6-153">출력</span><span class="sxs-lookup"><span data-stu-id="ab1e6-153">OUTPUTS</span></span>

### <span data-ttu-id="ab1e6-154">Api20150615 (Microsoft. PowerShell. i N.exe 할당량</span><span class="sxs-lookup"><span data-stu-id="ab1e6-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="ab1e6-155">상속자</span><span class="sxs-lookup"><span data-stu-id="ab1e6-155">NOTES</span></span>

<span data-ttu-id="ab1e6-156">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab1e6-157">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ab1e6-158">할당량 <IQuota> : 네트워크 할당량 리소스.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="ab1e6-159">`[Tag <IResourceTags>]`: 키 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="ab1e6-160">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ab1e6-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 최대 부하 분산 장치 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="ab1e6-162">`[MaxNicsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 최대 Nic 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="ab1e6-163">`[MaxPublicIpsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 공용 IP 주소의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="ab1e6-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 최대 보안 그룹 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="ab1e6-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이 연결의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="ab1e6-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크 게이트웨이의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="ab1e6-167">`[MaxVnetsPerSubscription <Int64?>]`: 테 넌 트 구독이 프로 비전 할 수 있는 가상 네트워크의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ab1e6-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="ab1e6-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab1e6-168">RELATED LINKS</span></span>

