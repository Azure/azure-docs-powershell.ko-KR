---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184265"
---
# <span data-ttu-id="374b3-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="374b3-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="374b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="374b3-102">SYNOPSIS</span></span>
<span data-ttu-id="374b3-103">Virtual Network 게이트웨이 다시 설정</span><span class="sxs-lookup"><span data-stu-id="374b3-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="374b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="374b3-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="374b3-105">설명</span><span class="sxs-lookup"><span data-stu-id="374b3-105">DESCRIPTION</span></span>
<span data-ttu-id="374b3-106">Virtual Network 게이트웨이 다시 설정</span><span class="sxs-lookup"><span data-stu-id="374b3-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="374b3-107">예제</span><span class="sxs-lookup"><span data-stu-id="374b3-107">EXAMPLES</span></span>

### <span data-ttu-id="374b3-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="374b3-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="374b3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="374b3-109">PARAMETERS</span></span>

### <span data-ttu-id="374b3-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="374b3-110">-AsJob</span></span>
<span data-ttu-id="374b3-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="374b3-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="374b3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="374b3-112">-DefaultProfile</span></span>
<span data-ttu-id="374b3-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="374b3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="374b3-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="374b3-114">-GatewayVip</span></span>
<span data-ttu-id="374b3-115">특정 게이트웨이 인스턴스를 다시 설정하기 위한 게이트웨이 vip입니다(예: Active-Active 활성화된 게이트웨이의 경우). 기본적으로 값이 전달되지 않았다면 게이트웨이 기본 인스턴스가 다시 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="374b3-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="374b3-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="374b3-116">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="374b3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="374b3-117">CommonParameters</span></span>
<span data-ttu-id="374b3-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="374b3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="374b3-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="374b3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="374b3-120">입력</span><span class="sxs-lookup"><span data-stu-id="374b3-120">INPUTS</span></span>

### <span data-ttu-id="374b3-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="374b3-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="374b3-122">System.String</span><span class="sxs-lookup"><span data-stu-id="374b3-122">System.String</span></span>

## <span data-ttu-id="374b3-123">출력</span><span class="sxs-lookup"><span data-stu-id="374b3-123">OUTPUTS</span></span>

### <span data-ttu-id="374b3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="374b3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="374b3-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="374b3-125">NOTES</span></span>

## <span data-ttu-id="374b3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="374b3-126">RELATED LINKS</span></span>

[<span data-ttu-id="374b3-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="374b3-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="374b3-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="374b3-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="374b3-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="374b3-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="374b3-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="374b3-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="374b3-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="374b3-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
