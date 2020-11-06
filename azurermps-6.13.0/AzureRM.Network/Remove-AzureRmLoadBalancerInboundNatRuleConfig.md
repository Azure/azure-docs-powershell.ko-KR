---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d76803df11ff3f89e20ca7d849577ca51331416c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531389"
---
# <span data-ttu-id="dbabf-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dbabf-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="dbabf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbabf-102">SYNOPSIS</span></span>
<span data-ttu-id="dbabf-103">부하 분산 장치에서 인바운드 NAT 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbabf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbabf-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbabf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dbabf-105">DESCRIPTION</span></span>
<span data-ttu-id="dbabf-106">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에서 인바운드 NAT (network address translation) 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="dbabf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dbabf-107">EXAMPLES</span></span>

### <span data-ttu-id="dbabf-108">1: Azure 부하 분산 장치에서 인바운드 NAT 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="dbabf-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="dbabf-109">첫 번째 명령은 이미 "mylb" 라는 기존 부하 분산 장치를 로드 하 여 변수 $load 조정기에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="dbabf-110">두 번째 명령은이 부하 분산 장치에 연결 된 인바운드 NAT 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="dbabf-111">변수</span><span class="sxs-lookup"><span data-stu-id="dbabf-111">PARAMETERS</span></span>

### <span data-ttu-id="dbabf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbabf-112">-DefaultProfile</span></span>
<span data-ttu-id="dbabf-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbabf-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dbabf-114">-LoadBalancer</span></span>
<span data-ttu-id="dbabf-115">이 cmdlet이 제거 하는 인바운드 NAT 규칙 구성을 포함 하는 **LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dbabf-116">-이름</span><span class="sxs-lookup"><span data-stu-id="dbabf-116">-Name</span></span>
<span data-ttu-id="dbabf-117">이 cmdlet이 제거 하는 인바운드 NAT 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dbabf-118">-확인</span><span class="sxs-lookup"><span data-stu-id="dbabf-118">-Confirm</span></span>
<span data-ttu-id="dbabf-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbabf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbabf-120">-WhatIf</span></span>
<span data-ttu-id="dbabf-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbabf-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbabf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbabf-123">CommonParameters</span></span>
<span data-ttu-id="dbabf-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbabf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbabf-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbabf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbabf-126">입력</span><span class="sxs-lookup"><span data-stu-id="dbabf-126">INPUTS</span></span>

### <span data-ttu-id="dbabf-127">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dbabf-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="dbabf-128">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dbabf-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="dbabf-129">출력</span><span class="sxs-lookup"><span data-stu-id="dbabf-129">OUTPUTS</span></span>

### <span data-ttu-id="dbabf-130">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dbabf-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dbabf-131">상속자</span><span class="sxs-lookup"><span data-stu-id="dbabf-131">NOTES</span></span>

## <span data-ttu-id="dbabf-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbabf-132">RELATED LINKS</span></span>

[<span data-ttu-id="dbabf-133">추가-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dbabf-133">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dbabf-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dbabf-134">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dbabf-135">새로운 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dbabf-135">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="dbabf-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dbabf-136">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


