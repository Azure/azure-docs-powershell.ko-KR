---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b51c7300296644ffeda75d1fb9e4cf695ff61def
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527815"
---
# <span data-ttu-id="5caba-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5caba-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="5caba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5caba-102">SYNOPSIS</span></span>
<span data-ttu-id="5caba-103">부하 분산 장치에 대 한 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5caba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5caba-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5caba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5caba-105">DESCRIPTION</span></span>
<span data-ttu-id="5caba-106">**AzureRmLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="5caba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5caba-107">EXAMPLES</span></span>

### <span data-ttu-id="5caba-108">예제 1: 부하 분산 장치에서 규칙 구성 제거</span><span class="sxs-lookup"><span data-stu-id="5caba-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="5caba-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="5caba-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에서 MyLBruleName 이라는 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="5caba-111">변수</span><span class="sxs-lookup"><span data-stu-id="5caba-111">PARAMETERS</span></span>

### <span data-ttu-id="5caba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5caba-112">-DefaultProfile</span></span>
<span data-ttu-id="5caba-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5caba-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5caba-114">-LoadBalancer</span></span>
<span data-ttu-id="5caba-115">이 cmdlet이 제거 하는 규칙 구성을 포함 하는 **LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5caba-116">-이름</span><span class="sxs-lookup"><span data-stu-id="5caba-116">-Name</span></span>
<span data-ttu-id="5caba-117">이 cmdlet이 제거 하는 부하 분산 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5caba-118">-확인</span><span class="sxs-lookup"><span data-stu-id="5caba-118">-Confirm</span></span>
<span data-ttu-id="5caba-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5caba-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5caba-120">-WhatIf</span></span>
<span data-ttu-id="5caba-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5caba-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5caba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5caba-123">CommonParameters</span></span>
<span data-ttu-id="5caba-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5caba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5caba-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5caba-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5caba-126">입력</span><span class="sxs-lookup"><span data-stu-id="5caba-126">INPUTS</span></span>

### <span data-ttu-id="5caba-127">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5caba-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="5caba-128">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5caba-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="5caba-129">출력</span><span class="sxs-lookup"><span data-stu-id="5caba-129">OUTPUTS</span></span>

### <span data-ttu-id="5caba-130">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5caba-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5caba-131">상속자</span><span class="sxs-lookup"><span data-stu-id="5caba-131">NOTES</span></span>

## <span data-ttu-id="5caba-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5caba-132">RELATED LINKS</span></span>

[<span data-ttu-id="5caba-133">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5caba-133">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="5caba-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5caba-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="5caba-135">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5caba-135">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="5caba-136">새로운 AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5caba-136">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="5caba-137">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5caba-137">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


