---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218417"
---
# <span data-ttu-id="67f79-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="67f79-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="67f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67f79-102">SYNOPSIS</span></span>
<span data-ttu-id="67f79-103">송장 섹션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67f79-103">Get invoice sections.</span></span>

## <span data-ttu-id="67f79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67f79-104">SYNTAX</span></span>

### <span data-ttu-id="67f79-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="67f79-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67f79-106">단일</span><span class="sxs-lookup"><span data-stu-id="67f79-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67f79-107">설명은</span><span class="sxs-lookup"><span data-stu-id="67f79-107">DESCRIPTION</span></span>
<span data-ttu-id="67f79-108">**AzInvoiceSection** cmdlet은 지정 된 청구 프로필 아래에 있는 송장 섹션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67f79-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="67f79-109">예제의</span><span class="sxs-lookup"><span data-stu-id="67f79-109">EXAMPLES</span></span>

### <span data-ttu-id="67f79-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="67f79-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="67f79-111">지정 된 청구 프로필의 모든 송장 섹션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67f79-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="67f79-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="67f79-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="67f79-113">지정 된 이름을 사용 하 여 송장 섹션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67f79-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="67f79-114">변수</span><span class="sxs-lookup"><span data-stu-id="67f79-114">PARAMETERS</span></span>

### <span data-ttu-id="67f79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f79-115">-DefaultProfile</span></span>
<span data-ttu-id="67f79-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67f79-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67f79-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="67f79-117">-BillingAccountName</span></span>
<span data-ttu-id="67f79-118">특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67f79-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="67f79-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="67f79-119">-BillingProfileName</span></span>
<span data-ttu-id="67f79-120">특정 청구 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67f79-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="67f79-121">-이름</span><span class="sxs-lookup"><span data-stu-id="67f79-121">-Name</span></span>
<span data-ttu-id="67f79-122">특정 송장 섹션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67f79-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="67f79-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f79-123">CommonParameters</span></span>
<span data-ttu-id="67f79-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f79-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f79-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f79-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f79-126">입력</span><span class="sxs-lookup"><span data-stu-id="67f79-126">INPUTS</span></span>

### <span data-ttu-id="67f79-127">않아야</span><span class="sxs-lookup"><span data-stu-id="67f79-127">None</span></span>

## <span data-ttu-id="67f79-128">출력</span><span class="sxs-lookup"><span data-stu-id="67f79-128">OUTPUTS</span></span>

### <span data-ttu-id="67f79-129">PSInvoiceSection를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="67f79-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="67f79-130">상속자</span><span class="sxs-lookup"><span data-stu-id="67f79-130">NOTES</span></span>

## <span data-ttu-id="67f79-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67f79-131">RELATED LINKS</span></span>
