---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 32e22416a6e624af293ffcc0597203d8b24351a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700550"
---
# <span data-ttu-id="e874a-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e874a-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="e874a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e874a-102">SYNOPSIS</span></span>
<span data-ttu-id="e874a-103">부하 분산 장치에서 아웃 바운드 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e874a-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="e874a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e874a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e874a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e874a-105">DESCRIPTION</span></span>
<span data-ttu-id="e874a-106">**AzLoadBalancerOutboundRuleConfig** cmdlet은 아웃 바운드 규칙 구성 또는 부하 분산 장치에 대 한 아웃 바운드 규칙 구성 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e874a-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="e874a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e874a-107">EXAMPLES</span></span>

### <span data-ttu-id="e874a-108">예제 1: 부하 분산 장치에서 아웃 바운드 규칙 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="e874a-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="e874a-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e874a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e874a-110">두 번째 명령은 해당 부하 분산 장치에 연결 된 MyRule 이라는 아웃 바운드 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e874a-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="e874a-111">변수</span><span class="sxs-lookup"><span data-stu-id="e874a-111">PARAMETERS</span></span>

### <span data-ttu-id="e874a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e874a-112">-DefaultProfile</span></span>
<span data-ttu-id="e874a-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e874a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e874a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e874a-114">-LoadBalancer</span></span>
<span data-ttu-id="e874a-115">부하 분산 장치 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="e874a-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="e874a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="e874a-116">-Name</span></span>
<span data-ttu-id="e874a-117">아웃 바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e874a-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="e874a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e874a-118">CommonParameters</span></span>
<span data-ttu-id="e874a-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e874a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e874a-120">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e874a-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e874a-121">입력</span><span class="sxs-lookup"><span data-stu-id="e874a-121">INPUTS</span></span>

### <span data-ttu-id="e874a-122">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e874a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e874a-123">출력</span><span class="sxs-lookup"><span data-stu-id="e874a-123">OUTPUTS</span></span>

### <span data-ttu-id="e874a-124">PSOutboundRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e874a-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="e874a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="e874a-125">NOTES</span></span>

## <span data-ttu-id="e874a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e874a-126">RELATED LINKS</span></span>

[<span data-ttu-id="e874a-127">추가-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e874a-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="e874a-128">새로운 AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e874a-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="e874a-129">제거-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e874a-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="e874a-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e874a-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
