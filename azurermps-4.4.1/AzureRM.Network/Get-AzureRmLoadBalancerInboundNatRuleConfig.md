---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 71c093573f4384884702c72e586c36bbdb9b4066
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532232"
---
# <span data-ttu-id="d3c70-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3c70-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d3c70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3c70-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c70-103">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c70-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3c70-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3c70-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3c70-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3c70-105">DESCRIPTION</span></span>
<span data-ttu-id="d3c70-106">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에서 하나 이상의 인바운드 NAT (network address translation) 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c70-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="d3c70-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d3c70-107">EXAMPLES</span></span>

### <span data-ttu-id="d3c70-108">예제 1: 인바운드 NAT 규칙 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3c70-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="d3c70-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져오고이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c70-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="d3c70-110">두 번째 명령은 $slb의 부하 분산 장치에서 MyInboundNatRule1 라는 연결 된 NAT 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3c70-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="d3c70-111">변수</span><span class="sxs-lookup"><span data-stu-id="d3c70-111">PARAMETERS</span></span>

### <span data-ttu-id="d3c70-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3c70-112">-LoadBalancer</span></span>
<span data-ttu-id="d3c70-113">가져올 인바운드 NAT 규칙 구성과 연결 된 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c70-113">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c70-114">-이름</span><span class="sxs-lookup"><span data-stu-id="d3c70-114">-Name</span></span>
<span data-ttu-id="d3c70-115">가져올 인바운드 NAT 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c70-115">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="d3c70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c70-116">-DefaultProfile</span></span>
<span data-ttu-id="d3c70-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3c70-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3c70-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c70-118">CommonParameters</span></span>
<span data-ttu-id="d3c70-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c70-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c70-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c70-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c70-121">입력</span><span class="sxs-lookup"><span data-stu-id="d3c70-121">INPUTS</span></span>

### <span data-ttu-id="d3c70-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3c70-122">PSLoadBalancer</span></span>
<span data-ttu-id="d3c70-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3c70-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d3c70-124">출력</span><span class="sxs-lookup"><span data-stu-id="d3c70-124">OUTPUTS</span></span>

### <span data-ttu-id="d3c70-125">PSInboundNatRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d3c70-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="d3c70-126">상속자</span><span class="sxs-lookup"><span data-stu-id="d3c70-126">NOTES</span></span>

## <span data-ttu-id="d3c70-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3c70-127">RELATED LINKS</span></span>

[<span data-ttu-id="d3c70-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3c70-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d3c70-129">새로운 AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3c70-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d3c70-130">제거-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3c70-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d3c70-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3c70-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


