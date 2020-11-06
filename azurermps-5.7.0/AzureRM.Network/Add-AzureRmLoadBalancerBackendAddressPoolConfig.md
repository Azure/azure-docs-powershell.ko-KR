---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 82775229bc368f80c03a886b10a631a4482341df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530466"
---
# <span data-ttu-id="f2edf-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f2edf-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f2edf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2edf-102">SYNOPSIS</span></span>
<span data-ttu-id="f2edf-103">부하 분산 장치에 백 엔드 주소 풀 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edf-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2edf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2edf-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2edf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2edf-105">DESCRIPTION</span></span>
<span data-ttu-id="f2edf-106">**추가-AzureRmLoadBalancerBackend** Cmdlet은 Azure 부하 분산 장치에 백 엔드 주소 풀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edf-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="f2edf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f2edf-107">EXAMPLES</span></span>

### <span data-ttu-id="f2edf-108">예제 1 부하 분산 장치에 백 엔드 주소 풀 구성 추가</span><span class="sxs-lookup"><span data-stu-id="f2edf-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="f2edf-109">이 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져오고 BackendAddressPool02 이라는 이름의 백엔드 주소 풀을 MyLoadBalancer에 추가한 다음 **Set-AzureRmLoadBalancer** cmdlet을 사용 하 여 myloadbalancer를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edf-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="f2edf-110">변수</span><span class="sxs-lookup"><span data-stu-id="f2edf-110">PARAMETERS</span></span>

### <span data-ttu-id="f2edf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2edf-111">-DefaultProfile</span></span>
<span data-ttu-id="f2edf-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2edf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2edf-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2edf-113">-LoadBalancer</span></span>
<span data-ttu-id="f2edf-114">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edf-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="f2edf-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f2edf-115">-Name</span></span>
<span data-ttu-id="f2edf-116">추가할 백 엔드 주소 풀 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edf-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2edf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2edf-117">CommonParameters</span></span>
<span data-ttu-id="f2edf-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2edf-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2edf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2edf-120">입력</span><span class="sxs-lookup"><span data-stu-id="f2edf-120">INPUTS</span></span>

### <span data-ttu-id="f2edf-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2edf-121">PSLoadBalancer</span></span>
<span data-ttu-id="f2edf-122">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2edf-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f2edf-123">출력</span><span class="sxs-lookup"><span data-stu-id="f2edf-123">OUTPUTS</span></span>

### <span data-ttu-id="f2edf-124">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2edf-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f2edf-125">상속자</span><span class="sxs-lookup"><span data-stu-id="f2edf-125">NOTES</span></span>

## <span data-ttu-id="f2edf-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2edf-126">RELATED LINKS</span></span>

[<span data-ttu-id="f2edf-127">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2edf-127">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f2edf-128">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f2edf-128">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="f2edf-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f2edf-129">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f2edf-130">새로운 AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f2edf-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f2edf-131">제거-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f2edf-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


