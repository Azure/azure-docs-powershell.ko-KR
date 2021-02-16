---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206693"
---
# <span data-ttu-id="059d3-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="059d3-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="059d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059d3-102">SYNOPSIS</span></span>
<span data-ttu-id="059d3-103">부하 균형 조정에 대한 백end 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="059d3-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="059d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="059d3-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059d3-105">설명</span><span class="sxs-lookup"><span data-stu-id="059d3-105">DESCRIPTION</span></span>
<span data-ttu-id="059d3-106">**New-AzLoadBalancerBackendAddressPoolConfig** cmdlet은 Azure Load Balancer에 대한 백end 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="059d3-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="059d3-107">예제</span><span class="sxs-lookup"><span data-stu-id="059d3-107">EXAMPLES</span></span>

### <span data-ttu-id="059d3-108">예제 1: 부하 균형 조정에 대한 백end 주소 풀 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="059d3-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="059d3-109">이 명령은 부하 균형 조정에 대한 BackendAddressPool02라는 백end 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="059d3-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="059d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="059d3-110">PARAMETERS</span></span>

### <span data-ttu-id="059d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059d3-111">-DefaultProfile</span></span>
<span data-ttu-id="059d3-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="059d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="059d3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="059d3-113">-Name</span></span>
<span data-ttu-id="059d3-114">만들 주소 풀 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="059d3-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="059d3-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="059d3-115">-Confirm</span></span>
<span data-ttu-id="059d3-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="059d3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059d3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059d3-117">-WhatIf</span></span>
<span data-ttu-id="059d3-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="059d3-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="059d3-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="059d3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059d3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059d3-120">CommonParameters</span></span>
<span data-ttu-id="059d3-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="059d3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059d3-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="059d3-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059d3-123">입력</span><span class="sxs-lookup"><span data-stu-id="059d3-123">INPUTS</span></span>

### <span data-ttu-id="059d3-124">없음</span><span class="sxs-lookup"><span data-stu-id="059d3-124">None</span></span>

## <span data-ttu-id="059d3-125">출력</span><span class="sxs-lookup"><span data-stu-id="059d3-125">OUTPUTS</span></span>

### <span data-ttu-id="059d3-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="059d3-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="059d3-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="059d3-127">NOTES</span></span>

## <span data-ttu-id="059d3-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="059d3-128">RELATED LINKS</span></span>

[<span data-ttu-id="059d3-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="059d3-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="059d3-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="059d3-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="059d3-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="059d3-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


