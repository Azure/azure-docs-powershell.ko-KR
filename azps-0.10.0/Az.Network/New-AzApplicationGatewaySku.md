---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 0b87119ccec521b85a210dc8685874bd4ba4b9ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875461"
---
# <span data-ttu-id="89030-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="89030-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="89030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89030-102">SYNOPSIS</span></span>
<span data-ttu-id="89030-103">응용 프로그램 게이트웨이에 대 한 SKU를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89030-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="89030-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89030-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89030-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89030-105">DESCRIPTION</span></span>
<span data-ttu-id="89030-106">**AzApplicationGatewaySku** Cmdlet은 Azure application gateway에 대 한 SKU (stock 보관 단위)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89030-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="89030-107">예제의</span><span class="sxs-lookup"><span data-stu-id="89030-107">EXAMPLES</span></span>

### <span data-ttu-id="89030-108">예제 1: Azure application gateway에 대 한 SKU 만들기</span><span class="sxs-lookup"><span data-stu-id="89030-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="89030-109">이 명령은 Azure application gateway에 대 한 Standard_Small 이라는 SKU를 만들고 그 결과를 $SKU 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="89030-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="89030-110">변수</span><span class="sxs-lookup"><span data-stu-id="89030-110">PARAMETERS</span></span>

### <span data-ttu-id="89030-111">용량</span><span class="sxs-lookup"><span data-stu-id="89030-111">-Capacity</span></span>
<span data-ttu-id="89030-112">응용 프로그램 게이트웨이의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89030-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="89030-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89030-113">-DefaultProfile</span></span>
<span data-ttu-id="89030-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89030-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89030-115">-이름</span><span class="sxs-lookup"><span data-stu-id="89030-115">-Name</span></span>
<span data-ttu-id="89030-116">SKU의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89030-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="89030-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="89030-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89030-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="89030-118">Standard_Small</span></span>
- <span data-ttu-id="89030-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="89030-119">Standard_Medium</span></span>
- <span data-ttu-id="89030-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="89030-120">Standard_Large</span></span>
- <span data-ttu-id="89030-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="89030-121">WAF_Medium</span></span>
- <span data-ttu-id="89030-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="89030-122">WAF_Large</span></span>

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

### <span data-ttu-id="89030-123">-티어</span><span class="sxs-lookup"><span data-stu-id="89030-123">-Tier</span></span>
<span data-ttu-id="89030-124">SKU의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89030-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="89030-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="89030-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89030-126">표준이</span><span class="sxs-lookup"><span data-stu-id="89030-126">Standard</span></span>
- <span data-ttu-id="89030-127">WAF</span><span class="sxs-lookup"><span data-stu-id="89030-127">WAF</span></span>

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

### <span data-ttu-id="89030-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89030-128">CommonParameters</span></span>
<span data-ttu-id="89030-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89030-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89030-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89030-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89030-131">입력</span><span class="sxs-lookup"><span data-stu-id="89030-131">INPUTS</span></span>

### <span data-ttu-id="89030-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89030-132">System.String</span></span>

## <span data-ttu-id="89030-133">출력</span><span class="sxs-lookup"><span data-stu-id="89030-133">OUTPUTS</span></span>

### <span data-ttu-id="89030-134">Microsoft. \*. i m a. 모델. m i m m</span><span class="sxs-lookup"><span data-stu-id="89030-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="89030-135">상속자</span><span class="sxs-lookup"><span data-stu-id="89030-135">NOTES</span></span>

## <span data-ttu-id="89030-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89030-136">RELATED LINKS</span></span>

[<span data-ttu-id="89030-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="89030-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="89030-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="89030-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


