---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: dd2c0064b92ff96fedd9e06c32b2f2f0f5a2c65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536572"
---
# <span data-ttu-id="ad164-101">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad164-101">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="ad164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad164-102">SYNOPSIS</span></span>
<span data-ttu-id="ad164-103">부하 분산 장치에 대 한 아웃 바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-103">Creates an outbound rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad164-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad164-104">SYNTAX</span></span>

### <span data-ttu-id="ad164-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad164-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad164-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad164-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad164-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ad164-107">DESCRIPTION</span></span>
<span data-ttu-id="ad164-108">**AzureRmLoadBalancerOutboundRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 아웃 바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-108">The **New-AzureRmLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ad164-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ad164-109">EXAMPLES</span></span>

### <span data-ttu-id="ad164-110">예제 1: 부하 분산 장치에 대 한 아웃 바운드 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="ad164-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\>$frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzureRmLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="ad164-111">첫 번째 명령은 MyResourceGroup 이라는 리소스 그룹에 MyPublicIP 이라는 공용 IP 주소를 만든 다음이를 $publicip 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="ad164-112">두 번째 명령은 $publicip에서 공용 IP 주소를 사용 하 여 FrontendIpConfig01 라는 프런트 엔드 IP 구성을 만든 다음 $frontend 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="ad164-113">세 번째 명령은 BackendAddressPool01 이라는 백 엔드 주소 풀 구성을 만든 다음이를 $backend 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="ad164-114">네 번째 명령은 $frontend 및 $backend의 프런트 엔드 및 백 엔드 개체를 사용 하 여 MyOutboundRule 이라는 아웃 바운드 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="ad164-115">*프로토콜* , *FrontendIPConfiguration* 및 *BackendAddressPool* 매개 변수는 모두 아웃 바운드 규칙 구성을 만드는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="ad164-116">변수</span><span class="sxs-lookup"><span data-stu-id="ad164-116">PARAMETERS</span></span>

### <span data-ttu-id="ad164-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="ad164-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="ad164-118">NAT에 사용 되는 아웃 바운드 포트의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-118">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="ad164-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ad164-119">-BackendAddressPool</span></span>
<span data-ttu-id="ad164-120">Dip 풀에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="ad164-121">아웃 바운드 트래픽은 백 엔드 Ip의 Ip에서 임의로 부하 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="ad164-122">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ad164-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="ad164-123">Dip 풀에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="ad164-124">아웃 바운드 트래픽은 백 엔드 Ip의 Ip에서 임의로 부하 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="ad164-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad164-125">-DefaultProfile</span></span>
<span data-ttu-id="ad164-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad164-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ad164-127">-EnableTcpReset</span></span>
<span data-ttu-id="ad164-128">TCP 흐름 유휴 시간 제한 또는 예기치 않은 연결 종료 시 양방향 TCP 재설정을 수신 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="ad164-129">이 요소는 프로토콜이 TCP로 설정 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ad164-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad164-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ad164-131">부하 분산 장치의 프런트 엔드 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-131">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad164-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ad164-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ad164-133">TCP 유휴 연결의 제한 시간</span><span class="sxs-lookup"><span data-stu-id="ad164-133">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="ad164-134">-이름</span><span class="sxs-lookup"><span data-stu-id="ad164-134">-Name</span></span>
<span data-ttu-id="ad164-135">아웃 바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="ad164-136">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="ad164-136">-Protocol</span></span>
<span data-ttu-id="ad164-137">프로토콜-TCP, UDP 또는 All</span><span class="sxs-lookup"><span data-stu-id="ad164-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="ad164-138">-확인</span><span class="sxs-lookup"><span data-stu-id="ad164-138">-Confirm</span></span>
<span data-ttu-id="ad164-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad164-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad164-140">-WhatIf</span></span>
<span data-ttu-id="ad164-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad164-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad164-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad164-143">CommonParameters</span></span>
<span data-ttu-id="ad164-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad164-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad164-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad164-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad164-146">입력</span><span class="sxs-lookup"><span data-stu-id="ad164-146">INPUTS</span></span>

### <span data-ttu-id="ad164-147">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="ad164-147">System.Int32</span></span>
<span data-ttu-id="ad164-148">System.webserver. 컬렉션. 목록 \` 1 [[Microsoft azure.. 모델. PSResourceId, Microsoft azure. commands. 네트워크, 버전 = 6.5.0.0, Culture = 중립, PublicKeyToken = null]] Microsoft. \* PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ad164-148">System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="ad164-149">출력</span><span class="sxs-lookup"><span data-stu-id="ad164-149">OUTPUTS</span></span>

### <span data-ttu-id="ad164-150">PSOutboundRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ad164-150">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="ad164-151">상속자</span><span class="sxs-lookup"><span data-stu-id="ad164-151">NOTES</span></span>

## <span data-ttu-id="ad164-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad164-152">RELATED LINKS</span></span>
