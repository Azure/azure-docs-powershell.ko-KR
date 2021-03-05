---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: f8c293870fa4eeb6f0df8a543473c8a9bda314c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012587"
---
# <span data-ttu-id="11e36-101">New-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="11e36-101">New-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="11e36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11e36-102">SYNOPSIS</span></span>
<span data-ttu-id="11e36-103">마켓플레이스 용어를 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-103">Accept marketplace terms.</span></span>

## <span data-ttu-id="11e36-104">구문</span><span class="sxs-lookup"><span data-stu-id="11e36-104">SYNTAX</span></span>

```
New-AzConfluentMarketplaceAgreement [-SubscriptionId <String>] [-Accepted] [-LicenseTextLink <String>]
 [-Plan <String>] [-PrivacyPolicyLink <String>] [-Product <String>] [-Publisher <String>]
 [-RetrieveDatetime <DateTime>] [-Signature <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="11e36-105">설명</span><span class="sxs-lookup"><span data-stu-id="11e36-105">DESCRIPTION</span></span>
<span data-ttu-id="11e36-106">마켓플레이스 용어를 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-106">Accept marketplace terms.</span></span>

## <span data-ttu-id="11e36-107">예제</span><span class="sxs-lookup"><span data-stu-id="11e36-107">EXAMPLES</span></span>

### <span data-ttu-id="11e36-108">예제 1: 구독에서 confluent Marketplace 계약 만들기</span><span class="sxs-lookup"><span data-stu-id="11e36-108">Example 1: Create confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> New-AzConfluentMarketplaceAgreement -Accepted

Name    Type
----    ----
default Microsoft.Confluent/agreement
```

<span data-ttu-id="11e36-109">이 명령은 구독 아래에서 confluent Marketplace 계약을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-109">This command create confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="11e36-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="11e36-110">PARAMETERS</span></span>

### <span data-ttu-id="11e36-111">-수락</span><span class="sxs-lookup"><span data-stu-id="11e36-111">-Accepted</span></span>
<span data-ttu-id="11e36-112">조건의 버전이 수락된 경우 그렇지 않으면 false입니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-112">If any version of the terms have been accepted, otherwise false.</span></span>

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

### <span data-ttu-id="11e36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e36-113">-DefaultProfile</span></span>
<span data-ttu-id="11e36-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-115">-LicenseTextLink</span><span class="sxs-lookup"><span data-stu-id="11e36-115">-LicenseTextLink</span></span>
<span data-ttu-id="11e36-116">Microsoft 및 Publisher 용어를 사용하여 HTML에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-116">Link to HTML with Microsoft and Publisher terms.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-117">-Plan</span><span class="sxs-lookup"><span data-stu-id="11e36-117">-Plan</span></span>
<span data-ttu-id="11e36-118">식별자 문자열을 계획합니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-118">Plan identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-119">-PrivacyPolicyLink</span><span class="sxs-lookup"><span data-stu-id="11e36-119">-PrivacyPolicyLink</span></span>
<span data-ttu-id="11e36-120">퍼블리셔의 개인 정보 취급 방침에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-120">Link to the privacy policy of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-121">-Product</span><span class="sxs-lookup"><span data-stu-id="11e36-121">-Product</span></span>
<span data-ttu-id="11e36-122">제품 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-122">Product identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="11e36-123">-Publisher</span></span>
<span data-ttu-id="11e36-124">게시자 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-124">Publisher identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-125">-RetrieveDatetime</span><span class="sxs-lookup"><span data-stu-id="11e36-125">-RetrieveDatetime</span></span>
<span data-ttu-id="11e36-126">약관이 수락된 날짜 및 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-126">Date and time in UTC of when the terms were accepted.</span></span>
<span data-ttu-id="11e36-127">수락이 false인 경우 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-127">This is empty if Accepted is false.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-128">-서명</span><span class="sxs-lookup"><span data-stu-id="11e36-128">-Signature</span></span>
<span data-ttu-id="11e36-129">용어 서명입니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-129">Terms signature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11e36-130">-SubscriptionId</span></span>
<span data-ttu-id="11e36-131">Microsoft Azure 구독 ID</span><span class="sxs-lookup"><span data-stu-id="11e36-131">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-132">-확인</span><span class="sxs-lookup"><span data-stu-id="11e36-132">-Confirm</span></span>
<span data-ttu-id="11e36-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e36-134">-WhatIf</span></span>
<span data-ttu-id="11e36-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e36-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e36-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e36-137">CommonParameters</span></span>
<span data-ttu-id="11e36-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11e36-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e36-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11e36-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e36-140">입력</span><span class="sxs-lookup"><span data-stu-id="11e36-140">INPUTS</span></span>

## <span data-ttu-id="11e36-141">출력</span><span class="sxs-lookup"><span data-stu-id="11e36-141">OUTPUTS</span></span>

### <span data-ttu-id="11e36-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="11e36-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="11e36-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11e36-143">NOTES</span></span>

<span data-ttu-id="11e36-144">별칭</span><span class="sxs-lookup"><span data-stu-id="11e36-144">ALIASES</span></span>

## <span data-ttu-id="11e36-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11e36-145">RELATED LINKS</span></span>

