---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 4c9c5a71b09f12d41c1126327045cdea12842d71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184252"
---
# <span data-ttu-id="ff264-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ff264-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="ff264-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff264-102">SYNOPSIS</span></span>
<span data-ttu-id="ff264-103">확장 가능한 VPN 게이트웨이를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff264-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="ff264-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff264-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff264-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff264-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff264-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ff264-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff264-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ff264-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff264-108">설명</span><span class="sxs-lookup"><span data-stu-id="ff264-108">DESCRIPTION</span></span>
<span data-ttu-id="ff264-109">VpnGateway를 다시 설정</span><span class="sxs-lookup"><span data-stu-id="ff264-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="ff264-110">예제</span><span class="sxs-lookup"><span data-stu-id="ff264-110">EXAMPLES</span></span>

### <span data-ttu-id="ff264-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="ff264-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="ff264-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff264-112">PARAMETERS</span></span>

### <span data-ttu-id="ff264-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff264-113">-AsJob</span></span>
<span data-ttu-id="ff264-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ff264-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff264-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff264-115">-DefaultProfile</span></span>
<span data-ttu-id="ff264-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff264-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff264-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="ff264-117">-VpnGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff264-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff264-118">CommonParameters</span></span>
<span data-ttu-id="ff264-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff264-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff264-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ff264-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff264-121">입력</span><span class="sxs-lookup"><span data-stu-id="ff264-121">INPUTS</span></span>

### <span data-ttu-id="ff264-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ff264-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="ff264-123">System.String</span><span class="sxs-lookup"><span data-stu-id="ff264-123">System.String</span></span>

## <span data-ttu-id="ff264-124">출력</span><span class="sxs-lookup"><span data-stu-id="ff264-124">OUTPUTS</span></span>

### <span data-ttu-id="ff264-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ff264-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="ff264-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff264-126">NOTES</span></span>

## <span data-ttu-id="ff264-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff264-127">RELATED LINKS</span></span>

[<span data-ttu-id="ff264-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ff264-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="ff264-129">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ff264-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="ff264-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ff264-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="ff264-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ff264-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
