---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 50a8cd14c6ea61f7c772df96f4addb9ae7955444
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869910"
---
# <span data-ttu-id="15cc3-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15cc3-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="15cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="15cc3-103">부하 분산 장치에 대 한 아웃 바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="15cc3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15cc3-104">SYNTAX</span></span>

### <span data-ttu-id="15cc3-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="15cc3-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15cc3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="15cc3-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15cc3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="15cc3-107">DESCRIPTION</span></span>
<span data-ttu-id="15cc3-108">**AzLoadBalancerOutboundRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 아웃 바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="15cc3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="15cc3-109">EXAMPLES</span></span>

### <span data-ttu-id="15cc3-110">예제 1: 부하 분산 장치에 대 한 아웃 바운드 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="15cc3-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="15cc3-111">첫 번째 명령은 MyResourceGroup 이라는 리소스 그룹에 MyPublicIP 이라는 공용 IP 주소를 만든 다음이를 $publicip 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="15cc3-112">두 번째 명령은 $publicip에서 공용 IP 주소를 사용 하 여 FrontendIpConfig01 라는 프런트 엔드 IP 구성을 만든 다음 $frontend 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="15cc3-113">세 번째 명령은 BackendAddressPool01 이라는 백 엔드 주소 풀 구성을 만든 다음이를 $backend 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="15cc3-114">네 번째 명령은 $frontend 및 $backend의 프런트 엔드 및 백 엔드 개체를 사용 하 여 MyOutboundRule 이라는 아웃 바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="15cc3-115">*프로토콜* , *FrontendIPConfiguration* 및 *BackendAddressPool* 매개 변수는 모두 아웃 바운드 규칙 구성을 만드는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="15cc3-116">변수</span><span class="sxs-lookup"><span data-stu-id="15cc3-116">PARAMETERS</span></span>

### <span data-ttu-id="15cc3-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="15cc3-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="15cc3-118">NAT에 사용 되는 아웃 바운드 포트의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-118">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="15cc3-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="15cc3-119">-BackendAddressPool</span></span>
<span data-ttu-id="15cc3-120">Dip 풀에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="15cc3-121">아웃 바운드 트래픽은 백 엔드 Ip의 Ip에서 임의로 부하 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15cc3-122">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="15cc3-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="15cc3-123">Dip 풀에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="15cc3-124">아웃 바운드 트래픽은 백 엔드 Ip의 Ip에서 임의로 부하 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15cc3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15cc3-125">-DefaultProfile</span></span>
<span data-ttu-id="15cc3-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15cc3-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="15cc3-127">-EnableTcpReset</span></span>
<span data-ttu-id="15cc3-128">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="15cc3-129">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="15cc3-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="15cc3-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="15cc3-131">부하 분산 장치의 프런트 엔드 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-131">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15cc3-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="15cc3-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="15cc3-133">TCP 유휴 연결의 제한 시간</span><span class="sxs-lookup"><span data-stu-id="15cc3-133">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="15cc3-134">-이름</span><span class="sxs-lookup"><span data-stu-id="15cc3-134">-Name</span></span>
<span data-ttu-id="15cc3-135">아웃 바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="15cc3-136">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="15cc3-136">-Protocol</span></span>
<span data-ttu-id="15cc3-137">프로토콜-TCP, UDP 또는 All</span><span class="sxs-lookup"><span data-stu-id="15cc3-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="15cc3-138">-확인</span><span class="sxs-lookup"><span data-stu-id="15cc3-138">-Confirm</span></span>
<span data-ttu-id="15cc3-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15cc3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15cc3-140">-WhatIf</span></span>
<span data-ttu-id="15cc3-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15cc3-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15cc3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15cc3-143">CommonParameters</span></span>
<span data-ttu-id="15cc3-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15cc3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15cc3-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15cc3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15cc3-146">입력</span><span class="sxs-lookup"><span data-stu-id="15cc3-146">INPUTS</span></span>

### <span data-ttu-id="15cc3-147">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="15cc3-147">System.Int32</span></span>

### <span data-ttu-id="15cc3-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="15cc3-148">System.String</span></span>

### <span data-ttu-id="15cc3-149">Microsoft. 네트워크 모델. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="15cc3-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="15cc3-150">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="15cc3-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="15cc3-151">출력</span><span class="sxs-lookup"><span data-stu-id="15cc3-151">OUTPUTS</span></span>

### <span data-ttu-id="15cc3-152">PSOutboundRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="15cc3-152">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="15cc3-153">상속자</span><span class="sxs-lookup"><span data-stu-id="15cc3-153">NOTES</span></span>

## <span data-ttu-id="15cc3-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15cc3-154">RELATED LINKS</span></span>

[<span data-ttu-id="15cc3-155">추가-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15cc3-155">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="15cc3-156">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15cc3-156">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="15cc3-157">제거-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15cc3-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="15cc3-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="15cc3-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
