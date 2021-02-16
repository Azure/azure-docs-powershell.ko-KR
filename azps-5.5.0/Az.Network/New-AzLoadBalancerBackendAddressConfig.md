---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179668"
---
# <span data-ttu-id="dfc44-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="dfc44-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="dfc44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfc44-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc44-103">부하 균형 조정기 백end 주소 구성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc44-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="dfc44-104">구문</span><span class="sxs-lookup"><span data-stu-id="dfc44-104">SYNTAX</span></span>

### <span data-ttu-id="dfc44-105">SetByResourcePublicIpAddress(기본값)</span><span class="sxs-lookup"><span data-stu-id="dfc44-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfc44-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfc44-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfc44-107">설명</span><span class="sxs-lookup"><span data-stu-id="dfc44-107">DESCRIPTION</span></span>
<span data-ttu-id="dfc44-108">부하 균형 조정기 백end 주소 구성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc44-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="dfc44-109">예제</span><span class="sxs-lookup"><span data-stu-id="dfc44-109">EXAMPLES</span></span>

### <span data-ttu-id="dfc44-110">예제 1: 가상 네트워크 참조를 포함한 새 부하 분산기 주소 구성</span><span class="sxs-lookup"><span data-stu-id="dfc44-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="dfc44-111">예제 2: 부하 분산기 프런트 엔드 IP 구성 참조를 포함한 새 부하 분산기 주소 구성</span><span class="sxs-lookup"><span data-stu-id="dfc44-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="dfc44-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfc44-112">PARAMETERS</span></span>

### <span data-ttu-id="dfc44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc44-113">-DefaultProfile</span></span>
<span data-ttu-id="dfc44-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfc44-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfc44-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="dfc44-115">-IpAddress</span></span>
<span data-ttu-id="dfc44-116">백end 풀에 추가할 IPAddress</span><span class="sxs-lookup"><span data-stu-id="dfc44-116">The IPAddress to add to the backend pool</span></span>

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

### <span data-ttu-id="dfc44-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="dfc44-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="dfc44-118">백 엔드 주소 구성과 연결된 부하 균형 조정기 프런트 엔드 IP 구성</span><span class="sxs-lookup"><span data-stu-id="dfc44-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

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

### <span data-ttu-id="dfc44-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dfc44-119">-Name</span></span>
<span data-ttu-id="dfc44-120">백end 주소 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfc44-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="dfc44-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="dfc44-121">-VirtualNetworkId</span></span>
<span data-ttu-id="dfc44-122">백end 주소 구성과 연결된 가상 네트워크</span><span class="sxs-lookup"><span data-stu-id="dfc44-122">The virtual network associated with Backend Address config</span></span>

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

### <span data-ttu-id="dfc44-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfc44-123">-Confirm</span></span>
<span data-ttu-id="dfc44-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfc44-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfc44-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfc44-125">-WhatIf</span></span>
<span data-ttu-id="dfc44-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dfc44-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfc44-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfc44-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfc44-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc44-128">CommonParameters</span></span>
<span data-ttu-id="dfc44-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dfc44-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc44-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dfc44-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc44-131">입력</span><span class="sxs-lookup"><span data-stu-id="dfc44-131">INPUTS</span></span>

### <span data-ttu-id="dfc44-132">System.String</span><span class="sxs-lookup"><span data-stu-id="dfc44-132">System.String</span></span>

### <span data-ttu-id="dfc44-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dfc44-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="dfc44-134">출력</span><span class="sxs-lookup"><span data-stu-id="dfc44-134">OUTPUTS</span></span>

### <span data-ttu-id="dfc44-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="dfc44-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="dfc44-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dfc44-136">NOTES</span></span>

## <span data-ttu-id="dfc44-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfc44-137">RELATED LINKS</span></span>
