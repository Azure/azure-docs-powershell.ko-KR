---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: 736e9abe12b00420a4d494510f2cd0d737ae3e02
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351386"
---
# <span data-ttu-id="edb92-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="edb92-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="edb92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb92-102">SYNOPSIS</span></span>
<span data-ttu-id="edb92-103">확장 가능한 P2S VPN 게이트웨이를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="edb92-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="edb92-104">구문</span><span class="sxs-lookup"><span data-stu-id="edb92-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edb92-105">ByP2SVpnGatewayName(기본값)</span><span class="sxs-lookup"><span data-stu-id="edb92-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edb92-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="edb92-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edb92-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="edb92-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb92-108">설명</span><span class="sxs-lookup"><span data-stu-id="edb92-108">DESCRIPTION</span></span>
<span data-ttu-id="edb92-109">P2SVpnGateway를 다시 설정</span><span class="sxs-lookup"><span data-stu-id="edb92-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="edb92-110">예제</span><span class="sxs-lookup"><span data-stu-id="edb92-110">EXAMPLES</span></span>

### <span data-ttu-id="edb92-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="edb92-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="edb92-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edb92-112">PARAMETERS</span></span>

### <span data-ttu-id="edb92-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edb92-113">-AsJob</span></span>
<span data-ttu-id="edb92-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="edb92-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edb92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb92-115">-DefaultProfile</span></span>
<span data-ttu-id="edb92-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="edb92-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edb92-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="edb92-117">-P2SVpnGateway</span></span>
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

### <span data-ttu-id="edb92-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb92-118">CommonParameters</span></span>
<span data-ttu-id="edb92-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="edb92-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb92-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="edb92-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb92-121">입력</span><span class="sxs-lookup"><span data-stu-id="edb92-121">INPUTS</span></span>

### <span data-ttu-id="edb92-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="edb92-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="edb92-123">System.String</span><span class="sxs-lookup"><span data-stu-id="edb92-123">System.String</span></span>

## <span data-ttu-id="edb92-124">출력</span><span class="sxs-lookup"><span data-stu-id="edb92-124">OUTPUTS</span></span>

### <span data-ttu-id="edb92-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="edb92-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="edb92-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="edb92-126">NOTES</span></span>

## <span data-ttu-id="edb92-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edb92-127">RELATED LINKS</span></span>

[<span data-ttu-id="edb92-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="edb92-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="edb92-129">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="edb92-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="edb92-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="edb92-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="edb92-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="edb92-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
