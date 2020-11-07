---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: 2359459688dbae2c718e4a5d5f65bf68b2c8c5ea
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882974"
---
# <span data-ttu-id="e294e-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e294e-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="e294e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e294e-102">SYNOPSIS</span></span>
<span data-ttu-id="e294e-103">응용 프로그램 게이트웨이의 SKU를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e294e-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e294e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e294e-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e294e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e294e-105">DESCRIPTION</span></span>
<span data-ttu-id="e294e-106">**AzureRmApplicationGatewaySku** cmdlet은 응용 프로그램 게이트웨이의 SKU (stock 유지 단위)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e294e-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="e294e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e294e-107">EXAMPLES</span></span>

### <span data-ttu-id="e294e-108">예제 1: 응용 프로그램 게이트웨이 SKU 가져오기</span><span class="sxs-lookup"><span data-stu-id="e294e-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="e294e-109">첫 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 가져와 그 결과를 $AppGW 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e294e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e294e-110">두 번째 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이의 SKU를 가져와 그 결과를 $SKU 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e294e-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="e294e-111">변수</span><span class="sxs-lookup"><span data-stu-id="e294e-111">PARAMETERS</span></span>

### <span data-ttu-id="e294e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e294e-112">-ApplicationGateway</span></span>
<span data-ttu-id="e294e-113">응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e294e-113">Specifies the application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e294e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e294e-114">-DefaultProfile</span></span>
<span data-ttu-id="e294e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e294e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e294e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e294e-116">CommonParameters</span></span>
<span data-ttu-id="e294e-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e294e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e294e-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e294e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e294e-119">입력</span><span class="sxs-lookup"><span data-stu-id="e294e-119">INPUTS</span></span>

### <span data-ttu-id="e294e-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e294e-120">System.String</span></span>

## <span data-ttu-id="e294e-121">출력</span><span class="sxs-lookup"><span data-stu-id="e294e-121">OUTPUTS</span></span>

### <span data-ttu-id="e294e-122">Microsoft. \*. i m a. 모델. m i m m</span><span class="sxs-lookup"><span data-stu-id="e294e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="e294e-123">상속자</span><span class="sxs-lookup"><span data-stu-id="e294e-123">NOTES</span></span>

## <span data-ttu-id="e294e-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e294e-124">RELATED LINKS</span></span>

[<span data-ttu-id="e294e-125">새로운 AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e294e-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="e294e-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e294e-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


