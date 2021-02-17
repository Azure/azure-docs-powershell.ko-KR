---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: dc39a7324f89e0a45efd4b631fb24a2e000d5e72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180577"
---
# <span data-ttu-id="da8b0-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="da8b0-101">New-AzHealthBot</span></span>

## <span data-ttu-id="da8b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="da8b0-103">새 HealthBot을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="da8b0-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="da8b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="da8b0-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da8b0-105">설명</span><span class="sxs-lookup"><span data-stu-id="da8b0-105">DESCRIPTION</span></span>
<span data-ttu-id="da8b0-106">새 HealthBot을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="da8b0-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="da8b0-107">예제</span><span class="sxs-lookup"><span data-stu-id="da8b0-107">EXAMPLES</span></span>

### <span data-ttu-id="da8b0-108">예제 1: 새 HealthBot 만들기</span><span class="sxs-lookup"><span data-stu-id="da8b0-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="da8b0-109">기본적으로 새 HealthBot 만들기</span><span class="sxs-lookup"><span data-stu-id="da8b0-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="da8b0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da8b0-110">PARAMETERS</span></span>

### <span data-ttu-id="da8b0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da8b0-111">-AsJob</span></span>
<span data-ttu-id="da8b0-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="da8b0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="da8b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8b0-113">-DefaultProfile</span></span>
<span data-ttu-id="da8b0-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da8b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da8b0-115">-Location</span><span class="sxs-lookup"><span data-stu-id="da8b0-115">-Location</span></span>
<span data-ttu-id="da8b0-116">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="da8b0-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="da8b0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="da8b0-117">-Name</span></span>
<span data-ttu-id="da8b0-118">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da8b0-118">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="da8b0-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="da8b0-119">-NoWait</span></span>
<span data-ttu-id="da8b0-120">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="da8b0-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="da8b0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da8b0-121">-ResourceGroupName</span></span>
<span data-ttu-id="da8b0-122">사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da8b0-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="da8b0-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="da8b0-123">-Sku</span></span>
<span data-ttu-id="da8b0-124">HealthBot SKU의 이름</span><span class="sxs-lookup"><span data-stu-id="da8b0-124">The name of the HealthBot SKU</span></span>

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

### <span data-ttu-id="da8b0-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da8b0-125">-SubscriptionId</span></span>
<span data-ttu-id="da8b0-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="da8b0-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="da8b0-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="da8b0-127">-Tag</span></span>
<span data-ttu-id="da8b0-128">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="da8b0-128">Resource tags.</span></span>

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

### <span data-ttu-id="da8b0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da8b0-129">-Confirm</span></span>
<span data-ttu-id="da8b0-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="da8b0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da8b0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da8b0-131">-WhatIf</span></span>
<span data-ttu-id="da8b0-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="da8b0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da8b0-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da8b0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da8b0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8b0-134">CommonParameters</span></span>
<span data-ttu-id="da8b0-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da8b0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8b0-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da8b0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8b0-137">입력</span><span class="sxs-lookup"><span data-stu-id="da8b0-137">INPUTS</span></span>

## <span data-ttu-id="da8b0-138">출력</span><span class="sxs-lookup"><span data-stu-id="da8b0-138">OUTPUTS</span></span>

### <span data-ttu-id="da8b0-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="da8b0-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="da8b0-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da8b0-140">NOTES</span></span>

<span data-ttu-id="da8b0-141">별칭</span><span class="sxs-lookup"><span data-stu-id="da8b0-141">ALIASES</span></span>

## <span data-ttu-id="da8b0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da8b0-142">RELATED LINKS</span></span>

