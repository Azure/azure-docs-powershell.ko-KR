---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358842"
---
# <span data-ttu-id="2f77b-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2f77b-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="2f77b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f77b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f77b-103">애플리케이션 게이트웨이에 대한 SKU를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f77b-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="2f77b-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f77b-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f77b-105">설명</span><span class="sxs-lookup"><span data-stu-id="2f77b-105">DESCRIPTION</span></span>
<span data-ttu-id="2f77b-106">**New-AzApplicationGatewaySku** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 SKU(Stock Keeping Unit)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f77b-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="2f77b-107">예제</span><span class="sxs-lookup"><span data-stu-id="2f77b-107">EXAMPLES</span></span>

### <span data-ttu-id="2f77b-108">예제 1: Azure 애플리케이션 게이트웨이에 대한 SKU 만들기</span><span class="sxs-lookup"><span data-stu-id="2f77b-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="2f77b-109">이 명령은 Azure 애플리케이션 Standard_Small 대한 이름의 SKU를 만들고 결과를 azure application gateway라는 이름의 변수에 $SKU.</span><span class="sxs-lookup"><span data-stu-id="2f77b-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="2f77b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f77b-110">PARAMETERS</span></span>

### <span data-ttu-id="2f77b-111">-Capacity</span><span class="sxs-lookup"><span data-stu-id="2f77b-111">-Capacity</span></span>
<span data-ttu-id="2f77b-112">애플리케이션 게이트웨이의 인스턴스 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f77b-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="2f77b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f77b-113">-DefaultProfile</span></span>
<span data-ttu-id="2f77b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f77b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f77b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2f77b-115">-Name</span></span>
<span data-ttu-id="2f77b-116">SKU의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f77b-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="2f77b-117">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="2f77b-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f77b-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="2f77b-118">Standard_Small</span></span>
- <span data-ttu-id="2f77b-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="2f77b-119">Standard_Medium</span></span>
- <span data-ttu-id="2f77b-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="2f77b-120">Standard_Large</span></span>
- <span data-ttu-id="2f77b-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="2f77b-121">WAF_Medium</span></span>
- <span data-ttu-id="2f77b-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="2f77b-122">WAF_Large</span></span>
- <span data-ttu-id="2f77b-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="2f77b-123">Standard_v2</span></span>
- <span data-ttu-id="2f77b-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="2f77b-124">WAF_v2</span></span>

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

### <span data-ttu-id="2f77b-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="2f77b-125">-Tier</span></span>
<span data-ttu-id="2f77b-126">SKU의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f77b-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="2f77b-127">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="2f77b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f77b-128">표준</span><span class="sxs-lookup"><span data-stu-id="2f77b-128">Standard</span></span>
- <span data-ttu-id="2f77b-129">WAF</span><span class="sxs-lookup"><span data-stu-id="2f77b-129">WAF</span></span>
- <span data-ttu-id="2f77b-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="2f77b-130">Standard_v2</span></span>
- <span data-ttu-id="2f77b-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="2f77b-131">WAF_v2</span></span>

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

### <span data-ttu-id="2f77b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f77b-132">CommonParameters</span></span>
<span data-ttu-id="2f77b-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f77b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f77b-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2f77b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f77b-135">입력</span><span class="sxs-lookup"><span data-stu-id="2f77b-135">INPUTS</span></span>

### <span data-ttu-id="2f77b-136">없음</span><span class="sxs-lookup"><span data-stu-id="2f77b-136">None</span></span>

## <span data-ttu-id="2f77b-137">출력</span><span class="sxs-lookup"><span data-stu-id="2f77b-137">OUTPUTS</span></span>

### <span data-ttu-id="2f77b-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2f77b-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="2f77b-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f77b-139">NOTES</span></span>

## <span data-ttu-id="2f77b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f77b-140">RELATED LINKS</span></span>

[<span data-ttu-id="2f77b-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2f77b-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="2f77b-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="2f77b-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


