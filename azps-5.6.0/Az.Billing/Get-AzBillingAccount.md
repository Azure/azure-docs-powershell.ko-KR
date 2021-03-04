---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959787"
---
# <span data-ttu-id="b3c4f-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="b3c4f-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="b3c4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c4f-103">청구 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-103">Get billing accounts.</span></span>

## <span data-ttu-id="b3c4f-104">구문</span><span class="sxs-lookup"><span data-stu-id="b3c4f-104">SYNTAX</span></span>

### <span data-ttu-id="b3c4f-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="b3c4f-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3c4f-106">Single</span><span class="sxs-lookup"><span data-stu-id="b3c4f-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3c4f-107">설명</span><span class="sxs-lookup"><span data-stu-id="b3c4f-107">DESCRIPTION</span></span>
<span data-ttu-id="b3c4f-108">**Get-AzBillingAccount** cmdlet은 청구 계정을 얻게 며, 사용자가 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="b3c4f-109">예제</span><span class="sxs-lookup"><span data-stu-id="b3c4f-109">EXAMPLES</span></span>

### <span data-ttu-id="b3c4f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b3c4f-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="b3c4f-111">사용자가 액세스할 수 있는 모든 청구 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="b3c4f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b3c4f-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="b3c4f-113">지정된 이름으로 청구 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="b3c4f-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="b3c4f-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="b3c4f-115">사용자가 액세스할 수 있는 모든 청구 계정을 얻게 하여 결과에 주소를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="b3c4f-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="b3c4f-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="b3c4f-117">사용자가 액세스할 수 있는 모든 청구 계정을 얻게 하여 결과에 청구 프로필을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="b3c4f-118">예제 5</span><span class="sxs-lookup"><span data-stu-id="b3c4f-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="b3c4f-119">사용자가 액세스할 수 있는 모든 청구 계정을 얻게 하여 결과에 청구 프로필 및 송장 섹션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="b3c4f-120">예제 6</span><span class="sxs-lookup"><span data-stu-id="b3c4f-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="b3c4f-121">지정된 이름으로 청구 계정을 얻게 하여 결과에 주소, 청구 프로필 및 송장 섹션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="b3c4f-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b3c4f-122">PARAMETERS</span></span>

### <span data-ttu-id="b3c4f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c4f-123">-DefaultProfile</span></span>
<span data-ttu-id="b3c4f-124">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b3c4f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3c4f-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="b3c4f-125">-IncludeAddress</span></span>
<span data-ttu-id="b3c4f-126">청구 계정의 주소를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="b3c4f-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="b3c4f-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="b3c4f-128">청구 계정 아래에 청구 프로필을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="b3c4f-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="b3c4f-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="b3c4f-130">청구 계정 아래에 청구 프로필 및 청구서 섹션을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="b3c4f-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b3c4f-131">-Name</span></span>
<span data-ttu-id="b3c4f-132">특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="b3c4f-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="b3c4f-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="b3c4f-134">구독을 만드는 데 입력으로 사용할 수 있는 청구 계정 아래에 청구 엔터티를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c4f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c4f-135">CommonParameters</span></span>
<span data-ttu-id="b3c4f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c4f-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b3c4f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c4f-138">입력</span><span class="sxs-lookup"><span data-stu-id="b3c4f-138">INPUTS</span></span>

### <span data-ttu-id="b3c4f-139">없음</span><span class="sxs-lookup"><span data-stu-id="b3c4f-139">None</span></span>

## <span data-ttu-id="b3c4f-140">출력</span><span class="sxs-lookup"><span data-stu-id="b3c4f-140">OUTPUTS</span></span>

### <span data-ttu-id="b3c4f-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="b3c4f-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="b3c4f-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b3c4f-142">NOTES</span></span>

## <span data-ttu-id="b3c4f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3c4f-143">RELATED LINKS</span></span>
