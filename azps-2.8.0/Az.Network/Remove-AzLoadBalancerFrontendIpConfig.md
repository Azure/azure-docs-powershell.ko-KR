---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 75a12ab9543eb19301cc8e17e4ebff6e4db80c00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869713"
---
# <span data-ttu-id="1e626-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e626-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="1e626-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e626-102">SYNOPSIS</span></span>
<span data-ttu-id="1e626-103">부하 분산 장치에서 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="1e626-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e626-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e626-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e626-105">DESCRIPTION</span></span>
<span data-ttu-id="1e626-106">**AzLoadBalancerFrontendIpConfig** Cmdlet은 Azure 부하 분산 장치에서 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="1e626-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1e626-107">EXAMPLES</span></span>

### <span data-ttu-id="1e626-108">예제 1: 부하 분산 장치에서 프런트 엔드 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="1e626-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="1e626-109">첫 번째 명령은 제거 하려는 프런트 엔드 IP 구성과 연결 된 부하 분산을 가져온 다음 $loadbalancer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="1e626-110">두 번째 명령은 $loadbalancer의 부하 분산 장치에서 연결 된 프런트 엔드 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="1e626-111">변수</span><span class="sxs-lookup"><span data-stu-id="1e626-111">PARAMETERS</span></span>

### <span data-ttu-id="1e626-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e626-112">-DefaultProfile</span></span>
<span data-ttu-id="1e626-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e626-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e626-114">-LoadBalancer</span></span>
<span data-ttu-id="1e626-115">제거할 프런트 엔드 IP 구성을 포함 하는 부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="1e626-116">-이름</span><span class="sxs-lookup"><span data-stu-id="1e626-116">-Name</span></span>
<span data-ttu-id="1e626-117">제거할 프런트 엔드 IP 주소 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="1e626-118">-확인</span><span class="sxs-lookup"><span data-stu-id="1e626-118">-Confirm</span></span>
<span data-ttu-id="1e626-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e626-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e626-120">-WhatIf</span></span>
<span data-ttu-id="1e626-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e626-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e626-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e626-123">CommonParameters</span></span>
<span data-ttu-id="1e626-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e626-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e626-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e626-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e626-126">입력</span><span class="sxs-lookup"><span data-stu-id="1e626-126">INPUTS</span></span>

### <span data-ttu-id="1e626-127">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e626-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1e626-128">출력</span><span class="sxs-lookup"><span data-stu-id="1e626-128">OUTPUTS</span></span>

### <span data-ttu-id="1e626-129">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e626-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1e626-130">상속자</span><span class="sxs-lookup"><span data-stu-id="1e626-130">NOTES</span></span>

## <span data-ttu-id="1e626-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e626-131">RELATED LINKS</span></span>

[<span data-ttu-id="1e626-132">추가-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e626-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1e626-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e626-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1e626-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e626-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1e626-135">새로운 AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e626-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1e626-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e626-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


