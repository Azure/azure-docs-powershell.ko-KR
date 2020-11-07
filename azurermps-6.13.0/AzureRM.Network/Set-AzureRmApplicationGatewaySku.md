---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 487a3cd096f1d27852f4472d478977ac0cbe2ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711039"
---
# <span data-ttu-id="eae06-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="eae06-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="eae06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eae06-102">SYNOPSIS</span></span>
<span data-ttu-id="eae06-103">응용 프로그램 게이트웨이의 SKU를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eae06-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eae06-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eae06-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eae06-105">DESCRIPTION</span></span>
<span data-ttu-id="eae06-106">**AzureRmApplicationGatewaySku** cmdlet은 응용 프로그램 게이트웨이의 SKU (stock 보관 단위)를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="eae06-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eae06-107">EXAMPLES</span></span>

### <span data-ttu-id="eae06-108">예제 1: 응용 프로그램 게이트웨이 SKU 업데이트</span><span class="sxs-lookup"><span data-stu-id="eae06-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="eae06-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eae06-110">두 번째 명령은 응용 프로그램 게이트웨이의 SKU를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="eae06-111">변수</span><span class="sxs-lookup"><span data-stu-id="eae06-111">PARAMETERS</span></span>

### <span data-ttu-id="eae06-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eae06-112">-ApplicationGateway</span></span>
<span data-ttu-id="eae06-113">이 cmdlet이 SKU를 연결 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="eae06-114">용량</span><span class="sxs-lookup"><span data-stu-id="eae06-114">-Capacity</span></span>
<span data-ttu-id="eae06-115">응용 프로그램 게이트웨이의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="eae06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eae06-116">-DefaultProfile</span></span>
<span data-ttu-id="eae06-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eae06-118">-이름</span><span class="sxs-lookup"><span data-stu-id="eae06-118">-Name</span></span>
<span data-ttu-id="eae06-119">Application gateway의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="eae06-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eae06-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="eae06-121">Standard_Small</span></span>
- <span data-ttu-id="eae06-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="eae06-122">Standard_Medium</span></span>
- <span data-ttu-id="eae06-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="eae06-123">Standard_Large</span></span>
- <span data-ttu-id="eae06-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="eae06-124">WAF_Medium</span></span>
- <span data-ttu-id="eae06-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="eae06-125">WAF_Large</span></span>

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

### <span data-ttu-id="eae06-126">-티어</span><span class="sxs-lookup"><span data-stu-id="eae06-126">-Tier</span></span>
<span data-ttu-id="eae06-127">응용 프로그램 게이트웨이의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="eae06-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eae06-129">표준이</span><span class="sxs-lookup"><span data-stu-id="eae06-129">Standard</span></span>
- <span data-ttu-id="eae06-130">WAF</span><span class="sxs-lookup"><span data-stu-id="eae06-130">WAF</span></span>

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

### <span data-ttu-id="eae06-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eae06-131">CommonParameters</span></span>
<span data-ttu-id="eae06-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eae06-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eae06-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eae06-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eae06-134">입력</span><span class="sxs-lookup"><span data-stu-id="eae06-134">INPUTS</span></span>

### <span data-ttu-id="eae06-135">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eae06-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="eae06-136">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eae06-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="eae06-137">출력</span><span class="sxs-lookup"><span data-stu-id="eae06-137">OUTPUTS</span></span>

### <span data-ttu-id="eae06-138">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eae06-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eae06-139">상속자</span><span class="sxs-lookup"><span data-stu-id="eae06-139">NOTES</span></span>

## <span data-ttu-id="eae06-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eae06-140">RELATED LINKS</span></span>

[<span data-ttu-id="eae06-141">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="eae06-141">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="eae06-142">새로운 AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="eae06-142">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


