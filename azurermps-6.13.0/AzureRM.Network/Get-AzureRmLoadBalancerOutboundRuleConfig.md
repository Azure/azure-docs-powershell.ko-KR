---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1bcaab526ac2fbb82d696db7197bbc8d69c0078f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711818"
---
# <span data-ttu-id="b316b-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b316b-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="b316b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b316b-102">SYNOPSIS</span></span>
<span data-ttu-id="b316b-103">부하 분산 장치에서 아웃 바운드 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b316b-103">Gets an outbound rule configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b316b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b316b-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b316b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b316b-105">DESCRIPTION</span></span>
<span data-ttu-id="b316b-106">**AzureRmLoadBalancerOutboundRuleConfig** cmdlet은 아웃 바운드 규칙 구성 또는 부하 분산 장치에 대 한 아웃 바운드 규칙 구성 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b316b-106">The **Get-AzureRmLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="b316b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b316b-107">EXAMPLES</span></span>

### <span data-ttu-id="b316b-108">예제 1: 부하 분산 장치에서 아웃 바운드 규칙 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b316b-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="b316b-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b316b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b316b-110">두 번째 명령은 해당 부하 분산 장치에 연결 된 MyRule 이라는 아웃 바운드 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b316b-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="b316b-111">변수</span><span class="sxs-lookup"><span data-stu-id="b316b-111">PARAMETERS</span></span>

### <span data-ttu-id="b316b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b316b-112">-DefaultProfile</span></span>
<span data-ttu-id="b316b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b316b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b316b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b316b-114">-LoadBalancer</span></span>
<span data-ttu-id="b316b-115">부하 분산 장치 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="b316b-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="b316b-116">-이름</span><span class="sxs-lookup"><span data-stu-id="b316b-116">-Name</span></span>
<span data-ttu-id="b316b-117">아웃 바운드 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b316b-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="b316b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b316b-118">CommonParameters</span></span>
<span data-ttu-id="b316b-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b316b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b316b-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b316b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b316b-121">입력</span><span class="sxs-lookup"><span data-stu-id="b316b-121">INPUTS</span></span>

### <span data-ttu-id="b316b-122">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b316b-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b316b-123">출력</span><span class="sxs-lookup"><span data-stu-id="b316b-123">OUTPUTS</span></span>

### <span data-ttu-id="b316b-124">PSOutboundRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b316b-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="b316b-125">상속자</span><span class="sxs-lookup"><span data-stu-id="b316b-125">NOTES</span></span>

## <span data-ttu-id="b316b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b316b-126">RELATED LINKS</span></span>
