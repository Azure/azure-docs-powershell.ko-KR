---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2819da4d49a116f451b3842c5e0eab1702d8c4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530196"
---
# <span data-ttu-id="c42ff-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c42ff-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="c42ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c42ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c42ff-103">부하 분산 장치에 대 한 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c42ff-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c42ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c42ff-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c42ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c42ff-105">DESCRIPTION</span></span>
<span data-ttu-id="c42ff-106">**AzureRmLoadBalancerBackendAddressPoolConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c42ff-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c42ff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c42ff-107">EXAMPLES</span></span>

### <span data-ttu-id="c42ff-108">예제 1: 부하 분산 장치에 대 한 백 엔드 주소 풀 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="c42ff-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="c42ff-109">이 명령은 부하 분산 장치에 대 한 BackendAddressPool02 이라는 백 엔드 주소 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c42ff-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="c42ff-110">변수</span><span class="sxs-lookup"><span data-stu-id="c42ff-110">PARAMETERS</span></span>

### <span data-ttu-id="c42ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42ff-111">-DefaultProfile</span></span>
<span data-ttu-id="c42ff-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c42ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42ff-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c42ff-113">-Name</span></span>
<span data-ttu-id="c42ff-114">만들려는 주소 풀 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42ff-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="c42ff-115">-확인</span><span class="sxs-lookup"><span data-stu-id="c42ff-115">-Confirm</span></span>
<span data-ttu-id="c42ff-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42ff-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c42ff-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c42ff-117">-WhatIf</span></span>
<span data-ttu-id="c42ff-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c42ff-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c42ff-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c42ff-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c42ff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42ff-120">CommonParameters</span></span>
<span data-ttu-id="c42ff-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42ff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42ff-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c42ff-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42ff-123">입력</span><span class="sxs-lookup"><span data-stu-id="c42ff-123">INPUTS</span></span>

### <span data-ttu-id="c42ff-124">않아야</span><span class="sxs-lookup"><span data-stu-id="c42ff-124">None</span></span>

## <span data-ttu-id="c42ff-125">출력</span><span class="sxs-lookup"><span data-stu-id="c42ff-125">OUTPUTS</span></span>

### <span data-ttu-id="c42ff-126">PSBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c42ff-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c42ff-127">상속자</span><span class="sxs-lookup"><span data-stu-id="c42ff-127">NOTES</span></span>

## <span data-ttu-id="c42ff-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c42ff-128">RELATED LINKS</span></span>

[<span data-ttu-id="c42ff-129">추가-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c42ff-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c42ff-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c42ff-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c42ff-131">제거-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c42ff-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


