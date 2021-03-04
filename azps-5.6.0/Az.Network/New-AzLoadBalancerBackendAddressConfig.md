---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 980b16d373f17101266908c0a24443764d96561f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955803"
---
# <span data-ttu-id="97e4e-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="97e4e-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="97e4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="97e4e-103">부하 균형 조정기 백end 주소 구성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="97e4e-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="97e4e-104">구문</span><span class="sxs-lookup"><span data-stu-id="97e4e-104">SYNTAX</span></span>

### <span data-ttu-id="97e4e-105">SetByResourcePublicIpAddress(기본값)</span><span class="sxs-lookup"><span data-stu-id="97e4e-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e4e-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="97e4e-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97e4e-107">설명</span><span class="sxs-lookup"><span data-stu-id="97e4e-107">DESCRIPTION</span></span>
<span data-ttu-id="97e4e-108">부하 균형 조정기 백end 주소 구성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="97e4e-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="97e4e-109">예제</span><span class="sxs-lookup"><span data-stu-id="97e4e-109">EXAMPLES</span></span>

### <span data-ttu-id="97e4e-110">예제 1: 가상 네트워크 참조를 포함한 새 부하 분산기 주소 구성</span><span class="sxs-lookup"><span data-stu-id="97e4e-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="97e4e-111">예제 2: 부하 분산기 프런트 엔드 IP 구성 참조를 포함한 새 부하 분산기 주소 구성</span><span class="sxs-lookup"><span data-stu-id="97e4e-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="97e4e-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="97e4e-112">PARAMETERS</span></span>

### <span data-ttu-id="97e4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e4e-113">-DefaultProfile</span></span>
<span data-ttu-id="97e4e-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97e4e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97e4e-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="97e4e-115">-IpAddress</span></span>
<span data-ttu-id="97e4e-116">백던드 풀에 추가할 IPAddress</span><span class="sxs-lookup"><span data-stu-id="97e4e-116">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e4e-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="97e4e-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="97e4e-118">백 엔드 주소 구성과 연결된 부하 균형 조정기 프런트 엔드 IP 구성</span><span class="sxs-lookup"><span data-stu-id="97e4e-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceFrontendIPConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e4e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="97e4e-119">-Name</span></span>
<span data-ttu-id="97e4e-120">백end 주소 구성의 이름</span><span class="sxs-lookup"><span data-stu-id="97e4e-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="97e4e-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="97e4e-121">-VirtualNetworkId</span></span>
<span data-ttu-id="97e4e-122">백end 주소 구성과 연결된 가상 네트워크</span><span class="sxs-lookup"><span data-stu-id="97e4e-122">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97e4e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="97e4e-123">-Confirm</span></span>
<span data-ttu-id="97e4e-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e4e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97e4e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e4e-125">-WhatIf</span></span>
<span data-ttu-id="97e4e-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="97e4e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97e4e-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="97e4e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97e4e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e4e-128">CommonParameters</span></span>
<span data-ttu-id="97e4e-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="97e4e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e4e-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97e4e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e4e-131">입력</span><span class="sxs-lookup"><span data-stu-id="97e4e-131">INPUTS</span></span>

### <span data-ttu-id="97e4e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="97e4e-132">System.String</span></span>

### <span data-ttu-id="97e4e-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="97e4e-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="97e4e-134">출력</span><span class="sxs-lookup"><span data-stu-id="97e4e-134">OUTPUTS</span></span>

### <span data-ttu-id="97e4e-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="97e4e-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="97e4e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="97e4e-136">NOTES</span></span>

## <span data-ttu-id="97e4e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97e4e-137">RELATED LINKS</span></span>
