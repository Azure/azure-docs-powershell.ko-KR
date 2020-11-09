---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 7d373092f850dd25abe5b6d913ddcf2572d4be94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310202"
---
# <span data-ttu-id="3ee41-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="3ee41-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="3ee41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee41-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee41-103">부하 분산 장치 백 엔드 주소 구성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee41-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="3ee41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ee41-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ee41-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3ee41-105">DESCRIPTION</span></span>
<span data-ttu-id="3ee41-106">부하 분산 장치 백 엔드 주소 구성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee41-106">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="3ee41-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3ee41-107">EXAMPLES</span></span>

### <span data-ttu-id="3ee41-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ee41-108">Example 1</span></span>
### <span data-ttu-id="3ee41-109">예제 2: 가상 네트워크 참조를 사용 하는 새 loadbalancer 주소 구성</span><span class="sxs-lookup"><span data-stu-id="3ee41-109">Example 2: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

## <span data-ttu-id="3ee41-110">변수</span><span class="sxs-lookup"><span data-stu-id="3ee41-110">PARAMETERS</span></span>

### <span data-ttu-id="3ee41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee41-111">-DefaultProfile</span></span>
<span data-ttu-id="3ee41-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee41-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee41-113">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="3ee41-113">-IpAddress</span></span>
<span data-ttu-id="3ee41-114">백 엔드 풀에 추가 하는 IPAddress</span><span class="sxs-lookup"><span data-stu-id="3ee41-114">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee41-115">-이름</span><span class="sxs-lookup"><span data-stu-id="3ee41-115">-Name</span></span>
<span data-ttu-id="3ee41-116">백 엔드 주소 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ee41-116">The name of the Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee41-117">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3ee41-117">-VirtualNetworkId</span></span>
<span data-ttu-id="3ee41-118">백 엔드 주소 구성에 연결 된 가상 네트워크</span><span class="sxs-lookup"><span data-stu-id="3ee41-118">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee41-119">-확인</span><span class="sxs-lookup"><span data-stu-id="3ee41-119">-Confirm</span></span>
<span data-ttu-id="3ee41-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee41-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee41-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ee41-121">-WhatIf</span></span>
<span data-ttu-id="3ee41-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ee41-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ee41-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ee41-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee41-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee41-124">CommonParameters</span></span>
<span data-ttu-id="3ee41-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ee41-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee41-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3ee41-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee41-127">입력</span><span class="sxs-lookup"><span data-stu-id="3ee41-127">INPUTS</span></span>

### <span data-ttu-id="3ee41-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3ee41-128">System.String</span></span>

### <span data-ttu-id="3ee41-129">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="3ee41-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="3ee41-130">출력</span><span class="sxs-lookup"><span data-stu-id="3ee41-130">OUTPUTS</span></span>

### <span data-ttu-id="3ee41-131">PSLoadBalancerBackendAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="3ee41-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="3ee41-132">상속자</span><span class="sxs-lookup"><span data-stu-id="3ee41-132">NOTES</span></span>

## <span data-ttu-id="3ee41-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ee41-133">RELATED LINKS</span></span>
