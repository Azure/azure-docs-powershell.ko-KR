---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186948"
---
# <span data-ttu-id="cae43-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cae43-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="cae43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cae43-102">SYNOPSIS</span></span>
<span data-ttu-id="cae43-103">부하 균형 조정에 대한 규칙 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cae43-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="cae43-104">구문</span><span class="sxs-lookup"><span data-stu-id="cae43-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae43-105">설명</span><span class="sxs-lookup"><span data-stu-id="cae43-105">DESCRIPTION</span></span>
<span data-ttu-id="cae43-106">**Remove-AzLoadBalancerRuleConfig** cmdlet은 Azure Load Balancer에 대한 규칙 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cae43-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="cae43-107">예제</span><span class="sxs-lookup"><span data-stu-id="cae43-107">EXAMPLES</span></span>

### <span data-ttu-id="cae43-108">예제 1: 부하 균형 조정기에서 규칙 구성 제거</span><span class="sxs-lookup"><span data-stu-id="cae43-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="cae43-109">첫 번째 명령은 MyLoadBalancer라는 부하 분산 $loadbalancer 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="cae43-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="cae43-110">두 번째 명령은 MyLBruleName이라는 규칙 구성을 해당 명령의 부하 $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="cae43-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="cae43-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cae43-111">PARAMETERS</span></span>

### <span data-ttu-id="cae43-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae43-112">-DefaultProfile</span></span>
<span data-ttu-id="cae43-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cae43-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cae43-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cae43-114">-LoadBalancer</span></span>
<span data-ttu-id="cae43-115">이 cmdlet에서 제거하는 규칙 구성을 포함하는 **LoadBalancer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cae43-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cae43-116">-Name</span><span class="sxs-lookup"><span data-stu-id="cae43-116">-Name</span></span>
<span data-ttu-id="cae43-117">이 cmdlet이 제거하는 부하 균형 조정기 규칙 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cae43-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cae43-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cae43-118">-Confirm</span></span>
<span data-ttu-id="cae43-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cae43-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae43-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae43-120">-WhatIf</span></span>
<span data-ttu-id="cae43-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cae43-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cae43-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cae43-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae43-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae43-123">CommonParameters</span></span>
<span data-ttu-id="cae43-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cae43-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae43-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cae43-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae43-126">입력</span><span class="sxs-lookup"><span data-stu-id="cae43-126">INPUTS</span></span>

### <span data-ttu-id="cae43-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cae43-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cae43-128">출력</span><span class="sxs-lookup"><span data-stu-id="cae43-128">OUTPUTS</span></span>

### <span data-ttu-id="cae43-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cae43-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cae43-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cae43-130">NOTES</span></span>

## <span data-ttu-id="cae43-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cae43-131">RELATED LINKS</span></span>

[<span data-ttu-id="cae43-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cae43-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="cae43-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cae43-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="cae43-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cae43-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="cae43-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cae43-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="cae43-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cae43-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


