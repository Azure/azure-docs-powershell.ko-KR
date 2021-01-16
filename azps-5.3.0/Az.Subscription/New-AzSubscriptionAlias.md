---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384217"
---
# <span data-ttu-id="9bf53-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="9bf53-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="9bf53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bf53-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf53-103">새 별칭 및 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9bf53-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="9bf53-104">구문</span><span class="sxs-lookup"><span data-stu-id="9bf53-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bf53-105">설명</span><span class="sxs-lookup"><span data-stu-id="9bf53-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf53-106">**New-AzSubscriptionAlias** cmdlet은 새 별칭 및 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9bf53-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="9bf53-107">예제</span><span class="sxs-lookup"><span data-stu-id="9bf53-107">EXAMPLES</span></span>

### <span data-ttu-id="9bf53-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9bf53-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="9bf53-109">새 별칭 및 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9bf53-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="9bf53-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bf53-110">PARAMETERS</span></span>

### <span data-ttu-id="9bf53-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="9bf53-111">-AliasName</span></span>
<span data-ttu-id="9bf53-112">구독에 대한 별칭</span><span class="sxs-lookup"><span data-stu-id="9bf53-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="9bf53-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bf53-113">-AsJob</span></span>
<span data-ttu-id="9bf53-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9bf53-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bf53-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="9bf53-115">-BillingScope</span></span>
<span data-ttu-id="9bf53-116">청구 범위</span><span class="sxs-lookup"><span data-stu-id="9bf53-116">Billing Scope</span></span>

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

### <span data-ttu-id="9bf53-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf53-117">-DefaultProfile</span></span>
<span data-ttu-id="9bf53-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9bf53-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf53-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="9bf53-119">-ResellerId</span></span>
<span data-ttu-id="9bf53-120">대리자 ID</span><span class="sxs-lookup"><span data-stu-id="9bf53-120">Reseller Id</span></span>

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

### <span data-ttu-id="9bf53-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9bf53-121">-SubscriptionId</span></span>
<span data-ttu-id="9bf53-122">기존 구독 ID</span><span class="sxs-lookup"><span data-stu-id="9bf53-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="9bf53-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9bf53-123">-SubscriptionName</span></span>
<span data-ttu-id="9bf53-124">구독의 이름</span><span class="sxs-lookup"><span data-stu-id="9bf53-124">Name of the subscription</span></span>

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

### <span data-ttu-id="9bf53-125">-Workload</span><span class="sxs-lookup"><span data-stu-id="9bf53-125">-Workload</span></span>
<span data-ttu-id="9bf53-126">워크로드 유형</span><span class="sxs-lookup"><span data-stu-id="9bf53-126">Type of Workload</span></span>

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

### <span data-ttu-id="9bf53-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bf53-127">-Confirm</span></span>
<span data-ttu-id="9bf53-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bf53-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf53-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf53-129">-WhatIf</span></span>
<span data-ttu-id="9bf53-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9bf53-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf53-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bf53-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf53-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf53-132">CommonParameters</span></span>
<span data-ttu-id="9bf53-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9bf53-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf53-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9bf53-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf53-135">입력</span><span class="sxs-lookup"><span data-stu-id="9bf53-135">INPUTS</span></span>

### <span data-ttu-id="9bf53-136">없음</span><span class="sxs-lookup"><span data-stu-id="9bf53-136">None</span></span>

## <span data-ttu-id="9bf53-137">출력</span><span class="sxs-lookup"><span data-stu-id="9bf53-137">OUTPUTS</span></span>

### <span data-ttu-id="9bf53-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9bf53-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="9bf53-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9bf53-139">NOTES</span></span>

## <span data-ttu-id="9bf53-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9bf53-140">RELATED LINKS</span></span>
