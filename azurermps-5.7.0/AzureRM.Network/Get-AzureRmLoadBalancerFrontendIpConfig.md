---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: f6de3902770fd799f8ce5a41d5aa1230e6821f02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526780"
---
# <span data-ttu-id="63fda-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="63fda-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="63fda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63fda-102">SYNOPSIS</span></span>
<span data-ttu-id="63fda-103">부하 분산 장치에서 프런트 엔드 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63fda-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63fda-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63fda-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63fda-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63fda-105">DESCRIPTION</span></span>
<span data-ttu-id="63fda-106">**AzureRmLoadBalancerFrontendIpConfig** cmdlet은 부하 분산 장치에서 프런트 엔드 ip 구성 또는 프런트 엔드 ip 구성 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63fda-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="63fda-107">예제의</span><span class="sxs-lookup"><span data-stu-id="63fda-107">EXAMPLES</span></span>

### <span data-ttu-id="63fda-108">예제 1: 부하 분산 장치에서 프런트 엔드 IP 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="63fda-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="63fda-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음이를 변수 $slb에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fda-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="63fda-110">두 번째 명령은 해당 부하 분산 장치에 연결 된 프런트 엔드 IP 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63fda-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="63fda-111">변수</span><span class="sxs-lookup"><span data-stu-id="63fda-111">PARAMETERS</span></span>

### <span data-ttu-id="63fda-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fda-112">-DefaultProfile</span></span>
<span data-ttu-id="63fda-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63fda-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63fda-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63fda-114">-LoadBalancer</span></span>
<span data-ttu-id="63fda-115">가져올 프런트 엔드 IP 구성에 연결 된 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fda-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="63fda-116">-이름</span><span class="sxs-lookup"><span data-stu-id="63fda-116">-Name</span></span>
<span data-ttu-id="63fda-117">가져올 프런트 엔드 IP 구성을 포함 하는 부하 분산 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fda-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="63fda-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fda-118">CommonParameters</span></span>
<span data-ttu-id="63fda-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fda-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fda-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63fda-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fda-121">입력</span><span class="sxs-lookup"><span data-stu-id="63fda-121">INPUTS</span></span>

### <span data-ttu-id="63fda-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63fda-122">PSLoadBalancer</span></span>
<span data-ttu-id="63fda-123">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fda-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="63fda-124">출력</span><span class="sxs-lookup"><span data-stu-id="63fda-124">OUTPUTS</span></span>

### <span data-ttu-id="63fda-125">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="63fda-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="63fda-126">상속자</span><span class="sxs-lookup"><span data-stu-id="63fda-126">NOTES</span></span>

## <span data-ttu-id="63fda-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63fda-127">RELATED LINKS</span></span>

[<span data-ttu-id="63fda-128">추가-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="63fda-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="63fda-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63fda-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="63fda-130">새로운 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="63fda-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="63fda-131">제거-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="63fda-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="63fda-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="63fda-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


