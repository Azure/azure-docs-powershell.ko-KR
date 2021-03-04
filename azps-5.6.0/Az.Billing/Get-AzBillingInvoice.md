---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 604109a80171ff4bb294dc1643081cd8e933d728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959755"
---
# <span data-ttu-id="50ee4-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="50ee4-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="50ee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="50ee4-103">구독의 청구 청구서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="50ee4-104">청구 계정 및 청구 프로필의 청구 송장 사용</span><span class="sxs-lookup"><span data-stu-id="50ee4-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="50ee4-105">구문</span><span class="sxs-lookup"><span data-stu-id="50ee4-105">SYNTAX</span></span>

### <span data-ttu-id="50ee4-106">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="50ee4-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="50ee4-107">최신</span><span class="sxs-lookup"><span data-stu-id="50ee4-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="50ee4-108">Single</span><span class="sxs-lookup"><span data-stu-id="50ee4-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50ee4-109">설명</span><span class="sxs-lookup"><span data-stu-id="50ee4-109">DESCRIPTION</span></span>
<span data-ttu-id="50ee4-110">**Get-AzBillingInvoice** cmdlet은 구독의 청구 청구서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="50ee4-111">예제</span><span class="sxs-lookup"><span data-stu-id="50ee4-111">EXAMPLES</span></span>

### <span data-ttu-id="50ee4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="50ee4-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="50ee4-113">구독의 최신 송장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="50ee4-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="50ee4-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="50ee4-115">지정된 이름으로 구독의 송장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="50ee4-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="50ee4-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="50ee4-117">다운로드 URL 없이 가장 최근 송장부터 시작하여 구독의 사용 가능한 모든 송장을 역순으로 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="50ee4-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="50ee4-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="50ee4-119">구독의 가장 최근 10개 송장을 다운로드하고 결과에 다운로드 URL을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="50ee4-120">예제 5</span><span class="sxs-lookup"><span data-stu-id="50ee4-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="50ee4-121">이름별 특정 송장을 구하고 결과에 다운로드 URL을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="50ee4-122">예제 6</span><span class="sxs-lookup"><span data-stu-id="50ee4-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="50ee4-123">청구 계정 이름으로 송장을 얻고 결과에 각 송장에 대한 다운로드 URL을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="50ee4-124">예제 7</span><span class="sxs-lookup"><span data-stu-id="50ee4-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="50ee4-125">송장 이름 및 청구 계정 이름으로 특정 송장을 구하고 결과에 각 송장에 대한 다운로드 URL을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="50ee4-126">예제 8</span><span class="sxs-lookup"><span data-stu-id="50ee4-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="50ee4-127">청구 계정 이름으로 최신 송장을 다운로드하고 결과에 송장에 대한 다운로드 URL을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="50ee4-128">예제 9</span><span class="sxs-lookup"><span data-stu-id="50ee4-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="50ee4-129">특정 청구 계정 및 특정 청구 프로필의 가장 최근 10개 청구서를 다운로드하고 결과에 다운로드 URL을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="50ee4-130">예제 10</span><span class="sxs-lookup"><span data-stu-id="50ee4-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="50ee4-131">청구 계정 이름 및 청구 프로필 이름을 사용하여 최신 송장을 다운로드하고 결과에 송장에 대한 다운로드 URL을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="50ee4-132">예제 10</span><span class="sxs-lookup"><span data-stu-id="50ee4-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="50ee4-133">perioStart 날짜 및 기간End date로 지정된 청구 기간에 대한 청구 계정 이름 및 청구 프로필 이름을 사용하여 청구서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="50ee4-134">매개 변수</span><span class="sxs-lookup"><span data-stu-id="50ee4-134">PARAMETERS</span></span>

### <span data-ttu-id="50ee4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ee4-135">-DefaultProfile</span></span>
<span data-ttu-id="50ee4-136">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="50ee4-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50ee4-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="50ee4-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="50ee4-138">송장의 다운로드 URL을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="50ee4-139">-Latest</span><span class="sxs-lookup"><span data-stu-id="50ee4-139">-Latest</span></span>
<span data-ttu-id="50ee4-140">최신 송장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="50ee4-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="50ee4-141">-MaxCount</span></span>
<span data-ttu-id="50ee4-142">반환할 레코드의 최대 수를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="50ee4-143">-Name</span><span class="sxs-lookup"><span data-stu-id="50ee4-143">-Name</span></span>
<span data-ttu-id="50ee4-144">구할 특정 송장의 이름 또는 지정하지 않은 경우 가장 최근의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="50ee4-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="50ee4-145">-BillingAccountName</span></span>
<span data-ttu-id="50ee4-146">송장을 받을 특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-146">Name of a specific billing account to get invoices for.</span></span>

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

### <span data-ttu-id="50ee4-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="50ee4-147">-BillingProfileName</span></span>
<span data-ttu-id="50ee4-148">송장을 받을 특정 청구 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-148">Name of a specific billing profile to get invoices for.</span></span>

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

### <span data-ttu-id="50ee4-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="50ee4-149">-PeriodStartDate</span></span>
<span data-ttu-id="50ee4-150">송장의 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-150">Start date for invoice.</span></span>

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

### <span data-ttu-id="50ee4-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="50ee4-151">-PeriodEndDate</span></span>
<span data-ttu-id="50ee4-152">송장의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-152">End date for invoice.</span></span>

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



### <span data-ttu-id="50ee4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ee4-153">CommonParameters</span></span>
<span data-ttu-id="50ee4-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50ee4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ee4-155">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="50ee4-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ee4-156">입력</span><span class="sxs-lookup"><span data-stu-id="50ee4-156">INPUTS</span></span>

### <span data-ttu-id="50ee4-157">없음</span><span class="sxs-lookup"><span data-stu-id="50ee4-157">None</span></span>

## <span data-ttu-id="50ee4-158">출력</span><span class="sxs-lookup"><span data-stu-id="50ee4-158">OUTPUTS</span></span>

### <span data-ttu-id="50ee4-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span><span class="sxs-lookup"><span data-stu-id="50ee4-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="50ee4-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50ee4-160">NOTES</span></span>

## <span data-ttu-id="50ee4-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50ee4-161">RELATED LINKS</span></span>
