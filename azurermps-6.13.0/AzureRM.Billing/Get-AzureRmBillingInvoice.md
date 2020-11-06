---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 1f21022294b1bcf5c75a7cf49dcc009600dc4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533427"
---
# <span data-ttu-id="1526a-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="1526a-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="1526a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1526a-102">SYNOPSIS</span></span>
<span data-ttu-id="1526a-103">플랜에 대 한 청구 청구서를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="1526a-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1526a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1526a-104">SYNTAX</span></span>

### <span data-ttu-id="1526a-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1526a-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1526a-106">비최신</span><span class="sxs-lookup"><span data-stu-id="1526a-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1526a-107">단일</span><span class="sxs-lookup"><span data-stu-id="1526a-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1526a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1526a-108">DESCRIPTION</span></span>
<span data-ttu-id="1526a-109">**AzureRmBillingInvoice** cmdlet은 구독의 청구 송장을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="1526a-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="1526a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1526a-110">EXAMPLES</span></span>

### <span data-ttu-id="1526a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1526a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="1526a-112">구독에 대 한 최신 송장을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="1526a-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="1526a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1526a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="1526a-114">지정 된 이름의 구독에 대 한 송장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1526a-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="1526a-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="1526a-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="1526a-116">구독에 대 한 모든 사용 가능한 송장을 다운로드 Url 없이 가장 최근의 송장부터 시작 하 여 역순으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1526a-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="1526a-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="1526a-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="1526a-118">구독에 대 한 최신 10 개의 송장을 받고 결과에 다운로드 Url을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="1526a-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="1526a-119">변수</span><span class="sxs-lookup"><span data-stu-id="1526a-119">PARAMETERS</span></span>

### <span data-ttu-id="1526a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1526a-120">-DefaultProfile</span></span>
<span data-ttu-id="1526a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1526a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1526a-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="1526a-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="1526a-123">송장의 다운로드 url을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1526a-123">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1526a-124">-최신 버전</span><span class="sxs-lookup"><span data-stu-id="1526a-124">-Latest</span></span>
<span data-ttu-id="1526a-125">최신 송장을 받으세요.</span><span class="sxs-lookup"><span data-stu-id="1526a-125">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1526a-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1526a-126">-MaxCount</span></span>
<span data-ttu-id="1526a-127">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1526a-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="1526a-128">-이름</span><span class="sxs-lookup"><span data-stu-id="1526a-128">-Name</span></span>
<span data-ttu-id="1526a-129">가져올 특정 송장의 이름 또는 가장 최근 if를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1526a-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="1526a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1526a-130">CommonParameters</span></span>
<span data-ttu-id="1526a-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1526a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1526a-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1526a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1526a-133">입력</span><span class="sxs-lookup"><span data-stu-id="1526a-133">INPUTS</span></span>

### <span data-ttu-id="1526a-134">않아야</span><span class="sxs-lookup"><span data-stu-id="1526a-134">None</span></span>

## <span data-ttu-id="1526a-135">출력</span><span class="sxs-lookup"><span data-stu-id="1526a-135">OUTPUTS</span></span>

### <span data-ttu-id="1526a-136">Microsoft. Azure. m a. 모델. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="1526a-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="1526a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="1526a-137">NOTES</span></span>

## <span data-ttu-id="1526a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1526a-138">RELATED LINKS</span></span>
