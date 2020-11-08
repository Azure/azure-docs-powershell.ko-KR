---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212494"
---
# <span data-ttu-id="256ae-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="256ae-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="256ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="256ae-102">SYNOPSIS</span></span>
<span data-ttu-id="256ae-103">응용 프로그램 게이트웨이의 SKU를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="256ae-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="256ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="256ae-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="256ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="256ae-105">DESCRIPTION</span></span>
<span data-ttu-id="256ae-106">**AzApplicationGatewaySku** cmdlet은 응용 프로그램 게이트웨이의 SKU (stock 유지 단위)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="256ae-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="256ae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="256ae-107">EXAMPLES</span></span>

### <span data-ttu-id="256ae-108">예제 1: 응용 프로그램 게이트웨이 SKU 가져오기</span><span class="sxs-lookup"><span data-stu-id="256ae-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="256ae-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="256ae-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="256ae-110">두 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이의 SKU를 가져와 그 결과를 $SKU 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="256ae-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="256ae-111">변수</span><span class="sxs-lookup"><span data-stu-id="256ae-111">PARAMETERS</span></span>

### <span data-ttu-id="256ae-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="256ae-112">-ApplicationGateway</span></span>
<span data-ttu-id="256ae-113">응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="256ae-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="256ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="256ae-114">-DefaultProfile</span></span>
<span data-ttu-id="256ae-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="256ae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="256ae-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="256ae-116">CommonParameters</span></span>
<span data-ttu-id="256ae-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="256ae-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="256ae-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="256ae-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="256ae-119">입력</span><span class="sxs-lookup"><span data-stu-id="256ae-119">INPUTS</span></span>

### <span data-ttu-id="256ae-120">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="256ae-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="256ae-121">출력</span><span class="sxs-lookup"><span data-stu-id="256ae-121">OUTPUTS</span></span>

### <span data-ttu-id="256ae-122">Microsoft. \*. i m a. 모델. m i m m</span><span class="sxs-lookup"><span data-stu-id="256ae-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="256ae-123">상속자</span><span class="sxs-lookup"><span data-stu-id="256ae-123">NOTES</span></span>

## <span data-ttu-id="256ae-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="256ae-124">RELATED LINKS</span></span>

[<span data-ttu-id="256ae-125">새로운 AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="256ae-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="256ae-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="256ae-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


