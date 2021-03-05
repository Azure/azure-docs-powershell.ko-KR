---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: cf869a0de5847b1930879dbd610749746370791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994065"
---
# <span data-ttu-id="04fee-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="04fee-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="04fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04fee-102">SYNOPSIS</span></span>
<span data-ttu-id="04fee-103">애플리케이션 게이트웨이의 SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="04fee-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="04fee-104">구문</span><span class="sxs-lookup"><span data-stu-id="04fee-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04fee-105">설명</span><span class="sxs-lookup"><span data-stu-id="04fee-105">DESCRIPTION</span></span>
<span data-ttu-id="04fee-106">**Get-AzApplicationGatewaySku** cmdlet은 애플리케이션 게이트웨이의 SKU(재고 유지 장치)를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="04fee-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="04fee-107">예제</span><span class="sxs-lookup"><span data-stu-id="04fee-107">EXAMPLES</span></span>

### <span data-ttu-id="04fee-108">예제 1: 애플리케이션 게이트웨이 SKU를 얻다</span><span class="sxs-lookup"><span data-stu-id="04fee-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="04fee-109">첫 번째 명령은 ApplicationGateway01이라는 Application Gateway를 얻게 하여 결과를 $AppGW.</span><span class="sxs-lookup"><span data-stu-id="04fee-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="04fee-110">두 번째 명령은 ApplicationGateway01이라는 애플리케이션 게이트웨이의 SKU를 얻게 하여 결과를 $SKU.</span><span class="sxs-lookup"><span data-stu-id="04fee-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="04fee-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="04fee-111">PARAMETERS</span></span>

### <span data-ttu-id="04fee-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04fee-112">-ApplicationGateway</span></span>
<span data-ttu-id="04fee-113">애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04fee-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="04fee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04fee-114">-DefaultProfile</span></span>
<span data-ttu-id="04fee-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04fee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04fee-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04fee-116">CommonParameters</span></span>
<span data-ttu-id="04fee-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04fee-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04fee-118">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04fee-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04fee-119">입력</span><span class="sxs-lookup"><span data-stu-id="04fee-119">INPUTS</span></span>

### <span data-ttu-id="04fee-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="04fee-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="04fee-121">출력</span><span class="sxs-lookup"><span data-stu-id="04fee-121">OUTPUTS</span></span>

### <span data-ttu-id="04fee-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="04fee-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="04fee-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04fee-123">NOTES</span></span>

## <span data-ttu-id="04fee-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04fee-124">RELATED LINKS</span></span>

[<span data-ttu-id="04fee-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="04fee-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="04fee-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="04fee-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


