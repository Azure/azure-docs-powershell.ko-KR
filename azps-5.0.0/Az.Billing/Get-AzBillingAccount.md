---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309681"
---
# <span data-ttu-id="a74ca-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="a74ca-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="a74ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a74ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a74ca-103">청구 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="a74ca-103">Get billing accounts.</span></span>

## <span data-ttu-id="a74ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a74ca-104">SYNTAX</span></span>

### <span data-ttu-id="a74ca-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a74ca-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a74ca-106">단일</span><span class="sxs-lookup"><span data-stu-id="a74ca-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a74ca-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a74ca-107">DESCRIPTION</span></span>
<span data-ttu-id="a74ca-108">**AzBillingAccount** cmdlet은 청구 계정을 가져오며, 사용자는 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="a74ca-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a74ca-109">EXAMPLES</span></span>

### <span data-ttu-id="a74ca-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a74ca-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="a74ca-111">모든 청구 계정에 대해 사용자가 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="a74ca-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a74ca-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="a74ca-113">지정 된 이름의 청구 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="a74ca-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="a74ca-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="a74ca-115">모든 청구 계정 사용자가 액세스 권한을 가지 며 결과에 주소를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="a74ca-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="a74ca-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="a74ca-117">모든 청구 계정 받기 사용자에 게 액세스 권한이 있고 결과에 청구 프로필을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="a74ca-118">예제 5</span><span class="sxs-lookup"><span data-stu-id="a74ca-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="a74ca-119">모든 청구 계정 받기 사용자가 액세스 권한을 가지 며 결과에 청구 프로필 및 송장 섹션을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="a74ca-120">예제 6</span><span class="sxs-lookup"><span data-stu-id="a74ca-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="a74ca-121">지정 된 이름을 사용 하 여 청구 계정을 가져오고 그 아래에 주소, 청구 프로필, 송장 섹션을 추가 하 여 결과를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="a74ca-122">변수</span><span class="sxs-lookup"><span data-stu-id="a74ca-122">PARAMETERS</span></span>

### <span data-ttu-id="a74ca-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74ca-123">-DefaultProfile</span></span>
<span data-ttu-id="a74ca-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a74ca-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a74ca-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="a74ca-125">-IncludeAddress</span></span>
<span data-ttu-id="a74ca-126">대금 청구 계정의 주소를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="a74ca-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="a74ca-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="a74ca-128">청구 계정 아래에 청구 프로필을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="a74ca-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="a74ca-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="a74ca-130">청구 계정 및 송장 아래에 청구 프로필을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="a74ca-131">-이름</span><span class="sxs-lookup"><span data-stu-id="a74ca-131">-Name</span></span>
<span data-ttu-id="a74ca-132">특정 청구 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="a74ca-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="a74ca-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="a74ca-134">구독 만들기에 대 한 입력으로 사용할 수 있는 청구 계정 아래에 청구 엔터티를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

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

### <span data-ttu-id="a74ca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74ca-135">CommonParameters</span></span>
<span data-ttu-id="a74ca-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a74ca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74ca-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a74ca-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74ca-138">입력</span><span class="sxs-lookup"><span data-stu-id="a74ca-138">INPUTS</span></span>

### <span data-ttu-id="a74ca-139">않아야</span><span class="sxs-lookup"><span data-stu-id="a74ca-139">None</span></span>

## <span data-ttu-id="a74ca-140">출력</span><span class="sxs-lookup"><span data-stu-id="a74ca-140">OUTPUTS</span></span>

### <span data-ttu-id="a74ca-141">PSBillingAccount를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="a74ca-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="a74ca-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a74ca-142">NOTES</span></span>

## <span data-ttu-id="a74ca-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a74ca-143">RELATED LINKS</span></span>
