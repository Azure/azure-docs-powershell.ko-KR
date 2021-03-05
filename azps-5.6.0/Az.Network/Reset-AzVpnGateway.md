---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 33abb4e724f5a442efd6791cbf6256100662ab65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979531"
---
# <span data-ttu-id="25dd9-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="25dd9-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="25dd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="25dd9-103">확장 가능한 VPN 게이트웨이를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="25dd9-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="25dd9-104">구문</span><span class="sxs-lookup"><span data-stu-id="25dd9-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25dd9-105">ByVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="25dd9-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25dd9-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="25dd9-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25dd9-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="25dd9-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25dd9-108">설명</span><span class="sxs-lookup"><span data-stu-id="25dd9-108">DESCRIPTION</span></span>
<span data-ttu-id="25dd9-109">VpnGateway 재설정</span><span class="sxs-lookup"><span data-stu-id="25dd9-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="25dd9-110">예제</span><span class="sxs-lookup"><span data-stu-id="25dd9-110">EXAMPLES</span></span>

### <span data-ttu-id="25dd9-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="25dd9-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="25dd9-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="25dd9-112">PARAMETERS</span></span>

### <span data-ttu-id="25dd9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25dd9-113">-AsJob</span></span>
<span data-ttu-id="25dd9-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="25dd9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25dd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25dd9-115">-DefaultProfile</span></span>
<span data-ttu-id="25dd9-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25dd9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25dd9-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="25dd9-117">-VpnGateway</span></span>
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

### <span data-ttu-id="25dd9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25dd9-118">CommonParameters</span></span>
<span data-ttu-id="25dd9-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25dd9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25dd9-120">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="25dd9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25dd9-121">입력</span><span class="sxs-lookup"><span data-stu-id="25dd9-121">INPUTS</span></span>

### <span data-ttu-id="25dd9-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="25dd9-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="25dd9-123">System.String</span><span class="sxs-lookup"><span data-stu-id="25dd9-123">System.String</span></span>

## <span data-ttu-id="25dd9-124">출력</span><span class="sxs-lookup"><span data-stu-id="25dd9-124">OUTPUTS</span></span>

### <span data-ttu-id="25dd9-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="25dd9-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="25dd9-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25dd9-126">NOTES</span></span>

## <span data-ttu-id="25dd9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25dd9-127">RELATED LINKS</span></span>

[<span data-ttu-id="25dd9-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="25dd9-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="25dd9-129">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="25dd9-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="25dd9-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="25dd9-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="25dd9-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="25dd9-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
