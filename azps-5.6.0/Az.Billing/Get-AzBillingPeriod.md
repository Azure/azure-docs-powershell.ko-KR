---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: d2a859740d2e5627eca3ca0748aab8e72c1ee9af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990453"
---
# <span data-ttu-id="6ea89-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="6ea89-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="6ea89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ea89-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea89-103">구독의 청구 기간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea89-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="6ea89-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ea89-104">SYNTAX</span></span>

### <span data-ttu-id="6ea89-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="6ea89-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ea89-106">Single</span><span class="sxs-lookup"><span data-stu-id="6ea89-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ea89-107">설명</span><span class="sxs-lookup"><span data-stu-id="6ea89-107">DESCRIPTION</span></span>
<span data-ttu-id="6ea89-108">**Get-AzBillingPeriod** cmdlet은 구독의 청구 기간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea89-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="6ea89-109">예제</span><span class="sxs-lookup"><span data-stu-id="6ea89-109">EXAMPLES</span></span>

### <span data-ttu-id="6ea89-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ea89-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="6ea89-111">구독의 사용 가능한 모든 청구 기간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea89-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="6ea89-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="6ea89-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="6ea89-113">지정된 이름으로 구독의 청구 기간을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea89-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="6ea89-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="6ea89-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="6ea89-115">구독의 청구 기간은 2회입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea89-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="6ea89-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6ea89-116">PARAMETERS</span></span>

### <span data-ttu-id="6ea89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea89-117">-DefaultProfile</span></span>
<span data-ttu-id="6ea89-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6ea89-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ea89-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6ea89-119">-MaxCount</span></span>
<span data-ttu-id="6ea89-120">반환할 레코드의 최대 수를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea89-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="6ea89-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6ea89-121">-Name</span></span>
<span data-ttu-id="6ea89-122">받을 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea89-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="6ea89-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea89-123">CommonParameters</span></span>
<span data-ttu-id="6ea89-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea89-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea89-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6ea89-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea89-126">입력</span><span class="sxs-lookup"><span data-stu-id="6ea89-126">INPUTS</span></span>

### <span data-ttu-id="6ea89-127">없음</span><span class="sxs-lookup"><span data-stu-id="6ea89-127">None</span></span>

## <span data-ttu-id="6ea89-128">출력</span><span class="sxs-lookup"><span data-stu-id="6ea89-128">OUTPUTS</span></span>

### <span data-ttu-id="6ea89-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="6ea89-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="6ea89-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ea89-130">NOTES</span></span>

## <span data-ttu-id="6ea89-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ea89-131">RELATED LINKS</span></span>
