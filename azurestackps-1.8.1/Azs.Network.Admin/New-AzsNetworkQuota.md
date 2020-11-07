---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875126"
---
# <span data-ttu-id="8254c-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="8254c-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="8254c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8254c-102">SYNOPSIS</span></span>
<span data-ttu-id="8254c-103">할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-103">Create or update a quota.</span></span>

## <span data-ttu-id="8254c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8254c-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8254c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8254c-105">DESCRIPTION</span></span>
<span data-ttu-id="8254c-106">할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-106">Create or update a quota.</span></span>

## <span data-ttu-id="8254c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8254c-107">EXAMPLES</span></span>

### <span data-ttu-id="8254c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8254c-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="8254c-109">모든 기본값을 사용 하 여 새 네트워크 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="8254c-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="8254c-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="8254c-111">할당량 값이 아닌 새 네트워크 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="8254c-112">변수</span><span class="sxs-lookup"><span data-stu-id="8254c-112">PARAMETERS</span></span>

### <span data-ttu-id="8254c-113">-이름</span><span class="sxs-lookup"><span data-stu-id="8254c-113">-Name</span></span>
<span data-ttu-id="8254c-114">네트워크 할당량 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-114">Name of the network quota resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254c-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8254c-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="8254c-116">구독 당 허용 되는 최대 Nic입니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-116">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254c-117">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8254c-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="8254c-118">구독 당 허용 되는 최대 공개 IP 주소</span><span class="sxs-lookup"><span data-stu-id="8254c-118">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254c-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8254c-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="8254c-120">구독 당 허용 되는 가상 네트워크 게이트웨이 연결의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254c-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8254c-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="8254c-122">구독 당 허용 되는 가상 네트워크 maxium 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-122">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254c-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8254c-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="8254c-124">구독 당 허용 되는 최대 가상 네트워크 게이트웨이 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254c-125">-Maxsecurity그룹 Persubscription</span><span class="sxs-lookup"><span data-stu-id="8254c-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="8254c-126">구독 당 허용 되는 최대 보안 그룹 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-126">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254c-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8254c-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="8254c-128">구독 당 허용 되는 최대 부하 분산 장치 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-128">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254c-129">-위치</span><span class="sxs-lookup"><span data-stu-id="8254c-129">-Location</span></span>
<span data-ttu-id="8254c-130">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-130">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254c-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="8254c-131">-MigrationPhase</span></span>
<span data-ttu-id="8254c-132">마이그레이션 상태 (예: 없음, 준비, 커밋, 중단)입니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8254c-133">-WhatIf</span></span>
<span data-ttu-id="8254c-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8254c-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8254c-136">-확인</span><span class="sxs-lookup"><span data-stu-id="8254c-136">-Confirm</span></span>
<span data-ttu-id="8254c-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8254c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8254c-138">CommonParameters</span></span>
<span data-ttu-id="8254c-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8254c-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8254c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8254c-141">입력</span><span class="sxs-lookup"><span data-stu-id="8254c-141">INPUTS</span></span>

## <span data-ttu-id="8254c-142">출력</span><span class="sxs-lookup"><span data-stu-id="8254c-142">OUTPUTS</span></span>

### <span data-ttu-id="8254c-143">Microsoft AzureStack. 관리자. i a 관리. 할당량</span><span class="sxs-lookup"><span data-stu-id="8254c-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="8254c-144">상속자</span><span class="sxs-lookup"><span data-stu-id="8254c-144">NOTES</span></span>

## <span data-ttu-id="8254c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8254c-145">RELATED LINKS</span></span>
