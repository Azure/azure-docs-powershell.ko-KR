---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353882"
---
# <span data-ttu-id="55d0b-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="55d0b-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="55d0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="55d0b-103">구독의 청구 기간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="55d0b-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="55d0b-104">구문</span><span class="sxs-lookup"><span data-stu-id="55d0b-104">SYNTAX</span></span>

### <span data-ttu-id="55d0b-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="55d0b-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55d0b-106">Single</span><span class="sxs-lookup"><span data-stu-id="55d0b-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55d0b-107">설명</span><span class="sxs-lookup"><span data-stu-id="55d0b-107">DESCRIPTION</span></span>
<span data-ttu-id="55d0b-108">**Get-AzBillingPeriod** cmdlet은 구독의 청구 기간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="55d0b-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="55d0b-109">예제</span><span class="sxs-lookup"><span data-stu-id="55d0b-109">EXAMPLES</span></span>

### <span data-ttu-id="55d0b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="55d0b-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="55d0b-111">구독의 사용 가능한 모든 청구 기간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="55d0b-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="55d0b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="55d0b-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="55d0b-113">지정된 이름으로 구독의 청구 기간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="55d0b-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="55d0b-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="55d0b-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="55d0b-115">구독의 청구 기간을 2회까지 받을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55d0b-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="55d0b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55d0b-116">PARAMETERS</span></span>

### <span data-ttu-id="55d0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d0b-117">-DefaultProfile</span></span>
<span data-ttu-id="55d0b-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="55d0b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55d0b-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="55d0b-119">-MaxCount</span></span>
<span data-ttu-id="55d0b-120">반환할 레코드의 최대 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55d0b-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="55d0b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="55d0b-121">-Name</span></span>
<span data-ttu-id="55d0b-122">얻을 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55d0b-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="55d0b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d0b-123">CommonParameters</span></span>
<span data-ttu-id="55d0b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="55d0b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d0b-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="55d0b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d0b-126">입력</span><span class="sxs-lookup"><span data-stu-id="55d0b-126">INPUTS</span></span>

### <span data-ttu-id="55d0b-127">없음</span><span class="sxs-lookup"><span data-stu-id="55d0b-127">None</span></span>

## <span data-ttu-id="55d0b-128">출력</span><span class="sxs-lookup"><span data-stu-id="55d0b-128">OUTPUTS</span></span>

### <span data-ttu-id="55d0b-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="55d0b-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="55d0b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="55d0b-130">NOTES</span></span>

## <span data-ttu-id="55d0b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55d0b-131">RELATED LINKS</span></span>
