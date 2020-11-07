---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: a9a76af9eaee36913fd22c8003d6f4b9ba8c7b77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700161"
---
# <span data-ttu-id="07f4e-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="07f4e-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="07f4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="07f4e-103">부하 분산 장치에서 인바운드 NAT 풀 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4e-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="07f4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07f4e-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f4e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07f4e-105">DESCRIPTION</span></span>
<span data-ttu-id="07f4e-106">**AzLoadBalancerInboundNatPoolConfig** cmdlet은 부하 분산 장치에서 인바운드 NAT 풀 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4e-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="07f4e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="07f4e-107">EXAMPLES</span></span>

### <span data-ttu-id="07f4e-108">1: 제거</span><span class="sxs-lookup"><span data-stu-id="07f4e-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="07f4e-109">변수</span><span class="sxs-lookup"><span data-stu-id="07f4e-109">PARAMETERS</span></span>

### <span data-ttu-id="07f4e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f4e-110">-DefaultProfile</span></span>
<span data-ttu-id="07f4e-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07f4e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07f4e-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07f4e-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="07f4e-113">-이름</span><span class="sxs-lookup"><span data-stu-id="07f4e-113">-Name</span></span>
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

### <span data-ttu-id="07f4e-114">-확인</span><span class="sxs-lookup"><span data-stu-id="07f4e-114">-Confirm</span></span>
<span data-ttu-id="07f4e-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f4e-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f4e-116">-WhatIf</span></span>
<span data-ttu-id="07f4e-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07f4e-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07f4e-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f4e-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f4e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f4e-119">CommonParameters</span></span>
<span data-ttu-id="07f4e-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f4e-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f4e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f4e-122">입력</span><span class="sxs-lookup"><span data-stu-id="07f4e-122">INPUTS</span></span>

### <span data-ttu-id="07f4e-123">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07f4e-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="07f4e-124">출력</span><span class="sxs-lookup"><span data-stu-id="07f4e-124">OUTPUTS</span></span>

### <span data-ttu-id="07f4e-125">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07f4e-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="07f4e-126">상속자</span><span class="sxs-lookup"><span data-stu-id="07f4e-126">NOTES</span></span>

## <span data-ttu-id="07f4e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07f4e-127">RELATED LINKS</span></span>

[<span data-ttu-id="07f4e-128">추가-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="07f4e-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="07f4e-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="07f4e-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="07f4e-130">새로운 AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="07f4e-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="07f4e-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="07f4e-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
