---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218425"
---
# <span data-ttu-id="716d3-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="716d3-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="716d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="716d3-102">SYNOPSIS</span></span>
<span data-ttu-id="716d3-103">청구 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="716d3-103">Get billing profiles.</span></span>

## <span data-ttu-id="716d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="716d3-104">SYNTAX</span></span>

### <span data-ttu-id="716d3-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="716d3-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="716d3-106">단일</span><span class="sxs-lookup"><span data-stu-id="716d3-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="716d3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="716d3-107">DESCRIPTION</span></span>
<span data-ttu-id="716d3-108">**AzBillingProfile** cmdlet은 지정 된 청구 계정 아래에 청구 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="716d3-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="716d3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="716d3-109">EXAMPLES</span></span>

### <span data-ttu-id="716d3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="716d3-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="716d3-111">지정 된 청구 계정으로 모든 청구 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="716d3-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="716d3-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="716d3-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="716d3-113">지정 된 이름을 사용 하 여 청구 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="716d3-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="716d3-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="716d3-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="716d3-115">모든 청구 프로필을 지정 된 청구 계정에서 가져오고, 결과에 송장 섹션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="716d3-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="716d3-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="716d3-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="716d3-117">지정 된 이름을 사용 하 여 청구 프로필을 가져오고, 결과에 송장 섹션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="716d3-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="716d3-118">변수</span><span class="sxs-lookup"><span data-stu-id="716d3-118">PARAMETERS</span></span>

### <span data-ttu-id="716d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716d3-119">-DefaultProfile</span></span>
<span data-ttu-id="716d3-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="716d3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="716d3-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="716d3-121">-BillingAccountName</span></span>
<span data-ttu-id="716d3-122">특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716d3-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="716d3-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="716d3-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="716d3-124">청구 프로필 아래에 송장 섹션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="716d3-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="716d3-125">-이름</span><span class="sxs-lookup"><span data-stu-id="716d3-125">-Name</span></span>
<span data-ttu-id="716d3-126">특정 청구 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="716d3-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="716d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716d3-127">CommonParameters</span></span>
<span data-ttu-id="716d3-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="716d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716d3-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="716d3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716d3-130">입력</span><span class="sxs-lookup"><span data-stu-id="716d3-130">INPUTS</span></span>

### <span data-ttu-id="716d3-131">않아야</span><span class="sxs-lookup"><span data-stu-id="716d3-131">None</span></span>

## <span data-ttu-id="716d3-132">출력</span><span class="sxs-lookup"><span data-stu-id="716d3-132">OUTPUTS</span></span>

### <span data-ttu-id="716d3-133">PSBillingProfile를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="716d3-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="716d3-134">상속자</span><span class="sxs-lookup"><span data-stu-id="716d3-134">NOTES</span></span>

## <span data-ttu-id="716d3-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="716d3-135">RELATED LINKS</span></span>
