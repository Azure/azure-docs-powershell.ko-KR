---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: cda4281b1bf52b9f0b94926bc66590d1bd741c44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881001"
---
# <span data-ttu-id="5e296-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5e296-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="5e296-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e296-102">SYNOPSIS</span></span>
<span data-ttu-id="5e296-103">응용 프로그램 게이트웨이에 대 한 SKU를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e296-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e296-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e296-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e296-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5e296-105">DESCRIPTION</span></span>
<span data-ttu-id="5e296-106">**AzureRmApplicationGatewaySku** Cmdlet은 Azure application gateway에 대 한 SKU (stock 보관 단위)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e296-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="5e296-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5e296-107">EXAMPLES</span></span>

### <span data-ttu-id="5e296-108">예제 1: Azure application gateway에 대 한 SKU 만들기</span><span class="sxs-lookup"><span data-stu-id="5e296-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="5e296-109">이 명령은 Azure application gateway에 대 한 Standard_Small 이라는 SKU를 만들고 그 결과를 $SKU 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e296-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="5e296-110">변수</span><span class="sxs-lookup"><span data-stu-id="5e296-110">PARAMETERS</span></span>

### <span data-ttu-id="5e296-111">용량</span><span class="sxs-lookup"><span data-stu-id="5e296-111">-Capacity</span></span>
<span data-ttu-id="5e296-112">응용 프로그램 게이트웨이의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e296-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="5e296-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e296-113">-DefaultProfile</span></span>
<span data-ttu-id="5e296-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e296-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e296-115">-이름</span><span class="sxs-lookup"><span data-stu-id="5e296-115">-Name</span></span>
<span data-ttu-id="5e296-116">SKU의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e296-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="5e296-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e296-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e296-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="5e296-118">Standard_Small</span></span>
- <span data-ttu-id="5e296-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="5e296-119">Standard_Medium</span></span>
- <span data-ttu-id="5e296-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="5e296-120">Standard_Large</span></span>
- <span data-ttu-id="5e296-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="5e296-121">WAF_Medium</span></span>
- <span data-ttu-id="5e296-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="5e296-122">WAF_Large</span></span>

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

### <span data-ttu-id="5e296-123">-티어</span><span class="sxs-lookup"><span data-stu-id="5e296-123">-Tier</span></span>
<span data-ttu-id="5e296-124">SKU의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e296-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="5e296-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5e296-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e296-126">표준이</span><span class="sxs-lookup"><span data-stu-id="5e296-126">Standard</span></span>
- <span data-ttu-id="5e296-127">WAF</span><span class="sxs-lookup"><span data-stu-id="5e296-127">WAF</span></span>

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

### <span data-ttu-id="5e296-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e296-128">CommonParameters</span></span>
<span data-ttu-id="5e296-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e296-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e296-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e296-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e296-131">입력</span><span class="sxs-lookup"><span data-stu-id="5e296-131">INPUTS</span></span>

### <span data-ttu-id="5e296-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5e296-132">System.String</span></span>

## <span data-ttu-id="5e296-133">출력</span><span class="sxs-lookup"><span data-stu-id="5e296-133">OUTPUTS</span></span>

### <span data-ttu-id="5e296-134">Microsoft. \*. i m a. 모델. m i m m</span><span class="sxs-lookup"><span data-stu-id="5e296-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="5e296-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5e296-135">NOTES</span></span>

## <span data-ttu-id="5e296-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e296-136">RELATED LINKS</span></span>

[<span data-ttu-id="5e296-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5e296-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="5e296-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="5e296-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


