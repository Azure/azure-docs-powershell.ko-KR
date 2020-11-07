---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: a5d21e5a34727d0bc13730503d55be6ef604a245
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875567"
---
# <span data-ttu-id="3b653-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3b653-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="3b653-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b653-102">SYNOPSIS</span></span>
<span data-ttu-id="3b653-103">부하 분산 장치에 대 한 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3b653-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="3b653-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b653-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b653-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3b653-105">DESCRIPTION</span></span>
<span data-ttu-id="3b653-106">**AzLoadBalancerRuleConfig** cmdlet은 부하 분산 장치에 대 한 하나 이상의 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3b653-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="3b653-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3b653-107">EXAMPLES</span></span>

### <span data-ttu-id="3b653-108">예제 1: 부하 분산 장치에 대 한 규칙 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="3b653-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="3b653-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b653-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="3b653-110">두 번째 명령은 $slb의 부하 분산 장치에서 MyLBrulename 이라는 연결 된 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3b653-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="3b653-111">변수</span><span class="sxs-lookup"><span data-stu-id="3b653-111">PARAMETERS</span></span>

### <span data-ttu-id="3b653-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b653-112">-DefaultProfile</span></span>
<span data-ttu-id="3b653-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3b653-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b653-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3b653-114">-LoadBalancer</span></span>
<span data-ttu-id="3b653-115">가져올 규칙 구성에 연결 된 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b653-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b653-116">-이름</span><span class="sxs-lookup"><span data-stu-id="3b653-116">-Name</span></span>
<span data-ttu-id="3b653-117">가져올 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b653-117">Specifies the name of the rule configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b653-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b653-118">CommonParameters</span></span>
<span data-ttu-id="3b653-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b653-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b653-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b653-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b653-121">입력</span><span class="sxs-lookup"><span data-stu-id="3b653-121">INPUTS</span></span>

### <span data-ttu-id="3b653-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3b653-122">PSLoadBalancer</span></span>
<span data-ttu-id="3b653-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b653-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="3b653-124">출력</span><span class="sxs-lookup"><span data-stu-id="3b653-124">OUTPUTS</span></span>

### <span data-ttu-id="3b653-125">PSLoadBalancingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="3b653-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="3b653-126">상속자</span><span class="sxs-lookup"><span data-stu-id="3b653-126">NOTES</span></span>

## <span data-ttu-id="3b653-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b653-127">RELATED LINKS</span></span>

[<span data-ttu-id="3b653-128">추가-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3b653-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3b653-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3b653-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="3b653-130">제거-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3b653-130">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="3b653-131">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3b653-131">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


