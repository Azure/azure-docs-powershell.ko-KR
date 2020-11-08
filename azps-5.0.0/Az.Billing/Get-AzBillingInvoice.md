---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 2392b3275feeb6fa23f8f76dd3e76b6d97c33d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218429"
---
# <span data-ttu-id="2b1a9-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="2b1a9-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="2b1a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b1a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1a9-103">플랜에 대 한 청구 청구서를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="2b1a9-104">청구 계정 및 청구 프로필의 청구 송장 받기</span><span class="sxs-lookup"><span data-stu-id="2b1a9-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="2b1a9-105">구문과</span><span class="sxs-lookup"><span data-stu-id="2b1a9-105">SYNTAX</span></span>

### <span data-ttu-id="2b1a9-106">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b1a9-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="2b1a9-107">비최신</span><span class="sxs-lookup"><span data-stu-id="2b1a9-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="2b1a9-108">단일</span><span class="sxs-lookup"><span data-stu-id="2b1a9-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b1a9-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2b1a9-109">DESCRIPTION</span></span>
<span data-ttu-id="2b1a9-110">**AzBillingInvoice** cmdlet은 구독의 청구 송장을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="2b1a9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2b1a9-111">EXAMPLES</span></span>

### <span data-ttu-id="2b1a9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b1a9-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="2b1a9-113">구독에 대 한 최신 송장을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="2b1a9-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="2b1a9-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="2b1a9-115">지정 된 이름의 구독에 대 한 송장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="2b1a9-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="2b1a9-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="2b1a9-117">구독에 대 한 모든 사용 가능한 송장을 다운로드 Url 없이 가장 최근의 송장부터 시작 하 여 역순으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="2b1a9-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="2b1a9-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="2b1a9-119">구독에 대 한 최신 10 개의 송장을 받고 결과에 다운로드 Url을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="2b1a9-120">예제 5</span><span class="sxs-lookup"><span data-stu-id="2b1a9-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="2b1a9-121">특정 송장을 이름으로 가져오고 다운로드 url을 결과에 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="2b1a9-122">예제 6</span><span class="sxs-lookup"><span data-stu-id="2b1a9-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="2b1a9-123">청구 계정 이름으로 송장을 가져오고 결과에 각 송장의 다운로드 url을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="2b1a9-124">예제 7</span><span class="sxs-lookup"><span data-stu-id="2b1a9-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="2b1a9-125">송장 이름과 청구 계정 이름으로 특정 송장을 받고 결과에 각 송장에 대 한 다운로드 url을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="2b1a9-126">예제 8</span><span class="sxs-lookup"><span data-stu-id="2b1a9-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="2b1a9-127">청구 계정 이름과 송장에 따라 최신 송장을 얻고 결과에 송장의 다운로드 url을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="2b1a9-128">예제 9</span><span class="sxs-lookup"><span data-stu-id="2b1a9-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="2b1a9-129">특정 청구 계정 및 특정 청구 프로필의 최근 10 개 송장을 얻고 결과에 다운로드 Url을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="2b1a9-130">예제 10</span><span class="sxs-lookup"><span data-stu-id="2b1a9-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="2b1a9-131">청구 계정 이름과 대금 청구 프로필 이름을 기준으로 최신 송장을 가져오고 송장에 대 한 다운로드 url을 결과에 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="2b1a9-132">예제 10</span><span class="sxs-lookup"><span data-stu-id="2b1a9-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="2b1a9-133">PerioStart date 및 periodEnd date로 지정 된 청구 기간에 대 한 청구 계정 이름 및 청구 프로필 이름을 기준으로 송장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="2b1a9-134">변수</span><span class="sxs-lookup"><span data-stu-id="2b1a9-134">PARAMETERS</span></span>

### <span data-ttu-id="2b1a9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1a9-135">-DefaultProfile</span></span>
<span data-ttu-id="2b1a9-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2b1a9-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b1a9-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="2b1a9-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="2b1a9-138">송장의 다운로드 url을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-138">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1a9-139">-최신 버전</span><span class="sxs-lookup"><span data-stu-id="2b1a9-139">-Latest</span></span>
<span data-ttu-id="2b1a9-140">최신 송장을 받으세요.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="2b1a9-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2b1a9-141">-MaxCount</span></span>
<span data-ttu-id="2b1a9-142">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="2b1a9-143">-이름</span><span class="sxs-lookup"><span data-stu-id="2b1a9-143">-Name</span></span>
<span data-ttu-id="2b1a9-144">가져올 특정 송장의 이름 또는 가장 최근 if를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="2b1a9-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="2b1a9-145">-BillingAccountName</span></span>
<span data-ttu-id="2b1a9-146">송장을 받을 특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1a9-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="2b1a9-147">-BillingProfileName</span></span>
<span data-ttu-id="2b1a9-148">송장을 받을 특정 청구 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1a9-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="2b1a9-149">-PeriodStartDate</span></span>
<span data-ttu-id="2b1a9-150">송장의 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1a9-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="2b1a9-151">-PeriodEndDate</span></span>
<span data-ttu-id="2b1a9-152">송장 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="2b1a9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1a9-153">CommonParameters</span></span>
<span data-ttu-id="2b1a9-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1a9-155">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b1a9-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1a9-156">입력</span><span class="sxs-lookup"><span data-stu-id="2b1a9-156">INPUTS</span></span>

### <span data-ttu-id="2b1a9-157">않아야</span><span class="sxs-lookup"><span data-stu-id="2b1a9-157">None</span></span>

## <span data-ttu-id="2b1a9-158">출력</span><span class="sxs-lookup"><span data-stu-id="2b1a9-158">OUTPUTS</span></span>

### <span data-ttu-id="2b1a9-159">Microsoft. Azure. m a. 모델. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="2b1a9-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="2b1a9-160">상속자</span><span class="sxs-lookup"><span data-stu-id="2b1a9-160">NOTES</span></span>

## <span data-ttu-id="2b1a9-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b1a9-161">RELATED LINKS</span></span>
