---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322776"
---
# <span data-ttu-id="e3479-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e3479-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="e3479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3479-102">SYNOPSIS</span></span>
<span data-ttu-id="e3479-103">애플리케이션 게이트웨이의 SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e3479-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="e3479-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3479-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3479-105">설명</span><span class="sxs-lookup"><span data-stu-id="e3479-105">DESCRIPTION</span></span>
<span data-ttu-id="e3479-106">**Get-AzApplicationGatewaySku** cmdlet은 애플리케이션 게이트웨이의 SKU(Stock Keeping Unit)를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e3479-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="e3479-107">예제</span><span class="sxs-lookup"><span data-stu-id="e3479-107">EXAMPLES</span></span>

### <span data-ttu-id="e3479-108">예제 1: 애플리케이션 게이트웨이 SKU를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3479-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="e3479-109">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 해당 애플리케이션이라는 변수에 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e3479-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e3479-110">두 번째 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이의 SKU를 사용하여 결과를 $SKU.</span><span class="sxs-lookup"><span data-stu-id="e3479-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="e3479-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3479-111">PARAMETERS</span></span>

### <span data-ttu-id="e3479-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3479-112">-ApplicationGateway</span></span>
<span data-ttu-id="e3479-113">애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e3479-113">Specifies the application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3479-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3479-114">-DefaultProfile</span></span>
<span data-ttu-id="e3479-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3479-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3479-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3479-116">CommonParameters</span></span>
<span data-ttu-id="e3479-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3479-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3479-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3479-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3479-119">입력</span><span class="sxs-lookup"><span data-stu-id="e3479-119">INPUTS</span></span>

### <span data-ttu-id="e3479-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3479-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3479-121">출력</span><span class="sxs-lookup"><span data-stu-id="e3479-121">OUTPUTS</span></span>

### <span data-ttu-id="e3479-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e3479-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="e3479-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3479-123">NOTES</span></span>

## <span data-ttu-id="e3479-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3479-124">RELATED LINKS</span></span>

[<span data-ttu-id="e3479-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e3479-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="e3479-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e3479-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


