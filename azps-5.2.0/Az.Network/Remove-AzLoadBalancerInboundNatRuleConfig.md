---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 76cf9e2624c812d99702823b303e4e6427845670
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342698"
---
# <span data-ttu-id="ca6aa-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca6aa-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ca6aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca6aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6aa-103">부하 균형 조정기에서 인바운드 NAT 규칙 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="ca6aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca6aa-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca6aa-105">설명</span><span class="sxs-lookup"><span data-stu-id="ca6aa-105">DESCRIPTION</span></span>
<span data-ttu-id="ca6aa-106">**Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet은 Azure Load Balancer에서 인바운드 NAT(네트워크 주소 변환) 규칙 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="ca6aa-107">예제</span><span class="sxs-lookup"><span data-stu-id="ca6aa-107">EXAMPLES</span></span>

### <span data-ttu-id="ca6aa-108">1: Azure Load Balancer에서 인바운드 NAT 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="ca6aa-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="ca6aa-109">첫 번째 명령은 "mylb"라는 기존 부하를 로드하고 부하 $load 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="ca6aa-110">두 번째 명령은 이 부하 균형 조정과 연결된 인바운드 NAT 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="ca6aa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca6aa-111">PARAMETERS</span></span>

### <span data-ttu-id="ca6aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6aa-112">-DefaultProfile</span></span>
<span data-ttu-id="ca6aa-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca6aa-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ca6aa-114">-LoadBalancer</span></span>
<span data-ttu-id="ca6aa-115">이 cmdlet에서 제거하는 인바운드 NAT 규칙 구성을 포함하는 **LoadBalancer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ca6aa-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ca6aa-116">-Name</span></span>
<span data-ttu-id="ca6aa-117">이 cmdlet에서 제거하는 인바운드 NAT 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ca6aa-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca6aa-118">-Confirm</span></span>
<span data-ttu-id="ca6aa-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca6aa-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca6aa-120">-WhatIf</span></span>
<span data-ttu-id="ca6aa-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ca6aa-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca6aa-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca6aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6aa-123">CommonParameters</span></span>
<span data-ttu-id="ca6aa-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6aa-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca6aa-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6aa-126">입력</span><span class="sxs-lookup"><span data-stu-id="ca6aa-126">INPUTS</span></span>

### <span data-ttu-id="ca6aa-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ca6aa-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ca6aa-128">출력</span><span class="sxs-lookup"><span data-stu-id="ca6aa-128">OUTPUTS</span></span>

### <span data-ttu-id="ca6aa-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ca6aa-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ca6aa-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca6aa-130">NOTES</span></span>

## <span data-ttu-id="ca6aa-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca6aa-131">RELATED LINKS</span></span>

[<span data-ttu-id="ca6aa-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca6aa-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ca6aa-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca6aa-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ca6aa-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca6aa-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ca6aa-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ca6aa-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


