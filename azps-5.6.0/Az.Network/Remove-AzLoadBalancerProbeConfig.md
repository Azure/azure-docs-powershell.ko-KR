---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 3e7433c8c779c078ab1b264e6b724d06cd884bab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993664"
---
# <span data-ttu-id="91f95-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="91f95-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="91f95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91f95-102">SYNOPSIS</span></span>
<span data-ttu-id="91f95-103">부하 균형 조정기에서 프로브 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="91f95-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="91f95-104">구문</span><span class="sxs-lookup"><span data-stu-id="91f95-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91f95-105">설명</span><span class="sxs-lookup"><span data-stu-id="91f95-105">DESCRIPTION</span></span>
<span data-ttu-id="91f95-106">**Remove-AzLoadBalancerProbeConfig** cmdlet은 부하 분산기에서 프로브 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="91f95-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="91f95-107">예제</span><span class="sxs-lookup"><span data-stu-id="91f95-107">EXAMPLES</span></span>

### <span data-ttu-id="91f95-108">예제 1: 부하 저울에서 프로브 구성 제거</span><span class="sxs-lookup"><span data-stu-id="91f95-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="91f95-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산 $loadbalancer 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="91f95-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="91f95-110">두 번째 명령은 에 있는 부하 균형 장치에서 MyProbe라는 구성을 $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="91f95-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="91f95-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="91f95-111">PARAMETERS</span></span>

### <span data-ttu-id="91f95-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f95-112">-DefaultProfile</span></span>
<span data-ttu-id="91f95-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91f95-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91f95-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="91f95-114">-LoadBalancer</span></span>
<span data-ttu-id="91f95-115">이 cmdlet이 제거하는 프로브 구성을 포함하는 부하 균형 조정기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91f95-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="91f95-116">-Name</span><span class="sxs-lookup"><span data-stu-id="91f95-116">-Name</span></span>
<span data-ttu-id="91f95-117">이 cmdlet이 제거하는 프로브 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91f95-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f95-118">-확인</span><span class="sxs-lookup"><span data-stu-id="91f95-118">-Confirm</span></span>
<span data-ttu-id="91f95-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="91f95-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f95-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f95-120">-WhatIf</span></span>
<span data-ttu-id="91f95-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="91f95-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91f95-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91f95-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f95-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f95-123">CommonParameters</span></span>
<span data-ttu-id="91f95-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91f95-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f95-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="91f95-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f95-126">입력</span><span class="sxs-lookup"><span data-stu-id="91f95-126">INPUTS</span></span>

### <span data-ttu-id="91f95-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="91f95-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="91f95-128">출력</span><span class="sxs-lookup"><span data-stu-id="91f95-128">OUTPUTS</span></span>

### <span data-ttu-id="91f95-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="91f95-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="91f95-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91f95-130">NOTES</span></span>

## <span data-ttu-id="91f95-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91f95-131">RELATED LINKS</span></span>

[<span data-ttu-id="91f95-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="91f95-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="91f95-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="91f95-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="91f95-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="91f95-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="91f95-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="91f95-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="91f95-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="91f95-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


