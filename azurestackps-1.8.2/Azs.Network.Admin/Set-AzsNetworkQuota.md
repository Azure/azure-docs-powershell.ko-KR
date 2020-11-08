---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d20f84d91c110ae1f4e55508b33f758fc0d5583
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046887"
---
# <span data-ttu-id="16f94-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="16f94-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="16f94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16f94-102">SYNOPSIS</span></span>
<span data-ttu-id="16f94-103">할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-103">Create or update a quota.</span></span>

## <span data-ttu-id="16f94-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16f94-104">SYNTAX</span></span>

### <span data-ttu-id="16f94-105">할당량 (기본값)</span><span class="sxs-lookup"><span data-stu-id="16f94-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f94-106">리소스</span><span class="sxs-lookup"><span data-stu-id="16f94-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16f94-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="16f94-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16f94-108">설명은</span><span class="sxs-lookup"><span data-stu-id="16f94-108">DESCRIPTION</span></span>
<span data-ttu-id="16f94-109">할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-109">Create or update a quota.</span></span>

## <span data-ttu-id="16f94-110">예제의</span><span class="sxs-lookup"><span data-stu-id="16f94-110">EXAMPLES</span></span>

### <span data-ttu-id="16f94-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="16f94-111">EXAMPLE 1</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="16f94-112">이름으로 네트워크 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-112">Update a network quota by name.</span></span>

### <span data-ttu-id="16f94-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="16f94-113">EXAMPLE 2</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="16f94-114">이름으로 네트워크 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-114">Update a network quota by name.</span></span>

## <span data-ttu-id="16f94-115">변수</span><span class="sxs-lookup"><span data-stu-id="16f94-115">PARAMETERS</span></span>

### <span data-ttu-id="16f94-116">-이름</span><span class="sxs-lookup"><span data-stu-id="16f94-116">-Name</span></span>
<span data-ttu-id="16f94-117">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-117">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-118">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="16f94-118">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="16f94-119">구독 당 허용 되는 최대 Nic입니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-119">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-120">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="16f94-120">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="16f94-121">구독 당 허용 되는 최대 공개 IP 주소</span><span class="sxs-lookup"><span data-stu-id="16f94-121">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="16f94-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="16f94-123">구독 당 허용 되는 가상 네트워크 게이트웨이 연결의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-123">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-124">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="16f94-124">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="16f94-125">구독 당 허용 되는 가상 네트워크 maxium 수입니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-125">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-126">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="16f94-126">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="16f94-127">구독 당 허용 되는 최대 가상 네트워크 게이트웨이 수입니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-127">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-128">-Maxsecurity그룹 Persubscription</span><span class="sxs-lookup"><span data-stu-id="16f94-128">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="16f94-129">구독 당 허용 되는 최대 보안 그룹 수입니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-129">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-130">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="16f94-130">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="16f94-131">구독 당 허용 되는 최대 부하 분산 장치 수입니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-131">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-132">-위치</span><span class="sxs-lookup"><span data-stu-id="16f94-132">-Location</span></span>
<span data-ttu-id="16f94-133">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-133">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16f94-134">-ResourceId</span></span>
<span data-ttu-id="16f94-135">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16f94-136">-InputObject</span></span>
<span data-ttu-id="16f94-137">Get-AzsNetworkQuota에서 반환 된 Posbbily 수정한 네트워크 할당량</span><span class="sxs-lookup"><span data-stu-id="16f94-137">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

```yaml
Type: Quota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16f94-138">-WhatIf</span></span>
<span data-ttu-id="16f94-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16f94-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-141">-확인</span><span class="sxs-lookup"><span data-stu-id="16f94-141">-Confirm</span></span>
<span data-ttu-id="16f94-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f94-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f94-143">CommonParameters</span></span>
<span data-ttu-id="16f94-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16f94-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f94-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16f94-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f94-146">입력</span><span class="sxs-lookup"><span data-stu-id="16f94-146">INPUTS</span></span>

## <span data-ttu-id="16f94-147">출력</span><span class="sxs-lookup"><span data-stu-id="16f94-147">OUTPUTS</span></span>

### <span data-ttu-id="16f94-148">Microsoft AzureStack. 관리자. i a 관리. 할당량</span><span class="sxs-lookup"><span data-stu-id="16f94-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="16f94-149">상속자</span><span class="sxs-lookup"><span data-stu-id="16f94-149">NOTES</span></span>

## <span data-ttu-id="16f94-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16f94-150">RELATED LINKS</span></span>
