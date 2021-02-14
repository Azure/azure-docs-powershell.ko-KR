---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181988"
---
# <span data-ttu-id="dca2c-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="dca2c-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="dca2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca2c-102">SYNOPSIS</span></span>
<span data-ttu-id="dca2c-103">청구서 섹션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dca2c-103">Get invoice sections.</span></span>

## <span data-ttu-id="dca2c-104">구문</span><span class="sxs-lookup"><span data-stu-id="dca2c-104">SYNTAX</span></span>

### <span data-ttu-id="dca2c-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="dca2c-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dca2c-106">Single</span><span class="sxs-lookup"><span data-stu-id="dca2c-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dca2c-107">설명</span><span class="sxs-lookup"><span data-stu-id="dca2c-107">DESCRIPTION</span></span>
<span data-ttu-id="dca2c-108">**Get-AzInvoiceSection** cmdlet은 지정된 청구 프로필 아래에 청구서 섹션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dca2c-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="dca2c-109">예제</span><span class="sxs-lookup"><span data-stu-id="dca2c-109">EXAMPLES</span></span>

### <span data-ttu-id="dca2c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="dca2c-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="dca2c-111">지정된 청구 프로필에서 모든 청구서 섹션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dca2c-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="dca2c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="dca2c-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="dca2c-113">지정된 이름으로 송장 섹션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dca2c-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="dca2c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dca2c-114">PARAMETERS</span></span>

### <span data-ttu-id="dca2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca2c-115">-DefaultProfile</span></span>
<span data-ttu-id="dca2c-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dca2c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dca2c-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="dca2c-117">-BillingAccountName</span></span>
<span data-ttu-id="dca2c-118">특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dca2c-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="dca2c-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="dca2c-119">-BillingProfileName</span></span>
<span data-ttu-id="dca2c-120">특정 청구 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dca2c-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="dca2c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dca2c-121">-Name</span></span>
<span data-ttu-id="dca2c-122">특정 청구서 섹션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dca2c-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="dca2c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca2c-123">CommonParameters</span></span>
<span data-ttu-id="dca2c-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dca2c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca2c-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dca2c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca2c-126">입력</span><span class="sxs-lookup"><span data-stu-id="dca2c-126">INPUTS</span></span>

### <span data-ttu-id="dca2c-127">없음</span><span class="sxs-lookup"><span data-stu-id="dca2c-127">None</span></span>

## <span data-ttu-id="dca2c-128">출력</span><span class="sxs-lookup"><span data-stu-id="dca2c-128">OUTPUTS</span></span>

### <span data-ttu-id="dca2c-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="dca2c-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="dca2c-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dca2c-130">NOTES</span></span>

## <span data-ttu-id="dca2c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dca2c-131">RELATED LINKS</span></span>
