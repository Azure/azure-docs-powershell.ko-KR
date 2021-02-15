---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189532"
---
# <span data-ttu-id="3610a-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3610a-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="3610a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3610a-102">SYNOPSIS</span></span>
<span data-ttu-id="3610a-103">애플리케이션 게이트웨이의 SKU를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3610a-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="3610a-104">구문</span><span class="sxs-lookup"><span data-stu-id="3610a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3610a-105">설명</span><span class="sxs-lookup"><span data-stu-id="3610a-105">DESCRIPTION</span></span>
<span data-ttu-id="3610a-106">**Set-AzApplicationGatewaySku** cmdlet은 애플리케이션 게이트웨이의 SKU(Stock Keeping Unit)를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3610a-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="3610a-107">예제</span><span class="sxs-lookup"><span data-stu-id="3610a-107">EXAMPLES</span></span>

### <span data-ttu-id="3610a-108">예제 1: 애플리케이션 게이트웨이 SKU 업데이트</span><span class="sxs-lookup"><span data-stu-id="3610a-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="3610a-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 사용하여 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3610a-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3610a-110">두 번째 명령은 애플리케이션 게이트웨이의 SKU를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3610a-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="3610a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3610a-111">PARAMETERS</span></span>

### <span data-ttu-id="3610a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3610a-112">-ApplicationGateway</span></span>
<span data-ttu-id="3610a-113">이 cmdlet이 SKU를 연결한 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3610a-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="3610a-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="3610a-114">-Capacity</span></span>
<span data-ttu-id="3610a-115">애플리케이션 게이트웨이의 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3610a-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="3610a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3610a-116">-DefaultProfile</span></span>
<span data-ttu-id="3610a-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3610a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3610a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3610a-118">-Name</span></span>
<span data-ttu-id="3610a-119">애플리케이션 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3610a-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="3610a-120">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="3610a-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3610a-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="3610a-121">Standard_Small</span></span>
- <span data-ttu-id="3610a-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="3610a-122">Standard_Medium</span></span>
- <span data-ttu-id="3610a-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="3610a-123">Standard_Large</span></span>
- <span data-ttu-id="3610a-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="3610a-124">WAF_Medium</span></span>
- <span data-ttu-id="3610a-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="3610a-125">WAF_Large</span></span>

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

### <span data-ttu-id="3610a-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="3610a-126">-Tier</span></span>
<span data-ttu-id="3610a-127">애플리케이션 게이트웨이의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3610a-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="3610a-128">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="3610a-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3610a-129">표준</span><span class="sxs-lookup"><span data-stu-id="3610a-129">Standard</span></span>
- <span data-ttu-id="3610a-130">WAF</span><span class="sxs-lookup"><span data-stu-id="3610a-130">WAF</span></span>

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

### <span data-ttu-id="3610a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3610a-131">CommonParameters</span></span>
<span data-ttu-id="3610a-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3610a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3610a-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3610a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3610a-134">입력</span><span class="sxs-lookup"><span data-stu-id="3610a-134">INPUTS</span></span>

### <span data-ttu-id="3610a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3610a-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3610a-136">출력</span><span class="sxs-lookup"><span data-stu-id="3610a-136">OUTPUTS</span></span>

### <span data-ttu-id="3610a-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3610a-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3610a-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3610a-138">NOTES</span></span>

## <span data-ttu-id="3610a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3610a-139">RELATED LINKS</span></span>

[<span data-ttu-id="3610a-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3610a-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="3610a-141">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3610a-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


