---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875327"
---
# <span data-ttu-id="213e9-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="213e9-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="213e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="213e9-102">SYNOPSIS</span></span>
<span data-ttu-id="213e9-103">부하 분산 장치에 대 한 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="213e9-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="213e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="213e9-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="213e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="213e9-105">DESCRIPTION</span></span>
<span data-ttu-id="213e9-106">**AzLoadBalancerRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="213e9-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="213e9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="213e9-107">EXAMPLES</span></span>

### <span data-ttu-id="213e9-108">예제 1: 부하 분산 장치에서 규칙 구성 제거</span><span class="sxs-lookup"><span data-stu-id="213e9-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="213e9-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="213e9-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="213e9-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에서 MyLBruleName 이라는 규칙 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="213e9-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="213e9-111">변수</span><span class="sxs-lookup"><span data-stu-id="213e9-111">PARAMETERS</span></span>

### <span data-ttu-id="213e9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213e9-112">-DefaultProfile</span></span>
<span data-ttu-id="213e9-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="213e9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="213e9-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="213e9-114">-LoadBalancer</span></span>
<span data-ttu-id="213e9-115">이 cmdlet이 제거 하는 규칙 구성을 포함 하는 **LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213e9-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="213e9-116">-이름</span><span class="sxs-lookup"><span data-stu-id="213e9-116">-Name</span></span>
<span data-ttu-id="213e9-117">이 cmdlet이 제거 하는 부하 분산 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="213e9-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="213e9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213e9-118">CommonParameters</span></span>
<span data-ttu-id="213e9-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="213e9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213e9-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="213e9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213e9-121">입력</span><span class="sxs-lookup"><span data-stu-id="213e9-121">INPUTS</span></span>

### <span data-ttu-id="213e9-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="213e9-122">PSLoadBalancer</span></span>
<span data-ttu-id="213e9-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="213e9-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="213e9-124">출력</span><span class="sxs-lookup"><span data-stu-id="213e9-124">OUTPUTS</span></span>

### <span data-ttu-id="213e9-125">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="213e9-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="213e9-126">상속자</span><span class="sxs-lookup"><span data-stu-id="213e9-126">NOTES</span></span>

## <span data-ttu-id="213e9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="213e9-127">RELATED LINKS</span></span>

[<span data-ttu-id="213e9-128">추가-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="213e9-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="213e9-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="213e9-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="213e9-130">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="213e9-130">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="213e9-131">새로운 AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="213e9-131">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="213e9-132">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="213e9-132">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


