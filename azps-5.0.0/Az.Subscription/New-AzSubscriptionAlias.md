---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226015"
---
# <span data-ttu-id="a979f-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="a979f-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="a979f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a979f-102">SYNOPSIS</span></span>
<span data-ttu-id="a979f-103">새 별칭 및 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="a979f-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="a979f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a979f-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a979f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a979f-105">DESCRIPTION</span></span>
<span data-ttu-id="a979f-106">**AzSubscriptionAlias** cmdlet은 새 별칭과 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a979f-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="a979f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a979f-107">EXAMPLES</span></span>

### <span data-ttu-id="a979f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a979f-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="a979f-109">새 별칭 및 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="a979f-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="a979f-110">변수</span><span class="sxs-lookup"><span data-stu-id="a979f-110">PARAMETERS</span></span>

### <span data-ttu-id="a979f-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="a979f-111">-AliasName</span></span>
<span data-ttu-id="a979f-112">구독에 대 한 별칭</span><span class="sxs-lookup"><span data-stu-id="a979f-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="a979f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a979f-113">-AsJob</span></span>
<span data-ttu-id="a979f-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a979f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a979f-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="a979f-115">-BillingScope</span></span>
<span data-ttu-id="a979f-116">청구 범위</span><span class="sxs-lookup"><span data-stu-id="a979f-116">Billing Scope</span></span>

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

### <span data-ttu-id="a979f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a979f-117">-DefaultProfile</span></span>
<span data-ttu-id="a979f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a979f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a979f-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="a979f-119">-ResellerId</span></span>
<span data-ttu-id="a979f-120">리셀러 Id</span><span class="sxs-lookup"><span data-stu-id="a979f-120">Reseller Id</span></span>

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

### <span data-ttu-id="a979f-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a979f-121">-SubscriptionId</span></span>
<span data-ttu-id="a979f-122">기존 구독 Id</span><span class="sxs-lookup"><span data-stu-id="a979f-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="a979f-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a979f-123">-SubscriptionName</span></span>
<span data-ttu-id="a979f-124">구독 이름</span><span class="sxs-lookup"><span data-stu-id="a979f-124">Name of the subscription</span></span>

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

### <span data-ttu-id="a979f-125">-작업 부하</span><span class="sxs-lookup"><span data-stu-id="a979f-125">-Workload</span></span>
<span data-ttu-id="a979f-126">작업 부하 유형</span><span class="sxs-lookup"><span data-stu-id="a979f-126">Type of Workload</span></span>

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

### <span data-ttu-id="a979f-127">-확인</span><span class="sxs-lookup"><span data-stu-id="a979f-127">-Confirm</span></span>
<span data-ttu-id="a979f-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a979f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a979f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a979f-129">-WhatIf</span></span>
<span data-ttu-id="a979f-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a979f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a979f-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a979f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a979f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a979f-132">CommonParameters</span></span>
<span data-ttu-id="a979f-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a979f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a979f-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a979f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a979f-135">입력</span><span class="sxs-lookup"><span data-stu-id="a979f-135">INPUTS</span></span>

### <span data-ttu-id="a979f-136">않아야</span><span class="sxs-lookup"><span data-stu-id="a979f-136">None</span></span>

## <span data-ttu-id="a979f-137">출력</span><span class="sxs-lookup"><span data-stu-id="a979f-137">OUTPUTS</span></span>

### <span data-ttu-id="a979f-138">PSAzureSubscription에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a979f-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="a979f-139">상속자</span><span class="sxs-lookup"><span data-stu-id="a979f-139">NOTES</span></span>

## <span data-ttu-id="a979f-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a979f-140">RELATED LINKS</span></span>
