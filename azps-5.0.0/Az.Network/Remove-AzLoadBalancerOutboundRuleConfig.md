---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218242"
---
# <span data-ttu-id="d5a79-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d5a79-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="d5a79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a79-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a79-103">부하 분산 장치에서 아웃 바운드 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="d5a79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5a79-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a79-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d5a79-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a79-106">**AzLoadBalancerOutboundRuleConfig** Cmdlet은 Azure 부하 분산 장치에서 아웃 바운드 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="d5a79-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d5a79-107">EXAMPLES</span></span>

### <span data-ttu-id="d5a79-108">예제 1: Azure 부하 분산 장치에서 아웃 바운드 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="d5a79-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="d5a79-109">첫 번째 명령은 제거 하려는 아웃 바운드 규칙 구성과 연결 된 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="d5a79-110">두 번째 명령은 연결 된 아웃 바운드 규칙 구성을 부하 분산 장치에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="d5a79-111">세 번째 명령은 부하 분산 장치를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="d5a79-112">변수</span><span class="sxs-lookup"><span data-stu-id="d5a79-112">PARAMETERS</span></span>

### <span data-ttu-id="d5a79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a79-113">-DefaultProfile</span></span>
<span data-ttu-id="d5a79-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5a79-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5a79-115">-LoadBalancer</span></span>
<span data-ttu-id="d5a79-116">부하 분산 장치 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="d5a79-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d5a79-117">-Name</span></span>
<span data-ttu-id="d5a79-118">아웃 바운드 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="d5a79-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="d5a79-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d5a79-119">-Confirm</span></span>
<span data-ttu-id="d5a79-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a79-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a79-121">-WhatIf</span></span>
<span data-ttu-id="d5a79-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a79-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a79-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a79-124">CommonParameters</span></span>
<span data-ttu-id="d5a79-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5a79-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a79-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a79-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a79-127">입력</span><span class="sxs-lookup"><span data-stu-id="d5a79-127">INPUTS</span></span>

### <span data-ttu-id="d5a79-128">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5a79-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d5a79-129">출력</span><span class="sxs-lookup"><span data-stu-id="d5a79-129">OUTPUTS</span></span>

### <span data-ttu-id="d5a79-130">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d5a79-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d5a79-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d5a79-131">NOTES</span></span>

## <span data-ttu-id="d5a79-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5a79-132">RELATED LINKS</span></span>

[<span data-ttu-id="d5a79-133">추가-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d5a79-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d5a79-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d5a79-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d5a79-135">새로운 AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d5a79-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="d5a79-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d5a79-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
