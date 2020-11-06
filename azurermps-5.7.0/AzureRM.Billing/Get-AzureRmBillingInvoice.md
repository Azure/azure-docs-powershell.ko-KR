---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 5a6ccf36f8e7aecdca4d6560614e9185a5ca26b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527055"
---
# <span data-ttu-id="86cbc-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="86cbc-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="86cbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="86cbc-103">플랜에 대 한 청구 청구서를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="86cbc-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86cbc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86cbc-104">SYNTAX</span></span>

### <span data-ttu-id="86cbc-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="86cbc-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86cbc-106">비최신</span><span class="sxs-lookup"><span data-stu-id="86cbc-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86cbc-107">단일</span><span class="sxs-lookup"><span data-stu-id="86cbc-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86cbc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="86cbc-108">DESCRIPTION</span></span>
<span data-ttu-id="86cbc-109">**AzureRmBillingInvoice** cmdlet은 구독의 청구 송장을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="86cbc-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="86cbc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="86cbc-110">EXAMPLES</span></span>

### <span data-ttu-id="86cbc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="86cbc-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="86cbc-112">구독에 대 한 최신 송장을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="86cbc-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="86cbc-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="86cbc-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="86cbc-114">지정 된 이름의 구독에 대 한 송장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86cbc-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="86cbc-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="86cbc-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="86cbc-116">구독에 대 한 모든 사용 가능한 송장을 다운로드 Url 없이 가장 최근의 송장부터 시작 하 여 역순으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86cbc-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="86cbc-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="86cbc-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="86cbc-118">구독에 대 한 최신 10 개의 송장을 받고 결과에 다운로드 Url을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="86cbc-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="86cbc-119">변수</span><span class="sxs-lookup"><span data-stu-id="86cbc-119">PARAMETERS</span></span>

### <span data-ttu-id="86cbc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86cbc-120">-DefaultProfile</span></span>
<span data-ttu-id="86cbc-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="86cbc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86cbc-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="86cbc-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="86cbc-123">송장의 다운로드 url을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="86cbc-123">Generate the download url of the invoices.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86cbc-124">-최신 버전</span><span class="sxs-lookup"><span data-stu-id="86cbc-124">-Latest</span></span>
<span data-ttu-id="86cbc-125">최신 송장을 받으세요.</span><span class="sxs-lookup"><span data-stu-id="86cbc-125">Get the latest invoice.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86cbc-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="86cbc-126">-MaxCount</span></span>
<span data-ttu-id="86cbc-127">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86cbc-127">Determines the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86cbc-128">-이름</span><span class="sxs-lookup"><span data-stu-id="86cbc-128">-Name</span></span>
<span data-ttu-id="86cbc-129">가져올 특정 송장의 이름 또는 가장 최근 if를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86cbc-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="86cbc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86cbc-130">CommonParameters</span></span>
<span data-ttu-id="86cbc-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86cbc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86cbc-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86cbc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86cbc-133">입력</span><span class="sxs-lookup"><span data-stu-id="86cbc-133">INPUTS</span></span>

### <span data-ttu-id="86cbc-134">않아야</span><span class="sxs-lookup"><span data-stu-id="86cbc-134">None</span></span>

## <span data-ttu-id="86cbc-135">출력</span><span class="sxs-lookup"><span data-stu-id="86cbc-135">OUTPUTS</span></span>

### <span data-ttu-id="86cbc-136">System.webserver. List ' 1 [[Microsoft. e-경영진. 청구. 청구서, 버전 = 0.14.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="86cbc-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Billing.Models.Invoice, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="86cbc-137">Microsoft. Azure. 청구. 송장</span><span class="sxs-lookup"><span data-stu-id="86cbc-137">Microsoft.Azure.Management.Billing.Models.Invoice</span></span>

## <span data-ttu-id="86cbc-138">상속자</span><span class="sxs-lookup"><span data-stu-id="86cbc-138">NOTES</span></span>

## <span data-ttu-id="86cbc-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86cbc-139">RELATED LINKS</span></span>

