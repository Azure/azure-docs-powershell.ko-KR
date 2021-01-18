---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494048"
---
# <span data-ttu-id="54dc6-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="54dc6-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="54dc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="54dc6-103">청구 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54dc6-103">Get billing profiles.</span></span>

## <span data-ttu-id="54dc6-104">구문</span><span class="sxs-lookup"><span data-stu-id="54dc6-104">SYNTAX</span></span>

### <span data-ttu-id="54dc6-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="54dc6-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54dc6-106">Single</span><span class="sxs-lookup"><span data-stu-id="54dc6-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54dc6-107">설명</span><span class="sxs-lookup"><span data-stu-id="54dc6-107">DESCRIPTION</span></span>
<span data-ttu-id="54dc6-108">**Get-AzBillingProfile** cmdlet은 지정된 청구 계정에서 청구 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54dc6-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="54dc6-109">예제</span><span class="sxs-lookup"><span data-stu-id="54dc6-109">EXAMPLES</span></span>

### <span data-ttu-id="54dc6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="54dc6-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="54dc6-111">지정된 청구 계정에서 모든 청구 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54dc6-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="54dc6-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="54dc6-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="54dc6-113">지정된 이름으로 청구 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54dc6-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="54dc6-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="54dc6-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="54dc6-115">지정된 청구 계정에서 모든 청구 프로필을 얻을 수 있으며 결과에 청구서 섹션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="54dc6-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="54dc6-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="54dc6-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="54dc6-117">지정된 이름으로 청구 프로필을 얻고 결과에 청구서 섹션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="54dc6-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="54dc6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54dc6-118">PARAMETERS</span></span>

### <span data-ttu-id="54dc6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54dc6-119">-DefaultProfile</span></span>
<span data-ttu-id="54dc6-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="54dc6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54dc6-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="54dc6-121">-BillingAccountName</span></span>
<span data-ttu-id="54dc6-122">특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54dc6-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="54dc6-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="54dc6-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="54dc6-124">청구 프로필 아래에 청구서 섹션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="54dc6-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="54dc6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="54dc6-125">-Name</span></span>
<span data-ttu-id="54dc6-126">특정 청구 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54dc6-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="54dc6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54dc6-127">CommonParameters</span></span>
<span data-ttu-id="54dc6-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="54dc6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54dc6-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="54dc6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54dc6-130">입력</span><span class="sxs-lookup"><span data-stu-id="54dc6-130">INPUTS</span></span>

### <span data-ttu-id="54dc6-131">없음</span><span class="sxs-lookup"><span data-stu-id="54dc6-131">None</span></span>

## <span data-ttu-id="54dc6-132">출력</span><span class="sxs-lookup"><span data-stu-id="54dc6-132">OUTPUTS</span></span>

### <span data-ttu-id="54dc6-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="54dc6-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="54dc6-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="54dc6-134">NOTES</span></span>

## <span data-ttu-id="54dc6-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54dc6-135">RELATED LINKS</span></span>
