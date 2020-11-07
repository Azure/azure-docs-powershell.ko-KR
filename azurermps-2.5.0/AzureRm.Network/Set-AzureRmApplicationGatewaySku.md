---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: ccefc75d28ee49f12dd1f72d03512e3850298986
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881321"
---
# <span data-ttu-id="61a31-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="61a31-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="61a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61a31-102">SYNOPSIS</span></span>
<span data-ttu-id="61a31-103">응용 프로그램 게이트웨이의 SKU를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61a31-104">구문과</span><span class="sxs-lookup"><span data-stu-id="61a31-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61a31-105">설명은</span><span class="sxs-lookup"><span data-stu-id="61a31-105">DESCRIPTION</span></span>
<span data-ttu-id="61a31-106">**AzureRmApplicationGatewaySku** cmdlet은 응용 프로그램 게이트웨이의 SKU (stock 보관 단위)를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="61a31-107">예제의</span><span class="sxs-lookup"><span data-stu-id="61a31-107">EXAMPLES</span></span>

### <span data-ttu-id="61a31-108">예제 1: 응용 프로그램 게이트웨이 SKU 업데이트</span><span class="sxs-lookup"><span data-stu-id="61a31-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="61a31-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="61a31-110">두 번째 명령은 응용 프로그램 게이트웨이의 SKU를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="61a31-111">변수</span><span class="sxs-lookup"><span data-stu-id="61a31-111">PARAMETERS</span></span>

### <span data-ttu-id="61a31-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61a31-112">-ApplicationGateway</span></span>
<span data-ttu-id="61a31-113">이 cmdlet이 SKU를 연결 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="61a31-114">용량</span><span class="sxs-lookup"><span data-stu-id="61a31-114">-Capacity</span></span>
<span data-ttu-id="61a31-115">응용 프로그램 게이트웨이의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a31-116">-DefaultProfile</span></span>
<span data-ttu-id="61a31-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61a31-118">-이름</span><span class="sxs-lookup"><span data-stu-id="61a31-118">-Name</span></span>
<span data-ttu-id="61a31-119">Application gateway의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="61a31-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61a31-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="61a31-121">Standard_Small</span></span>
- <span data-ttu-id="61a31-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="61a31-122">Standard_Medium</span></span>
- <span data-ttu-id="61a31-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="61a31-123">Standard_Large</span></span>
- <span data-ttu-id="61a31-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="61a31-124">WAF_Medium</span></span>
- <span data-ttu-id="61a31-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="61a31-125">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a31-126">-티어</span><span class="sxs-lookup"><span data-stu-id="61a31-126">-Tier</span></span>
<span data-ttu-id="61a31-127">응용 프로그램 게이트웨이의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="61a31-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="61a31-129">표준이</span><span class="sxs-lookup"><span data-stu-id="61a31-129">Standard</span></span>
- <span data-ttu-id="61a31-130">WAF</span><span class="sxs-lookup"><span data-stu-id="61a31-130">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a31-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a31-131">CommonParameters</span></span>
<span data-ttu-id="61a31-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a31-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a31-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a31-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a31-134">입력</span><span class="sxs-lookup"><span data-stu-id="61a31-134">INPUTS</span></span>

### <span data-ttu-id="61a31-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="61a31-135">System.String</span></span>

## <span data-ttu-id="61a31-136">출력</span><span class="sxs-lookup"><span data-stu-id="61a31-136">OUTPUTS</span></span>

### <span data-ttu-id="61a31-137">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61a31-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="61a31-138">상속자</span><span class="sxs-lookup"><span data-stu-id="61a31-138">NOTES</span></span>

## <span data-ttu-id="61a31-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61a31-139">RELATED LINKS</span></span>

[<span data-ttu-id="61a31-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="61a31-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="61a31-141">새로운 AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="61a31-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


