---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: eb1f0dadd905ff4b57a58c46f763f3c2dd51f256
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534888"
---
# <span data-ttu-id="a17ff-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a17ff-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="a17ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a17ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a17ff-103">응용 프로그램 게이트웨이에 대 한 SKU를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a17ff-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a17ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a17ff-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a17ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a17ff-105">DESCRIPTION</span></span>
<span data-ttu-id="a17ff-106">**AzureRmApplicationGatewaySku** Cmdlet은 Azure application gateway에 대 한 SKU (stock 보관 단위)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a17ff-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="a17ff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a17ff-107">EXAMPLES</span></span>

### <span data-ttu-id="a17ff-108">예제 1: Azure application gateway에 대 한 SKU 만들기</span><span class="sxs-lookup"><span data-stu-id="a17ff-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="a17ff-109">이 명령은 Azure application gateway에 대 한 Standard_Small 이라는 SKU를 만들고 그 결과를 $SKU 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a17ff-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="a17ff-110">변수</span><span class="sxs-lookup"><span data-stu-id="a17ff-110">PARAMETERS</span></span>

### <span data-ttu-id="a17ff-111">용량</span><span class="sxs-lookup"><span data-stu-id="a17ff-111">-Capacity</span></span>
<span data-ttu-id="a17ff-112">응용 프로그램 게이트웨이의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a17ff-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="a17ff-113">-이름</span><span class="sxs-lookup"><span data-stu-id="a17ff-113">-Name</span></span>
<span data-ttu-id="a17ff-114">SKU의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a17ff-114">Specifies the name of the SKU.</span></span>

<span data-ttu-id="a17ff-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a17ff-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a17ff-116">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="a17ff-116">Standard_Small</span></span>
- <span data-ttu-id="a17ff-117">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="a17ff-117">Standard_Medium</span></span>
- <span data-ttu-id="a17ff-118">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="a17ff-118">Standard_Large</span></span>
- <span data-ttu-id="a17ff-119">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="a17ff-119">WAF_Medium</span></span>
- <span data-ttu-id="a17ff-120">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="a17ff-120">WAF_Large</span></span>

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

### <span data-ttu-id="a17ff-121">-티어</span><span class="sxs-lookup"><span data-stu-id="a17ff-121">-Tier</span></span>
<span data-ttu-id="a17ff-122">SKU의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a17ff-122">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="a17ff-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a17ff-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a17ff-124">표준이</span><span class="sxs-lookup"><span data-stu-id="a17ff-124">Standard</span></span>
- <span data-ttu-id="a17ff-125">WAF</span><span class="sxs-lookup"><span data-stu-id="a17ff-125">WAF</span></span>

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

### <span data-ttu-id="a17ff-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a17ff-126">-DefaultProfile</span></span>
<span data-ttu-id="a17ff-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a17ff-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a17ff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a17ff-128">CommonParameters</span></span>
<span data-ttu-id="a17ff-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a17ff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a17ff-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a17ff-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a17ff-131">입력</span><span class="sxs-lookup"><span data-stu-id="a17ff-131">INPUTS</span></span>

### <span data-ttu-id="a17ff-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a17ff-132">System.String</span></span>

## <span data-ttu-id="a17ff-133">출력</span><span class="sxs-lookup"><span data-stu-id="a17ff-133">OUTPUTS</span></span>

### <span data-ttu-id="a17ff-134">Microsoft. \*. i m a. 모델. m i m m</span><span class="sxs-lookup"><span data-stu-id="a17ff-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="a17ff-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a17ff-135">NOTES</span></span>

## <span data-ttu-id="a17ff-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a17ff-136">RELATED LINKS</span></span>

[<span data-ttu-id="a17ff-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a17ff-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="a17ff-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="a17ff-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


