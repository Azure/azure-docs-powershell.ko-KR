---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212591"
---
# <span data-ttu-id="27186-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="27186-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="27186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27186-102">SYNOPSIS</span></span>
<span data-ttu-id="27186-103">구독 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27186-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="27186-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27186-104">SYNTAX</span></span>

### <span data-ttu-id="27186-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="27186-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27186-106">단일</span><span class="sxs-lookup"><span data-stu-id="27186-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27186-107">설명은</span><span class="sxs-lookup"><span data-stu-id="27186-107">DESCRIPTION</span></span>
<span data-ttu-id="27186-108">**AzBillingPeriod** cmdlet은 구독 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27186-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="27186-109">예제의</span><span class="sxs-lookup"><span data-stu-id="27186-109">EXAMPLES</span></span>

### <span data-ttu-id="27186-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="27186-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="27186-111">구독에 사용 가능한 모든 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27186-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="27186-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="27186-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="27186-113">지정 된 이름을 사용 하 여 구독에 대 한 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27186-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="27186-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="27186-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="27186-115">구독에 대 한 최대 2 개의 청구 기간을 확보 합니다.</span><span class="sxs-lookup"><span data-stu-id="27186-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="27186-116">변수</span><span class="sxs-lookup"><span data-stu-id="27186-116">PARAMETERS</span></span>

### <span data-ttu-id="27186-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27186-117">-DefaultProfile</span></span>
<span data-ttu-id="27186-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="27186-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27186-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="27186-119">-MaxCount</span></span>
<span data-ttu-id="27186-120">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27186-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27186-121">-이름</span><span class="sxs-lookup"><span data-stu-id="27186-121">-Name</span></span>
<span data-ttu-id="27186-122">가져올 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27186-122">Name of a specific billing period to get.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27186-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27186-123">CommonParameters</span></span>
<span data-ttu-id="27186-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27186-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27186-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27186-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27186-126">입력</span><span class="sxs-lookup"><span data-stu-id="27186-126">INPUTS</span></span>

### <span data-ttu-id="27186-127">않아야</span><span class="sxs-lookup"><span data-stu-id="27186-127">None</span></span>

## <span data-ttu-id="27186-128">출력</span><span class="sxs-lookup"><span data-stu-id="27186-128">OUTPUTS</span></span>

### <span data-ttu-id="27186-129">PSBillingPeriod를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="27186-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="27186-130">상속자</span><span class="sxs-lookup"><span data-stu-id="27186-130">NOTES</span></span>

## <span data-ttu-id="27186-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27186-131">RELATED LINKS</span></span>
