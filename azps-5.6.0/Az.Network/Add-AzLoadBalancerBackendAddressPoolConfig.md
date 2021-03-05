---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2cda323e33b0c6a719b9a11bae461d5ced34862e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012891"
---
# <span data-ttu-id="2abda-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2abda-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="2abda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2abda-102">SYNOPSIS</span></span>
<span data-ttu-id="2abda-103">부하 균형 조정기에 백던드 주소 풀 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2abda-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="2abda-104">구문</span><span class="sxs-lookup"><span data-stu-id="2abda-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2abda-105">설명</span><span class="sxs-lookup"><span data-stu-id="2abda-105">DESCRIPTION</span></span>
<span data-ttu-id="2abda-106">**Add-AzLoadBalancerBackend cmdlet은** 백end 주소 풀을 Azure 부하 분산기에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="2abda-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="2abda-107">예제</span><span class="sxs-lookup"><span data-stu-id="2abda-107">EXAMPLES</span></span>

### <span data-ttu-id="2abda-108">예제 1: 부하 저울에 백던드 주소 풀 구성 추가</span><span class="sxs-lookup"><span data-stu-id="2abda-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="2abda-109">이 명령은 MyLoadBalancer라는 부하 분산 기능을 얻게 되고 BackendAddressPool02라는 백end 주소 풀을 MyLoadBalancer에 추가한 다음 **Set-AzLoadBalancer** cmdlet을 사용하여 MyLoadBalancer를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2abda-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="2abda-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2abda-110">PARAMETERS</span></span>

### <span data-ttu-id="2abda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2abda-111">-DefaultProfile</span></span>
<span data-ttu-id="2abda-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2abda-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2abda-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2abda-113">-LoadBalancer</span></span>
<span data-ttu-id="2abda-114">**LoadBalancer 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="2abda-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="2abda-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2abda-115">-Name</span></span>
<span data-ttu-id="2abda-116">추가할 백end 주소 풀 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2abda-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abda-117">-확인</span><span class="sxs-lookup"><span data-stu-id="2abda-117">-Confirm</span></span>
<span data-ttu-id="2abda-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2abda-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2abda-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2abda-119">-WhatIf</span></span>
<span data-ttu-id="2abda-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2abda-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2abda-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2abda-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2abda-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2abda-122">CommonParameters</span></span>
<span data-ttu-id="2abda-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2abda-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2abda-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2abda-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2abda-125">입력</span><span class="sxs-lookup"><span data-stu-id="2abda-125">INPUTS</span></span>

### <span data-ttu-id="2abda-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2abda-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2abda-127">출력</span><span class="sxs-lookup"><span data-stu-id="2abda-127">OUTPUTS</span></span>

### <span data-ttu-id="2abda-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2abda-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2abda-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2abda-129">NOTES</span></span>

## <span data-ttu-id="2abda-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2abda-130">RELATED LINKS</span></span>

[<span data-ttu-id="2abda-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2abda-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="2abda-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2abda-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="2abda-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2abda-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="2abda-134">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2abda-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="2abda-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="2abda-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


