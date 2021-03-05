---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: b9c4e4cd55f81449497b0d397574c3eeec64d2d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013227"
---
# <span data-ttu-id="0d85e-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="0d85e-101">New-AzHealthBot</span></span>

## <span data-ttu-id="0d85e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d85e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d85e-103">새 HealthBot을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="0d85e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d85e-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d85e-105">설명</span><span class="sxs-lookup"><span data-stu-id="0d85e-105">DESCRIPTION</span></span>
<span data-ttu-id="0d85e-106">새 HealthBot을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="0d85e-107">예제</span><span class="sxs-lookup"><span data-stu-id="0d85e-107">EXAMPLES</span></span>

### <span data-ttu-id="0d85e-108">예제 1: 새 HealthBot 만들기</span><span class="sxs-lookup"><span data-stu-id="0d85e-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="0d85e-109">기본적으로 새 HealthBot 만들기</span><span class="sxs-lookup"><span data-stu-id="0d85e-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="0d85e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d85e-110">PARAMETERS</span></span>

### <span data-ttu-id="0d85e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d85e-111">-AsJob</span></span>
<span data-ttu-id="0d85e-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0d85e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d85e-113">-DefaultProfile</span></span>
<span data-ttu-id="0d85e-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d85e-115">-Location</span><span class="sxs-lookup"><span data-stu-id="0d85e-115">-Location</span></span>
<span data-ttu-id="0d85e-116">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="0d85e-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="0d85e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0d85e-117">-Name</span></span>
<span data-ttu-id="0d85e-118">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-118">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d85e-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0d85e-119">-NoWait</span></span>
<span data-ttu-id="0d85e-120">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="0d85e-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0d85e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d85e-121">-ResourceGroupName</span></span>
<span data-ttu-id="0d85e-122">사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="0d85e-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="0d85e-123">-Sku</span></span>
<span data-ttu-id="0d85e-124">HealthBot SKU의 이름</span><span class="sxs-lookup"><span data-stu-id="0d85e-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d85e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d85e-125">-SubscriptionId</span></span>
<span data-ttu-id="0d85e-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0d85e-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="0d85e-127">-Tag</span></span>
<span data-ttu-id="0d85e-128">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-128">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d85e-129">-확인</span><span class="sxs-lookup"><span data-stu-id="0d85e-129">-Confirm</span></span>
<span data-ttu-id="0d85e-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d85e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d85e-131">-WhatIf</span></span>
<span data-ttu-id="0d85e-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d85e-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d85e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d85e-134">CommonParameters</span></span>
<span data-ttu-id="0d85e-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d85e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d85e-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d85e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d85e-137">입력</span><span class="sxs-lookup"><span data-stu-id="0d85e-137">INPUTS</span></span>

## <span data-ttu-id="0d85e-138">출력</span><span class="sxs-lookup"><span data-stu-id="0d85e-138">OUTPUTS</span></span>

### <span data-ttu-id="0d85e-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="0d85e-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="0d85e-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d85e-140">NOTES</span></span>

<span data-ttu-id="0d85e-141">별칭</span><span class="sxs-lookup"><span data-stu-id="0d85e-141">ALIASES</span></span>

## <span data-ttu-id="0d85e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d85e-142">RELATED LINKS</span></span>

