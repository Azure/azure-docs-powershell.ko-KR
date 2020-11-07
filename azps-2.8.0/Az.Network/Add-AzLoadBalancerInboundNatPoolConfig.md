---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 672829daffa2117265e8f43b30f504adc702f3d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870861"
---
# <span data-ttu-id="b2909-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2909-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b2909-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2909-102">SYNOPSIS</span></span>
<span data-ttu-id="b2909-103">부하 분산 장치에 인바운드 NAT 풀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="b2909-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2909-104">SYNTAX</span></span>

### <span data-ttu-id="b2909-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="b2909-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2909-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2909-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2909-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b2909-107">DESCRIPTION</span></span>
<span data-ttu-id="b2909-108">**Add-AzLoadBalancerInboundNatPoolConfig** cmdlet은 부하 분산 장치에 인바운드 NAT 풀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="b2909-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b2909-109">EXAMPLES</span></span>

### <span data-ttu-id="b2909-110">1: 추가</span><span class="sxs-lookup"><span data-stu-id="b2909-110">1: Add</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="b2909-111">변수</span><span class="sxs-lookup"><span data-stu-id="b2909-111">PARAMETERS</span></span>

### <span data-ttu-id="b2909-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b2909-112">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2909-113">-DefaultProfile</span></span>
<span data-ttu-id="b2909-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b2909-115">-EnableFloatingIP</span></span>
<span data-ttu-id="b2909-116">SQL AlwaysOn 가용성 그룹을 구성 하는 데 필요한 부동 IP 접근 권한 값에 대 한 가상 컴퓨터의 끝점을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="b2909-117">SQL server에서 SQL AlwaysOn 가용성 그룹을 사용 하는 경우이 설정이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="b2909-118">끝점을 만든 후에는이 설정을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-118">This setting can't be changed after you create the endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b2909-119">-EnableTcpReset</span></span>
<span data-ttu-id="b2909-120">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b2909-121">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-121">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2909-122">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b2909-123">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="b2909-124">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="b2909-125">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b2909-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b2909-127">TCP 유휴 연결에 대 한 제한 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="b2909-128">값을 4 ~ 30 분 사이로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="b2909-129">기본값은 4 분입니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-129">The default value is 4 minutes.</span></span> <span data-ttu-id="b2909-130">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-130">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b2909-131">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-132">-이름</span><span class="sxs-lookup"><span data-stu-id="b2909-132">-Name</span></span>
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

### <span data-ttu-id="b2909-133">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="b2909-133">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2909-134">-확인</span><span class="sxs-lookup"><span data-stu-id="b2909-134">-Confirm</span></span>
<span data-ttu-id="b2909-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2909-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2909-136">-WhatIf</span></span>
<span data-ttu-id="b2909-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2909-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2909-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2909-139">CommonParameters</span></span>
<span data-ttu-id="b2909-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2909-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2909-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2909-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2909-142">입력</span><span class="sxs-lookup"><span data-stu-id="b2909-142">INPUTS</span></span>

### <span data-ttu-id="b2909-143">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b2909-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b2909-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b2909-144">System.String</span></span>

### <span data-ttu-id="b2909-145">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="b2909-145">System.Int32</span></span>

### <span data-ttu-id="b2909-146">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b2909-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b2909-147">출력</span><span class="sxs-lookup"><span data-stu-id="b2909-147">OUTPUTS</span></span>

### <span data-ttu-id="b2909-148">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b2909-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b2909-149">상속자</span><span class="sxs-lookup"><span data-stu-id="b2909-149">NOTES</span></span>

## <span data-ttu-id="b2909-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2909-150">RELATED LINKS</span></span>

[<span data-ttu-id="b2909-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2909-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b2909-152">새로운 AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2909-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b2909-153">제거-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2909-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b2909-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2909-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
