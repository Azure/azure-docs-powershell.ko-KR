---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 30c90d4b04c6c32144946cbdf98c59991133dbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015824"
---
# <span data-ttu-id="f24c8-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="f24c8-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="f24c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f24c8-102">SYNOPSIS</span></span>
<span data-ttu-id="f24c8-103">새 별칭 및 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f24c8-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="f24c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="f24c8-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f24c8-105">설명</span><span class="sxs-lookup"><span data-stu-id="f24c8-105">DESCRIPTION</span></span>
<span data-ttu-id="f24c8-106">**New-AzSubscriptionAlias** cmdlet은 새 별칭 및 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f24c8-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="f24c8-107">예제</span><span class="sxs-lookup"><span data-stu-id="f24c8-107">EXAMPLES</span></span>

### <span data-ttu-id="f24c8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f24c8-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="f24c8-109">새 별칭 및 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f24c8-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="f24c8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f24c8-110">PARAMETERS</span></span>

### <span data-ttu-id="f24c8-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="f24c8-111">-AliasName</span></span>
<span data-ttu-id="f24c8-112">구독의 별칭</span><span class="sxs-lookup"><span data-stu-id="f24c8-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="f24c8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f24c8-113">-AsJob</span></span>
<span data-ttu-id="f24c8-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f24c8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f24c8-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="f24c8-115">-BillingScope</span></span>
<span data-ttu-id="f24c8-116">청구 범위</span><span class="sxs-lookup"><span data-stu-id="f24c8-116">Billing Scope</span></span>

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

### <span data-ttu-id="f24c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f24c8-117">-DefaultProfile</span></span>
<span data-ttu-id="f24c8-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f24c8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f24c8-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="f24c8-119">-ResellerId</span></span>
<span data-ttu-id="f24c8-120">리셀러 ID</span><span class="sxs-lookup"><span data-stu-id="f24c8-120">Reseller Id</span></span>

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

### <span data-ttu-id="f24c8-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f24c8-121">-SubscriptionId</span></span>
<span data-ttu-id="f24c8-122">기존 구독 ID</span><span class="sxs-lookup"><span data-stu-id="f24c8-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="f24c8-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f24c8-123">-SubscriptionName</span></span>
<span data-ttu-id="f24c8-124">구독 이름</span><span class="sxs-lookup"><span data-stu-id="f24c8-124">Name of the subscription</span></span>

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

### <span data-ttu-id="f24c8-125">-워크로드</span><span class="sxs-lookup"><span data-stu-id="f24c8-125">-Workload</span></span>
<span data-ttu-id="f24c8-126">워크로드 유형</span><span class="sxs-lookup"><span data-stu-id="f24c8-126">Type of Workload</span></span>

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

### <span data-ttu-id="f24c8-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f24c8-127">-Confirm</span></span>
<span data-ttu-id="f24c8-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f24c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f24c8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f24c8-129">-WhatIf</span></span>
<span data-ttu-id="f24c8-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f24c8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f24c8-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f24c8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f24c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f24c8-132">CommonParameters</span></span>
<span data-ttu-id="f24c8-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f24c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f24c8-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f24c8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f24c8-135">입력</span><span class="sxs-lookup"><span data-stu-id="f24c8-135">INPUTS</span></span>

### <span data-ttu-id="f24c8-136">없음</span><span class="sxs-lookup"><span data-stu-id="f24c8-136">None</span></span>

## <span data-ttu-id="f24c8-137">출력</span><span class="sxs-lookup"><span data-stu-id="f24c8-137">OUTPUTS</span></span>

### <span data-ttu-id="f24c8-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f24c8-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="f24c8-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f24c8-139">NOTES</span></span>

## <span data-ttu-id="f24c8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f24c8-140">RELATED LINKS</span></span>
