---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 5652615cf8072e4a448f2fe6c6d4b3fd784cc330
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996277"
---
# <span data-ttu-id="87c59-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="87c59-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="87c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87c59-102">SYNOPSIS</span></span>
<span data-ttu-id="87c59-103">부하 저울에서 아웃바운드 규칙 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="87c59-104">구문</span><span class="sxs-lookup"><span data-stu-id="87c59-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87c59-105">설명</span><span class="sxs-lookup"><span data-stu-id="87c59-105">DESCRIPTION</span></span>
<span data-ttu-id="87c59-106">**Remove-AzLoadBalancerOutboundRuleConfig** cmdlet은 Azure 부하 분산기에서 아웃바운드 규칙 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="87c59-107">예제</span><span class="sxs-lookup"><span data-stu-id="87c59-107">EXAMPLES</span></span>

### <span data-ttu-id="87c59-108">예제 1: Azure Load Balancer에서 아웃바운드 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="87c59-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="87c59-109">첫 번째 명령은 제거하려는 아웃바운드 규칙 구성과 연결된 부하 $slb 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="87c59-110">두 번째 명령은 부하 저울에서 연결된 아웃바운드 규칙 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="87c59-111">세 번째 명령은 부하 저울을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="87c59-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="87c59-112">PARAMETERS</span></span>

### <span data-ttu-id="87c59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c59-113">-DefaultProfile</span></span>
<span data-ttu-id="87c59-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87c59-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="87c59-115">-LoadBalancer</span></span>
<span data-ttu-id="87c59-116">부하 균형기 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="87c59-117">-Name</span><span class="sxs-lookup"><span data-stu-id="87c59-117">-Name</span></span>
<span data-ttu-id="87c59-118">아웃바운드 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="87c59-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="87c59-119">-확인</span><span class="sxs-lookup"><span data-stu-id="87c59-119">-Confirm</span></span>
<span data-ttu-id="87c59-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87c59-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c59-121">-WhatIf</span></span>
<span data-ttu-id="87c59-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87c59-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87c59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c59-124">CommonParameters</span></span>
<span data-ttu-id="87c59-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="87c59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c59-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="87c59-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c59-127">입력</span><span class="sxs-lookup"><span data-stu-id="87c59-127">INPUTS</span></span>

### <span data-ttu-id="87c59-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="87c59-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="87c59-129">출력</span><span class="sxs-lookup"><span data-stu-id="87c59-129">OUTPUTS</span></span>

### <span data-ttu-id="87c59-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="87c59-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="87c59-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="87c59-131">NOTES</span></span>

## <span data-ttu-id="87c59-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87c59-132">RELATED LINKS</span></span>

[<span data-ttu-id="87c59-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="87c59-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="87c59-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="87c59-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="87c59-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="87c59-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="87c59-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="87c59-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
