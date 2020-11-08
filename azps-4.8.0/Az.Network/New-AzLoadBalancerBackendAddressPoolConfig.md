---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214831"
---
# <span data-ttu-id="67caa-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="67caa-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="67caa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67caa-102">SYNOPSIS</span></span>
<span data-ttu-id="67caa-103">부하 분산 장치에 대 한 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67caa-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="67caa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67caa-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67caa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67caa-105">DESCRIPTION</span></span>
<span data-ttu-id="67caa-106">**AzLoadBalancerBackendAddressPoolConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67caa-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="67caa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="67caa-107">EXAMPLES</span></span>

### <span data-ttu-id="67caa-108">예제 1: 부하 분산 장치에 대 한 백 엔드 주소 풀 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="67caa-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="67caa-109">이 명령은 부하 분산 장치에 대 한 BackendAddressPool02 이라는 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67caa-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="67caa-110">변수</span><span class="sxs-lookup"><span data-stu-id="67caa-110">PARAMETERS</span></span>

### <span data-ttu-id="67caa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67caa-111">-DefaultProfile</span></span>
<span data-ttu-id="67caa-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67caa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67caa-113">-이름</span><span class="sxs-lookup"><span data-stu-id="67caa-113">-Name</span></span>
<span data-ttu-id="67caa-114">만들려는 주소 풀 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67caa-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="67caa-115">-확인</span><span class="sxs-lookup"><span data-stu-id="67caa-115">-Confirm</span></span>
<span data-ttu-id="67caa-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67caa-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67caa-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67caa-117">-WhatIf</span></span>
<span data-ttu-id="67caa-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67caa-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67caa-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67caa-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67caa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67caa-120">CommonParameters</span></span>
<span data-ttu-id="67caa-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67caa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67caa-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67caa-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67caa-123">입력</span><span class="sxs-lookup"><span data-stu-id="67caa-123">INPUTS</span></span>

### <span data-ttu-id="67caa-124">않아야</span><span class="sxs-lookup"><span data-stu-id="67caa-124">None</span></span>

## <span data-ttu-id="67caa-125">출력</span><span class="sxs-lookup"><span data-stu-id="67caa-125">OUTPUTS</span></span>

### <span data-ttu-id="67caa-126">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="67caa-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="67caa-127">상속자</span><span class="sxs-lookup"><span data-stu-id="67caa-127">NOTES</span></span>

## <span data-ttu-id="67caa-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67caa-128">RELATED LINKS</span></span>

[<span data-ttu-id="67caa-129">추가-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="67caa-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="67caa-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="67caa-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="67caa-131">제거-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="67caa-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


