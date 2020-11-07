---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e97e8f3ed5769e4f81175b29f097aa4946d28881
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875680"
---
# <span data-ttu-id="4df18-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4df18-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="4df18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df18-102">SYNOPSIS</span></span>
<span data-ttu-id="4df18-103">부하 분산 장치에 백 엔드 주소 풀 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df18-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="4df18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4df18-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4df18-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4df18-105">DESCRIPTION</span></span>
<span data-ttu-id="4df18-106">**추가-AzLoadBalancerBackend** Cmdlet은 Azure 부하 분산 장치에 백 엔드 주소 풀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df18-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="4df18-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4df18-107">EXAMPLES</span></span>

### <span data-ttu-id="4df18-108">예제 1 부하 분산 장치에 백 엔드 주소 풀 구성 추가</span><span class="sxs-lookup"><span data-stu-id="4df18-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="4df18-109">이 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져오고 BackendAddressPool02 이라는 이름의 백엔드 주소 풀을 MyLoadBalancer에 추가한 다음 **Set-AzLoadBalancer** cmdlet을 사용 하 여 myloadbalancer를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df18-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="4df18-110">변수</span><span class="sxs-lookup"><span data-stu-id="4df18-110">PARAMETERS</span></span>

### <span data-ttu-id="4df18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df18-111">-DefaultProfile</span></span>
<span data-ttu-id="4df18-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4df18-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df18-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4df18-113">-LoadBalancer</span></span>
<span data-ttu-id="4df18-114">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df18-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="4df18-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4df18-115">-Name</span></span>
<span data-ttu-id="4df18-116">추가할 백 엔드 주소 풀 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df18-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="4df18-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df18-117">CommonParameters</span></span>
<span data-ttu-id="4df18-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df18-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df18-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4df18-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df18-120">입력</span><span class="sxs-lookup"><span data-stu-id="4df18-120">INPUTS</span></span>

### <span data-ttu-id="4df18-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4df18-121">PSLoadBalancer</span></span>
<span data-ttu-id="4df18-122">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4df18-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4df18-123">출력</span><span class="sxs-lookup"><span data-stu-id="4df18-123">OUTPUTS</span></span>

### <span data-ttu-id="4df18-124">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4df18-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4df18-125">상속자</span><span class="sxs-lookup"><span data-stu-id="4df18-125">NOTES</span></span>

## <span data-ttu-id="4df18-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4df18-126">RELATED LINKS</span></span>

[<span data-ttu-id="4df18-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4df18-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4df18-128">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4df18-128">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="4df18-129">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4df18-129">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4df18-130">새로운 AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4df18-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4df18-131">제거-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4df18-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


