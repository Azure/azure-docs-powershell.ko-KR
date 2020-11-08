---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: 736e9abe12b00420a4d494510f2cd0d737ae3e02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048859"
---
# <span data-ttu-id="f2dcc-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f2dcc-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="f2dcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="f2dcc-103">확장 가능한 P2S VPN 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2dcc-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="f2dcc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2dcc-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2dcc-105">ByP2SVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f2dcc-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2dcc-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="f2dcc-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2dcc-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="f2dcc-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2dcc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f2dcc-108">DESCRIPTION</span></span>
<span data-ttu-id="f2dcc-109">P2SVpnGateway를 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2dcc-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="f2dcc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f2dcc-110">EXAMPLES</span></span>

### <span data-ttu-id="f2dcc-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="f2dcc-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="f2dcc-112">변수</span><span class="sxs-lookup"><span data-stu-id="f2dcc-112">PARAMETERS</span></span>

### <span data-ttu-id="f2dcc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2dcc-113">-AsJob</span></span>
<span data-ttu-id="f2dcc-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f2dcc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2dcc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2dcc-115">-DefaultProfile</span></span>
<span data-ttu-id="f2dcc-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2dcc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2dcc-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f2dcc-117">-P2SVpnGateway</span></span>
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

### <span data-ttu-id="f2dcc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2dcc-118">CommonParameters</span></span>
<span data-ttu-id="f2dcc-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2dcc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2dcc-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2dcc-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2dcc-121">입력</span><span class="sxs-lookup"><span data-stu-id="f2dcc-121">INPUTS</span></span>

### <span data-ttu-id="f2dcc-122">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f2dcc-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="f2dcc-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2dcc-123">System.String</span></span>

## <span data-ttu-id="f2dcc-124">출력</span><span class="sxs-lookup"><span data-stu-id="f2dcc-124">OUTPUTS</span></span>

### <span data-ttu-id="f2dcc-125">PSP2SVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f2dcc-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="f2dcc-126">상속자</span><span class="sxs-lookup"><span data-stu-id="f2dcc-126">NOTES</span></span>

## <span data-ttu-id="f2dcc-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2dcc-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2dcc-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f2dcc-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="f2dcc-129">새로운 AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f2dcc-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="f2dcc-130">제거-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f2dcc-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="f2dcc-131">업데이트-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f2dcc-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
