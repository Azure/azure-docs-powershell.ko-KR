---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: b1680d18e11851718ca6d9d49acf4dc9501e1aad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530760"
---
# <span data-ttu-id="6e62e-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6e62e-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="6e62e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e62e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e62e-103">응용 프로그램 게이트웨이의 SKU를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e62e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e62e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e62e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6e62e-105">DESCRIPTION</span></span>
<span data-ttu-id="6e62e-106">**AzureRmApplicationGatewaySku** cmdlet은 응용 프로그램 게이트웨이의 SKU (stock 보관 단위)를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="6e62e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6e62e-107">EXAMPLES</span></span>

### <span data-ttu-id="6e62e-108">예제 1: 응용 프로그램 게이트웨이 SKU 업데이트</span><span class="sxs-lookup"><span data-stu-id="6e62e-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="6e62e-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="6e62e-110">두 번째 명령은 응용 프로그램 게이트웨이의 SKU를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="6e62e-111">변수</span><span class="sxs-lookup"><span data-stu-id="6e62e-111">PARAMETERS</span></span>

### <span data-ttu-id="6e62e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e62e-112">-ApplicationGateway</span></span>
<span data-ttu-id="6e62e-113">이 cmdlet이 SKU를 연결 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="6e62e-114">용량</span><span class="sxs-lookup"><span data-stu-id="6e62e-114">-Capacity</span></span>
<span data-ttu-id="6e62e-115">응용 프로그램 게이트웨이의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e62e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="6e62e-116">-Name</span></span>
<span data-ttu-id="6e62e-117">Application gateway의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-117">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="6e62e-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e62e-119">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="6e62e-119">Standard_Small</span></span>
- <span data-ttu-id="6e62e-120">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="6e62e-120">Standard_Medium</span></span>
- <span data-ttu-id="6e62e-121">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="6e62e-121">Standard_Large</span></span>
- <span data-ttu-id="6e62e-122">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="6e62e-122">WAF_Medium</span></span>
- <span data-ttu-id="6e62e-123">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="6e62e-123">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e62e-124">-티어</span><span class="sxs-lookup"><span data-stu-id="6e62e-124">-Tier</span></span>
<span data-ttu-id="6e62e-125">응용 프로그램 게이트웨이의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-125">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="6e62e-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e62e-127">표준이</span><span class="sxs-lookup"><span data-stu-id="6e62e-127">Standard</span></span>
- <span data-ttu-id="6e62e-128">WAF</span><span class="sxs-lookup"><span data-stu-id="6e62e-128">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e62e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e62e-129">-DefaultProfile</span></span>
<span data-ttu-id="6e62e-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e62e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e62e-131">CommonParameters</span></span>
<span data-ttu-id="6e62e-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e62e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e62e-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e62e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e62e-134">입력</span><span class="sxs-lookup"><span data-stu-id="6e62e-134">INPUTS</span></span>

### <span data-ttu-id="6e62e-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6e62e-135">System.String</span></span>

## <span data-ttu-id="6e62e-136">출력</span><span class="sxs-lookup"><span data-stu-id="6e62e-136">OUTPUTS</span></span>

### <span data-ttu-id="6e62e-137">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6e62e-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6e62e-138">상속자</span><span class="sxs-lookup"><span data-stu-id="6e62e-138">NOTES</span></span>

## <span data-ttu-id="6e62e-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e62e-139">RELATED LINKS</span></span>

[<span data-ttu-id="6e62e-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6e62e-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="6e62e-141">새로운 AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="6e62e-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


