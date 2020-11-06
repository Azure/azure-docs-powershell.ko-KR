---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 4714b97773583197807d6ca54152ee25ab520909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529742"
---
# <span data-ttu-id="4a1e1-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="4a1e1-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="4a1e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1e1-103">사용 가능한 예약 카탈로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="4a1e1-103">Get the catalog of available reservation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a1e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a1e1-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="4a1e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4a1e1-105">DESCRIPTION</span></span>
<span data-ttu-id="4a1e1-106">지정 된 Azure 구독에 대해 예약 된 인스턴스 구입에 사용할 수 있는 지역 및 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a1e1-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="4a1e1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4a1e1-107">EXAMPLES</span></span>

### <span data-ttu-id="4a1e1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a1e1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog
```

<span data-ttu-id="4a1e1-109">기본 구독에 대 한 카탈로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="4a1e1-109">Get the catalog for the default subscription</span></span>

### <span data-ttu-id="4a1e1-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="4a1e1-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="4a1e1-111">지정 된 구독에 대 한 카탈로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="4a1e1-111">Get the catalog for the specified subscription</span></span>

## <span data-ttu-id="4a1e1-112">변수</span><span class="sxs-lookup"><span data-stu-id="4a1e1-112">PARAMETERS</span></span>

### <span data-ttu-id="4a1e1-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a1e1-113">-SubscriptionId</span></span>
<span data-ttu-id="4a1e1-114">구독 Id</span><span class="sxs-lookup"><span data-stu-id="4a1e1-114">Id of the subscription</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a1e1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1e1-115">CommonParameters</span></span>
<span data-ttu-id="4a1e1-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a1e1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1e1-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a1e1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1e1-118">입력</span><span class="sxs-lookup"><span data-stu-id="4a1e1-118">INPUTS</span></span>

### <span data-ttu-id="4a1e1-119">않아야</span><span class="sxs-lookup"><span data-stu-id="4a1e1-119">None</span></span>

## <span data-ttu-id="4a1e1-120">출력</span><span class="sxs-lookup"><span data-stu-id="4a1e1-120">OUTPUTS</span></span>

### <span data-ttu-id="4a1e1-121">System.webserver. List ' 1 [[PSCatalog, Microsoft azure. Commands. 예약, 버전 = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4a1e1-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSCatalog, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4a1e1-122">상속자</span><span class="sxs-lookup"><span data-stu-id="4a1e1-122">NOTES</span></span>

## <span data-ttu-id="4a1e1-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a1e1-123">RELATED LINKS</span></span>

