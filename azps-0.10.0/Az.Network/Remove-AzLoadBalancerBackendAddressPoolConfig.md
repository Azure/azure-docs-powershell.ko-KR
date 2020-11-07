---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 30abb6f2d11eeae9749e7285a91ddeb93a1bf743
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875342"
---
# <span data-ttu-id="a5f4d-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a5f4d-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="a5f4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f4d-103">부하 분산 장치에서 백 엔드 주소 풀 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f4d-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="a5f4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5f4d-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5f4d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="a5f4d-106">**AzLoadBalancerBackendAddressPoolConfig** cmdlet은 부하 분산 장치에서 백 엔드 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f4d-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="a5f4d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a5f4d-107">EXAMPLES</span></span>

### <span data-ttu-id="a5f4d-108">예제 1: 부하 분산 장치에서 백 엔드 주소 풀 구성 제거</span><span class="sxs-lookup"><span data-stu-id="a5f4d-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="a5f4d-109">이 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져오고 **AzLoadBalancerBackendAddressPoolConfig** 에 전달 하 여 Myloadbalancer의 BackendAddressPool02 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f4d-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="a5f4d-110">마지막으로, Set-AzLoadBalancer cmdlet은 MyLoadBalancer를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f4d-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="a5f4d-111">백 엔드 주소 풀 구성은 반드시 있어야 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5f4d-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="a5f4d-112">변수</span><span class="sxs-lookup"><span data-stu-id="a5f4d-112">PARAMETERS</span></span>

### <span data-ttu-id="a5f4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f4d-113">-DefaultProfile</span></span>
<span data-ttu-id="a5f4d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5f4d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5f4d-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5f4d-115">-LoadBalancer</span></span>
<span data-ttu-id="a5f4d-116">제거할 백 엔드 주소 풀을 포함 하는 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f4d-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="a5f4d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a5f4d-117">-Name</span></span>
<span data-ttu-id="a5f4d-118">이 cmdlet이 제거 하는 백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f4d-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a5f4d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f4d-119">CommonParameters</span></span>
<span data-ttu-id="a5f4d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f4d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f4d-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5f4d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f4d-122">입력</span><span class="sxs-lookup"><span data-stu-id="a5f4d-122">INPUTS</span></span>

### <span data-ttu-id="a5f4d-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5f4d-123">PSLoadBalancer</span></span>
<span data-ttu-id="a5f4d-124">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5f4d-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a5f4d-125">출력</span><span class="sxs-lookup"><span data-stu-id="a5f4d-125">OUTPUTS</span></span>

### <span data-ttu-id="a5f4d-126">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5f4d-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a5f4d-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a5f4d-127">NOTES</span></span>

## <span data-ttu-id="a5f4d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5f4d-128">RELATED LINKS</span></span>

[<span data-ttu-id="a5f4d-129">추가-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a5f4d-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a5f4d-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5f4d-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a5f4d-131">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a5f4d-131">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="a5f4d-132">새로운 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a5f4d-132">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


