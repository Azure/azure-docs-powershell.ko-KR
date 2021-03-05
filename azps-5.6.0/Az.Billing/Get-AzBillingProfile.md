---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: c66b3a2c4c151daf0a5d3df62aaaf248a7d2e338
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986216"
---
# <span data-ttu-id="aab1b-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="aab1b-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="aab1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aab1b-102">SYNOPSIS</span></span>
<span data-ttu-id="aab1b-103">청구 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1b-103">Get billing profiles.</span></span>

## <span data-ttu-id="aab1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="aab1b-104">SYNTAX</span></span>

### <span data-ttu-id="aab1b-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="aab1b-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aab1b-106">Single</span><span class="sxs-lookup"><span data-stu-id="aab1b-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aab1b-107">설명</span><span class="sxs-lookup"><span data-stu-id="aab1b-107">DESCRIPTION</span></span>
<span data-ttu-id="aab1b-108">**Get-AzBillingProfile** cmdlet은 지정된 청구 계정 아래에서 청구 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1b-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="aab1b-109">예제</span><span class="sxs-lookup"><span data-stu-id="aab1b-109">EXAMPLES</span></span>

### <span data-ttu-id="aab1b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="aab1b-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="aab1b-111">지정된 청구 계정에서 모든 청구 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1b-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="aab1b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="aab1b-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="aab1b-113">지정된 이름으로 청구 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aab1b-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="aab1b-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="aab1b-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="aab1b-115">지정된 청구 계정에서 모든 청구 프로필을 얻고 결과에 송장 섹션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1b-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="aab1b-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="aab1b-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="aab1b-117">지정된 이름으로 청구 프로필을 얻고 결과에 송장 섹션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1b-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="aab1b-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aab1b-118">PARAMETERS</span></span>

### <span data-ttu-id="aab1b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab1b-119">-DefaultProfile</span></span>
<span data-ttu-id="aab1b-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aab1b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aab1b-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="aab1b-121">-BillingAccountName</span></span>
<span data-ttu-id="aab1b-122">특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aab1b-122">Name of the specific billing account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aab1b-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="aab1b-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="aab1b-124">청구 프로필 아래에 송장 섹션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1b-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="aab1b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="aab1b-125">-Name</span></span>
<span data-ttu-id="aab1b-126">특정 청구 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aab1b-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="aab1b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab1b-127">CommonParameters</span></span>
<span data-ttu-id="aab1b-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aab1b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab1b-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="aab1b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab1b-130">입력</span><span class="sxs-lookup"><span data-stu-id="aab1b-130">INPUTS</span></span>

### <span data-ttu-id="aab1b-131">없음</span><span class="sxs-lookup"><span data-stu-id="aab1b-131">None</span></span>

## <span data-ttu-id="aab1b-132">출력</span><span class="sxs-lookup"><span data-stu-id="aab1b-132">OUTPUTS</span></span>

### <span data-ttu-id="aab1b-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="aab1b-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="aab1b-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aab1b-134">NOTES</span></span>

## <span data-ttu-id="aab1b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aab1b-135">RELATED LINKS</span></span>
