---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203934"
---
# <span data-ttu-id="c258d-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c258d-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c258d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c258d-102">SYNOPSIS</span></span>
<span data-ttu-id="c258d-103">부하 분산 장치에 대 한 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c258d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c258d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c258d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c258d-105">DESCRIPTION</span></span>
<span data-ttu-id="c258d-106">**AzLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c258d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c258d-107">EXAMPLES</span></span>

### <span data-ttu-id="c258d-108">예제 1: 부하 분산 장치에서 규칙 구성 제거</span><span class="sxs-lookup"><span data-stu-id="c258d-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="c258d-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="c258d-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에서 MyLBruleName 이라는 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="c258d-111">변수</span><span class="sxs-lookup"><span data-stu-id="c258d-111">PARAMETERS</span></span>

### <span data-ttu-id="c258d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c258d-112">-DefaultProfile</span></span>
<span data-ttu-id="c258d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c258d-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c258d-114">-LoadBalancer</span></span>
<span data-ttu-id="c258d-115">이 cmdlet이 제거 하는 규칙 구성을 포함 하는 **LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c258d-116">-이름</span><span class="sxs-lookup"><span data-stu-id="c258d-116">-Name</span></span>
<span data-ttu-id="c258d-117">이 cmdlet이 제거 하는 부하 분산 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c258d-118">-확인</span><span class="sxs-lookup"><span data-stu-id="c258d-118">-Confirm</span></span>
<span data-ttu-id="c258d-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c258d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c258d-120">-WhatIf</span></span>
<span data-ttu-id="c258d-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c258d-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c258d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c258d-123">CommonParameters</span></span>
<span data-ttu-id="c258d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c258d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c258d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c258d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c258d-126">입력</span><span class="sxs-lookup"><span data-stu-id="c258d-126">INPUTS</span></span>

### <span data-ttu-id="c258d-127">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c258d-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c258d-128">출력</span><span class="sxs-lookup"><span data-stu-id="c258d-128">OUTPUTS</span></span>

### <span data-ttu-id="c258d-129">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c258d-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c258d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="c258d-130">NOTES</span></span>

## <span data-ttu-id="c258d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c258d-131">RELATED LINKS</span></span>

[<span data-ttu-id="c258d-132">추가-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c258d-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c258d-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c258d-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c258d-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c258d-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c258d-135">새로운 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c258d-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c258d-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c258d-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


