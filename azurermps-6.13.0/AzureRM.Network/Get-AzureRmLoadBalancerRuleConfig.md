---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b09aeb7288f69d0edc678578bbcc91306f5b0c2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538000"
---
# <span data-ttu-id="48404-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48404-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="48404-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48404-102">SYNOPSIS</span></span>
<span data-ttu-id="48404-103">부하 분산 장치에 대 한 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="48404-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48404-104">구문과</span><span class="sxs-lookup"><span data-stu-id="48404-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48404-105">설명은</span><span class="sxs-lookup"><span data-stu-id="48404-105">DESCRIPTION</span></span>
<span data-ttu-id="48404-106">**AzureRmLoadBalancerRuleConfig** cmdlet은 부하 분산 장치에 대 한 하나 이상의 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="48404-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="48404-107">예제의</span><span class="sxs-lookup"><span data-stu-id="48404-107">EXAMPLES</span></span>

### <span data-ttu-id="48404-108">예제 1: 부하 분산 장치에 대 한 규칙 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="48404-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="48404-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="48404-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="48404-110">두 번째 명령은 $slb의 부하 분산 장치에서 MyLBrulename 이라는 연결 된 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="48404-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="48404-111">변수</span><span class="sxs-lookup"><span data-stu-id="48404-111">PARAMETERS</span></span>

### <span data-ttu-id="48404-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48404-112">-DefaultProfile</span></span>
<span data-ttu-id="48404-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48404-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48404-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48404-114">-LoadBalancer</span></span>
<span data-ttu-id="48404-115">가져올 규칙 구성에 연결 된 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48404-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="48404-116">-이름</span><span class="sxs-lookup"><span data-stu-id="48404-116">-Name</span></span>
<span data-ttu-id="48404-117">가져올 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48404-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="48404-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48404-118">CommonParameters</span></span>
<span data-ttu-id="48404-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48404-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48404-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48404-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48404-121">입력</span><span class="sxs-lookup"><span data-stu-id="48404-121">INPUTS</span></span>

### <span data-ttu-id="48404-122">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48404-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="48404-123">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48404-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="48404-124">출력</span><span class="sxs-lookup"><span data-stu-id="48404-124">OUTPUTS</span></span>

### <span data-ttu-id="48404-125">PSLoadBalancingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="48404-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="48404-126">상속자</span><span class="sxs-lookup"><span data-stu-id="48404-126">NOTES</span></span>

## <span data-ttu-id="48404-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48404-127">RELATED LINKS</span></span>

[<span data-ttu-id="48404-128">추가-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48404-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="48404-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="48404-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="48404-130">제거-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48404-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="48404-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48404-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


