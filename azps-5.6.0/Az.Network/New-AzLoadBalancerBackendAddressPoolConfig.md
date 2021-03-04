---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 805afd046505f6b1f6695205e858c6215c57ec7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955792"
---
# <span data-ttu-id="359c0-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="359c0-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="359c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="359c0-102">SYNOPSIS</span></span>
<span data-ttu-id="359c0-103">부하 저울에 대한 백던드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="359c0-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="359c0-104">구문</span><span class="sxs-lookup"><span data-stu-id="359c0-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="359c0-105">설명</span><span class="sxs-lookup"><span data-stu-id="359c0-105">DESCRIPTION</span></span>
<span data-ttu-id="359c0-106">**New-AzLoadBalancerBackendAddressPoolConfig** cmdlet은 Azure 부하 분산기에 대한 백end 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="359c0-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="359c0-107">예제</span><span class="sxs-lookup"><span data-stu-id="359c0-107">EXAMPLES</span></span>

### <span data-ttu-id="359c0-108">예제 1: 부하 저울에 대한 백던드 주소 풀 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="359c0-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="359c0-109">이 명령은 부하 균형기용 BackendAddressPool02라는 백던드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="359c0-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="359c0-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="359c0-110">PARAMETERS</span></span>

### <span data-ttu-id="359c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="359c0-111">-DefaultProfile</span></span>
<span data-ttu-id="359c0-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="359c0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="359c0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="359c0-113">-Name</span></span>
<span data-ttu-id="359c0-114">만들 주소 풀 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="359c0-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="359c0-115">-확인</span><span class="sxs-lookup"><span data-stu-id="359c0-115">-Confirm</span></span>
<span data-ttu-id="359c0-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="359c0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="359c0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="359c0-117">-WhatIf</span></span>
<span data-ttu-id="359c0-118">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="359c0-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="359c0-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="359c0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="359c0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="359c0-120">CommonParameters</span></span>
<span data-ttu-id="359c0-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="359c0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="359c0-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="359c0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="359c0-123">입력</span><span class="sxs-lookup"><span data-stu-id="359c0-123">INPUTS</span></span>

### <span data-ttu-id="359c0-124">없음</span><span class="sxs-lookup"><span data-stu-id="359c0-124">None</span></span>

## <span data-ttu-id="359c0-125">출력</span><span class="sxs-lookup"><span data-stu-id="359c0-125">OUTPUTS</span></span>

### <span data-ttu-id="359c0-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="359c0-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="359c0-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="359c0-127">NOTES</span></span>

## <span data-ttu-id="359c0-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="359c0-128">RELATED LINKS</span></span>

[<span data-ttu-id="359c0-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="359c0-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="359c0-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="359c0-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="359c0-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="359c0-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


