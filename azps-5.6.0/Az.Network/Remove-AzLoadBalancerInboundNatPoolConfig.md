---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9e266ad824d5637137649c73d4e3b427af2f176b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996291"
---
# <span data-ttu-id="b83d6-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b83d6-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b83d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b83d6-102">SYNOPSIS</span></span>
<span data-ttu-id="b83d6-103">부하 균형기에서 인바운드 NAT 풀 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b83d6-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="b83d6-104">구문</span><span class="sxs-lookup"><span data-stu-id="b83d6-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b83d6-105">설명</span><span class="sxs-lookup"><span data-stu-id="b83d6-105">DESCRIPTION</span></span>
<span data-ttu-id="b83d6-106">**Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet은 부하 분산기에서 인바운드 NAT 풀 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b83d6-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="b83d6-107">예제</span><span class="sxs-lookup"><span data-stu-id="b83d6-107">EXAMPLES</span></span>

### <span data-ttu-id="b83d6-108">1: 제거</span><span class="sxs-lookup"><span data-stu-id="b83d6-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="b83d6-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b83d6-109">PARAMETERS</span></span>

### <span data-ttu-id="b83d6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83d6-110">-DefaultProfile</span></span>
<span data-ttu-id="b83d6-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b83d6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b83d6-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b83d6-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="b83d6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b83d6-113">-Name</span></span>
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

### <span data-ttu-id="b83d6-114">-확인</span><span class="sxs-lookup"><span data-stu-id="b83d6-114">-Confirm</span></span>
<span data-ttu-id="b83d6-115">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b83d6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b83d6-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b83d6-116">-WhatIf</span></span>
<span data-ttu-id="b83d6-117">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b83d6-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b83d6-118">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b83d6-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b83d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83d6-119">CommonParameters</span></span>
<span data-ttu-id="b83d6-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b83d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83d6-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b83d6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83d6-122">입력</span><span class="sxs-lookup"><span data-stu-id="b83d6-122">INPUTS</span></span>

### <span data-ttu-id="b83d6-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b83d6-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b83d6-124">출력</span><span class="sxs-lookup"><span data-stu-id="b83d6-124">OUTPUTS</span></span>

### <span data-ttu-id="b83d6-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b83d6-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b83d6-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b83d6-126">NOTES</span></span>

## <span data-ttu-id="b83d6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b83d6-127">RELATED LINKS</span></span>

[<span data-ttu-id="b83d6-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b83d6-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b83d6-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b83d6-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b83d6-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b83d6-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b83d6-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b83d6-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
