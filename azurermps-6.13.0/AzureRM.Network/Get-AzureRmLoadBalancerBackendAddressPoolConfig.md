---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2a9fca5faf7ba024a5d5c891aa1c74ba002ac053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530213"
---
# <span data-ttu-id="87031-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="87031-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="87031-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87031-102">SYNOPSIS</span></span>
<span data-ttu-id="87031-103">부하 분산 장치에 대 한 백 엔드 주소 풀 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87031-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87031-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87031-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87031-105">설명은</span><span class="sxs-lookup"><span data-stu-id="87031-105">DESCRIPTION</span></span>
<span data-ttu-id="87031-106">**AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet은 단일 백엔드 주소 풀 또는 부하 분산 장치 내의 백엔드 주소 풀 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87031-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="87031-107">예제의</span><span class="sxs-lookup"><span data-stu-id="87031-107">EXAMPLES</span></span>

### <span data-ttu-id="87031-108">예제 1: 백 엔드 주소 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="87031-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="87031-109">첫 번째 명령은 Myloadbalancer 이라는 리소스 그룹에서 MyLoadBalancer 라는 기존 부하 분산 장치를 가져온 다음이를 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="87031-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="87031-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에 대 한 BackendAddressPool02 이라는 관련 백엔드 주소 풀 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87031-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="87031-111">변수</span><span class="sxs-lookup"><span data-stu-id="87031-111">PARAMETERS</span></span>

### <span data-ttu-id="87031-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87031-112">-DefaultProfile</span></span>
<span data-ttu-id="87031-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87031-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87031-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="87031-114">-LoadBalancer</span></span>
<span data-ttu-id="87031-115">가져올 백 엔드 주소 풀과 연결 된 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87031-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="87031-116">-이름</span><span class="sxs-lookup"><span data-stu-id="87031-116">-Name</span></span>
<span data-ttu-id="87031-117">가져올 백 엔드 주소 풀이 포함 된 부하 분산 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87031-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="87031-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87031-118">CommonParameters</span></span>
<span data-ttu-id="87031-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87031-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87031-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87031-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87031-121">입력</span><span class="sxs-lookup"><span data-stu-id="87031-121">INPUTS</span></span>

### <span data-ttu-id="87031-122">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="87031-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="87031-123">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="87031-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="87031-124">출력</span><span class="sxs-lookup"><span data-stu-id="87031-124">OUTPUTS</span></span>

### <span data-ttu-id="87031-125">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="87031-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="87031-126">상속자</span><span class="sxs-lookup"><span data-stu-id="87031-126">NOTES</span></span>

## <span data-ttu-id="87031-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87031-127">RELATED LINKS</span></span>

[<span data-ttu-id="87031-128">추가-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="87031-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="87031-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="87031-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="87031-130">새로운 AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="87031-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="87031-131">제거-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="87031-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


