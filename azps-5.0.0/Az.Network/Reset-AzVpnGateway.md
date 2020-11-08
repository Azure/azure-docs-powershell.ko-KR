---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 4c9c5a71b09f12d41c1126327045cdea12842d71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215953"
---
# <span data-ttu-id="6a83a-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6a83a-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="6a83a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a83a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a83a-103">확장 가능한 VPN 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="6a83a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a83a-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a83a-105">ByVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6a83a-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a83a-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6a83a-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a83a-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6a83a-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a83a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6a83a-108">DESCRIPTION</span></span>
<span data-ttu-id="6a83a-109">VpnGateway를 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="6a83a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6a83a-110">EXAMPLES</span></span>

### <span data-ttu-id="6a83a-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="6a83a-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="6a83a-112">변수</span><span class="sxs-lookup"><span data-stu-id="6a83a-112">PARAMETERS</span></span>

### <span data-ttu-id="6a83a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a83a-113">-AsJob</span></span>
<span data-ttu-id="6a83a-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6a83a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a83a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a83a-115">-DefaultProfile</span></span>
<span data-ttu-id="6a83a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a83a-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="6a83a-117">-VpnGateway</span></span>
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

### <span data-ttu-id="6a83a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a83a-118">CommonParameters</span></span>
<span data-ttu-id="6a83a-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a83a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a83a-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a83a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a83a-121">입력</span><span class="sxs-lookup"><span data-stu-id="6a83a-121">INPUTS</span></span>

### <span data-ttu-id="6a83a-122">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6a83a-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="6a83a-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6a83a-123">System.String</span></span>

## <span data-ttu-id="6a83a-124">출력</span><span class="sxs-lookup"><span data-stu-id="6a83a-124">OUTPUTS</span></span>

### <span data-ttu-id="6a83a-125">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6a83a-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="6a83a-126">상속자</span><span class="sxs-lookup"><span data-stu-id="6a83a-126">NOTES</span></span>

## <span data-ttu-id="6a83a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a83a-127">RELATED LINKS</span></span>

[<span data-ttu-id="6a83a-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6a83a-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="6a83a-129">새로운 AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6a83a-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="6a83a-130">제거-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6a83a-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="6a83a-131">업데이트-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6a83a-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
