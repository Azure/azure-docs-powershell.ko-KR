---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: f6b75a1c161515ee45571ba3db6d2f84b95af967
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528268"
---
# <span data-ttu-id="137b1-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="137b1-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="137b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="137b1-102">SYNOPSIS</span></span>
<span data-ttu-id="137b1-103">구독 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="137b1-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="137b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="137b1-104">SYNTAX</span></span>

### <span data-ttu-id="137b1-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="137b1-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="137b1-106">단일</span><span class="sxs-lookup"><span data-stu-id="137b1-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="137b1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="137b1-107">DESCRIPTION</span></span>
<span data-ttu-id="137b1-108">**AzureRmBillingPeriod** cmdlet은 구독 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="137b1-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="137b1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="137b1-109">EXAMPLES</span></span>

### <span data-ttu-id="137b1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="137b1-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="137b1-111">구독에 사용 가능한 모든 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="137b1-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="137b1-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="137b1-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="137b1-113">지정 된 이름을 사용 하 여 구독에 대 한 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="137b1-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="137b1-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="137b1-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="137b1-115">구독에 대 한 최대 2 개의 청구 기간을 확보 합니다.</span><span class="sxs-lookup"><span data-stu-id="137b1-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="137b1-116">변수</span><span class="sxs-lookup"><span data-stu-id="137b1-116">PARAMETERS</span></span>

### <span data-ttu-id="137b1-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="137b1-117">-MaxCount</span></span>
<span data-ttu-id="137b1-118">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="137b1-118">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="137b1-119">-이름</span><span class="sxs-lookup"><span data-stu-id="137b1-119">-Name</span></span>
<span data-ttu-id="137b1-120">가져올 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="137b1-120">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="137b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="137b1-121">-DefaultProfile</span></span>
<span data-ttu-id="137b1-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="137b1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="137b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="137b1-123">CommonParameters</span></span>
<span data-ttu-id="137b1-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="137b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="137b1-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="137b1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="137b1-126">입력</span><span class="sxs-lookup"><span data-stu-id="137b1-126">INPUTS</span></span>

### <span data-ttu-id="137b1-127">않아야</span><span class="sxs-lookup"><span data-stu-id="137b1-127">None</span></span>

## <span data-ttu-id="137b1-128">출력</span><span class="sxs-lookup"><span data-stu-id="137b1-128">OUTPUTS</span></span>

### <span data-ttu-id="137b1-129">System.webserver. List ' 1 [[Microsoft PSBillingPeriod, Microsoft Azure. 0.12.0.0, Version =, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="137b1-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod, Microsoft.Azure.Commands.Billing, Version=0.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="137b1-130">PSBillingPeriod를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="137b1-130">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="137b1-131">상속자</span><span class="sxs-lookup"><span data-stu-id="137b1-131">NOTES</span></span>

## <span data-ttu-id="137b1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="137b1-132">RELATED LINKS</span></span>

