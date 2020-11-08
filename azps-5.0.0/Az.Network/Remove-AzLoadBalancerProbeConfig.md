---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218108"
---
# <span data-ttu-id="30260-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="30260-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="30260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30260-102">SYNOPSIS</span></span>
<span data-ttu-id="30260-103">부하 분산 장치에서 프로브 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="30260-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="30260-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30260-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30260-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30260-105">DESCRIPTION</span></span>
<span data-ttu-id="30260-106">**AzLoadBalancerProbeConfig** cmdlet은 부하 분산 장치에서 프로브 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="30260-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="30260-107">예제의</span><span class="sxs-lookup"><span data-stu-id="30260-107">EXAMPLES</span></span>

### <span data-ttu-id="30260-108">예제 1: 부하 분산 장치에서 프로브 구성 제거</span><span class="sxs-lookup"><span data-stu-id="30260-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="30260-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="30260-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="30260-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에서 MyProbe 구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="30260-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="30260-111">변수</span><span class="sxs-lookup"><span data-stu-id="30260-111">PARAMETERS</span></span>

### <span data-ttu-id="30260-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30260-112">-DefaultProfile</span></span>
<span data-ttu-id="30260-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30260-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30260-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30260-114">-LoadBalancer</span></span>
<span data-ttu-id="30260-115">이 cmdlet이 제거 하는 프로브 구성을 포함 하는 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30260-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="30260-116">-이름</span><span class="sxs-lookup"><span data-stu-id="30260-116">-Name</span></span>
<span data-ttu-id="30260-117">이 cmdlet이 제거 하는 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30260-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="30260-118">-확인</span><span class="sxs-lookup"><span data-stu-id="30260-118">-Confirm</span></span>
<span data-ttu-id="30260-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30260-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30260-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30260-120">-WhatIf</span></span>
<span data-ttu-id="30260-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30260-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30260-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30260-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30260-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30260-123">CommonParameters</span></span>
<span data-ttu-id="30260-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30260-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30260-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30260-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30260-126">입력</span><span class="sxs-lookup"><span data-stu-id="30260-126">INPUTS</span></span>

### <span data-ttu-id="30260-127">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30260-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="30260-128">출력</span><span class="sxs-lookup"><span data-stu-id="30260-128">OUTPUTS</span></span>

### <span data-ttu-id="30260-129">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30260-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="30260-130">상속자</span><span class="sxs-lookup"><span data-stu-id="30260-130">NOTES</span></span>

## <span data-ttu-id="30260-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30260-131">RELATED LINKS</span></span>

[<span data-ttu-id="30260-132">추가-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="30260-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="30260-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30260-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="30260-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="30260-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="30260-135">새로운 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="30260-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="30260-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="30260-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


