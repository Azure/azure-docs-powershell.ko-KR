---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 9bbfa0aec2da00ada25fc4bb8a5334f67e80e41a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882881"
---
# <span data-ttu-id="b9c3d-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b9c3d-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b9c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c3d-103">부하 분산 장치에서 백 엔드 주소 풀 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9c3d-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b9c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c3d-106">**AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet은 부하 분산 장치에서 백 엔드 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="b9c3d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b9c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c3d-108">예제 1: 부하 분산 장치에서 백 엔드 주소 풀 구성 제거</span><span class="sxs-lookup"><span data-stu-id="b9c3d-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="b9c3d-109">이 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져오고 **AzureRmLoadBalancerBackendAddressPoolConfig** 에 전달 하 여 Myloadbalancer의 BackendAddressPool02 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="b9c3d-110">마지막으로, Set-AzureRmLoadBalancer cmdlet은 MyLoadBalancer를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="b9c3d-111">백 엔드 주소 풀 구성은 반드시 있어야 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="b9c3d-112">변수</span><span class="sxs-lookup"><span data-stu-id="b9c3d-112">PARAMETERS</span></span>

### <span data-ttu-id="b9c3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c3d-113">-DefaultProfile</span></span>
<span data-ttu-id="b9c3d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c3d-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b9c3d-115">-LoadBalancer</span></span>
<span data-ttu-id="b9c3d-116">제거할 백 엔드 주소 풀을 포함 하는 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="b9c3d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b9c3d-117">-Name</span></span>
<span data-ttu-id="b9c3d-118">이 cmdlet이 제거 하는 백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b9c3d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c3d-119">CommonParameters</span></span>
<span data-ttu-id="b9c3d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c3d-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c3d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c3d-122">입력</span><span class="sxs-lookup"><span data-stu-id="b9c3d-122">INPUTS</span></span>

### <span data-ttu-id="b9c3d-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b9c3d-123">PSLoadBalancer</span></span>
<span data-ttu-id="b9c3d-124">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c3d-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b9c3d-125">출력</span><span class="sxs-lookup"><span data-stu-id="b9c3d-125">OUTPUTS</span></span>

### <span data-ttu-id="b9c3d-126">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b9c3d-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b9c3d-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b9c3d-127">NOTES</span></span>

## <span data-ttu-id="b9c3d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9c3d-128">RELATED LINKS</span></span>

[<span data-ttu-id="b9c3d-129">추가-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b9c3d-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b9c3d-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b9c3d-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b9c3d-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b9c3d-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b9c3d-132">새로운 AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b9c3d-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


