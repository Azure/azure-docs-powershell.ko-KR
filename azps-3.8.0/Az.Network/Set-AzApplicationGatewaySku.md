---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877450"
---
# <span data-ttu-id="25b18-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="25b18-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="25b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25b18-102">SYNOPSIS</span></span>
<span data-ttu-id="25b18-103">응용 프로그램 게이트웨이의 SKU를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="25b18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25b18-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25b18-105">설명은</span><span class="sxs-lookup"><span data-stu-id="25b18-105">DESCRIPTION</span></span>
<span data-ttu-id="25b18-106">**AzApplicationGatewaySku** cmdlet은 응용 프로그램 게이트웨이의 SKU (stock 보관 단위)를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="25b18-107">예제의</span><span class="sxs-lookup"><span data-stu-id="25b18-107">EXAMPLES</span></span>

### <span data-ttu-id="25b18-108">예제 1: 응용 프로그램 게이트웨이 SKU 업데이트</span><span class="sxs-lookup"><span data-stu-id="25b18-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="25b18-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="25b18-110">두 번째 명령은 응용 프로그램 게이트웨이의 SKU를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="25b18-111">변수</span><span class="sxs-lookup"><span data-stu-id="25b18-111">PARAMETERS</span></span>

### <span data-ttu-id="25b18-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25b18-112">-ApplicationGateway</span></span>
<span data-ttu-id="25b18-113">이 cmdlet이 SKU를 연결 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="25b18-114">용량</span><span class="sxs-lookup"><span data-stu-id="25b18-114">-Capacity</span></span>
<span data-ttu-id="25b18-115">응용 프로그램 게이트웨이의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b18-116">-DefaultProfile</span></span>
<span data-ttu-id="25b18-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25b18-118">-이름</span><span class="sxs-lookup"><span data-stu-id="25b18-118">-Name</span></span>
<span data-ttu-id="25b18-119">Application gateway의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="25b18-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25b18-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="25b18-121">Standard_Small</span></span>
- <span data-ttu-id="25b18-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="25b18-122">Standard_Medium</span></span>
- <span data-ttu-id="25b18-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="25b18-123">Standard_Large</span></span>
- <span data-ttu-id="25b18-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="25b18-124">WAF_Medium</span></span>
- <span data-ttu-id="25b18-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="25b18-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b18-126">-티어</span><span class="sxs-lookup"><span data-stu-id="25b18-126">-Tier</span></span>
<span data-ttu-id="25b18-127">응용 프로그램 게이트웨이의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="25b18-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25b18-129">표준이</span><span class="sxs-lookup"><span data-stu-id="25b18-129">Standard</span></span>
- <span data-ttu-id="25b18-130">WAF</span><span class="sxs-lookup"><span data-stu-id="25b18-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b18-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b18-131">CommonParameters</span></span>
<span data-ttu-id="25b18-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25b18-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b18-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b18-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b18-134">입력</span><span class="sxs-lookup"><span data-stu-id="25b18-134">INPUTS</span></span>

### <span data-ttu-id="25b18-135">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25b18-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="25b18-136">출력</span><span class="sxs-lookup"><span data-stu-id="25b18-136">OUTPUTS</span></span>

### <span data-ttu-id="25b18-137">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="25b18-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="25b18-138">상속자</span><span class="sxs-lookup"><span data-stu-id="25b18-138">NOTES</span></span>

## <span data-ttu-id="25b18-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25b18-139">RELATED LINKS</span></span>

[<span data-ttu-id="25b18-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="25b18-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="25b18-141">새로운 AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="25b18-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


