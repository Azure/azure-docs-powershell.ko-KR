---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: 6bf0b5a25772d430695737d70ff68cae5c5aa0d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013995"
---
# <span data-ttu-id="c542e-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="c542e-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="c542e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c542e-102">SYNOPSIS</span></span>
<span data-ttu-id="c542e-103">송장 섹션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c542e-103">Get invoice sections.</span></span>

## <span data-ttu-id="c542e-104">구문</span><span class="sxs-lookup"><span data-stu-id="c542e-104">SYNTAX</span></span>

### <span data-ttu-id="c542e-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="c542e-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c542e-106">Single</span><span class="sxs-lookup"><span data-stu-id="c542e-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c542e-107">설명</span><span class="sxs-lookup"><span data-stu-id="c542e-107">DESCRIPTION</span></span>
<span data-ttu-id="c542e-108">**Get-AzInvoiceSection** cmdlet은 지정된 청구 프로필 아래에 송장 섹션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c542e-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="c542e-109">예제</span><span class="sxs-lookup"><span data-stu-id="c542e-109">EXAMPLES</span></span>

### <span data-ttu-id="c542e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c542e-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="c542e-111">지정된 청구 프로필 아래에서 모든 송장 섹션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c542e-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="c542e-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="c542e-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="c542e-113">지정된 이름으로 송장 섹션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c542e-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="c542e-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c542e-114">PARAMETERS</span></span>

### <span data-ttu-id="c542e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c542e-115">-DefaultProfile</span></span>
<span data-ttu-id="c542e-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c542e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c542e-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="c542e-117">-BillingAccountName</span></span>
<span data-ttu-id="c542e-118">특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c542e-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="c542e-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="c542e-119">-BillingProfileName</span></span>
<span data-ttu-id="c542e-120">특정 청구 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c542e-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="c542e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c542e-121">-Name</span></span>
<span data-ttu-id="c542e-122">특정 송장 섹션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c542e-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="c542e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c542e-123">CommonParameters</span></span>
<span data-ttu-id="c542e-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c542e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c542e-125">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c542e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c542e-126">입력</span><span class="sxs-lookup"><span data-stu-id="c542e-126">INPUTS</span></span>

### <span data-ttu-id="c542e-127">없음</span><span class="sxs-lookup"><span data-stu-id="c542e-127">None</span></span>

## <span data-ttu-id="c542e-128">출력</span><span class="sxs-lookup"><span data-stu-id="c542e-128">OUTPUTS</span></span>

### <span data-ttu-id="c542e-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="c542e-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="c542e-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c542e-130">NOTES</span></span>

## <span data-ttu-id="c542e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c542e-131">RELATED LINKS</span></span>
