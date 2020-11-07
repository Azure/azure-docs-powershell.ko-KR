---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 541306c8216168143e97bff84548e1c8e2a0ee47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689234"
---
# <span data-ttu-id="4ad69-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="4ad69-101">Set-AzContext</span></span>

## <span data-ttu-id="4ad69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ad69-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad69-103">Cmdlet에 대 한 테 넌 트, 구독 및 환경을 현재 세션에서 사용할 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="4ad69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ad69-104">SYNTAX</span></span>

### <span data-ttu-id="4ad69-105">Context (기본값)</span><span class="sxs-lookup"><span data-stu-id="4ad69-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ad69-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="4ad69-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ad69-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="4ad69-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ad69-108">구독</span><span class="sxs-lookup"><span data-stu-id="4ad69-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ad69-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="4ad69-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ad69-110">설명은</span><span class="sxs-lookup"><span data-stu-id="4ad69-110">DESCRIPTION</span></span>
<span data-ttu-id="4ad69-111">Set-AzContext cmdlet은 현재 세션에서 실행 하는 cmdlet에 대 한 인증 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="4ad69-112">컨텍스트에는 테 넌 트, 구독 및 환경 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="4ad69-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4ad69-113">EXAMPLES</span></span>

### <span data-ttu-id="4ad69-114">예제 1: 구독 컨텍스트 설정</span><span class="sxs-lookup"><span data-stu-id="4ad69-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="4ad69-115">이 명령은 지정 된 구독을 사용 하도록 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="4ad69-116">변수</span><span class="sxs-lookup"><span data-stu-id="4ad69-116">PARAMETERS</span></span>

### <span data-ttu-id="4ad69-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="4ad69-117">-Context</span></span>
<span data-ttu-id="4ad69-118">현재 세션에 대 한 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad69-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad69-119">-DefaultProfile</span></span>
<span data-ttu-id="4ad69-120">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ad69-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="4ad69-121">-ExtendedProperty</span></span>
<span data-ttu-id="4ad69-122">추가 컨텍스트 속성</span><span class="sxs-lookup"><span data-stu-id="4ad69-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad69-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4ad69-123">-Force</span></span>
<span data-ttu-id="4ad69-124">기존 컨텍스트를 같은 이름으로 덮어씁니다 (있는 경우).</span><span class="sxs-lookup"><span data-stu-id="4ad69-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="4ad69-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4ad69-125">-Name</span></span>
<span data-ttu-id="4ad69-126">컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="4ad69-126">Name of the context</span></span>

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

### <span data-ttu-id="4ad69-127">-범위</span><span class="sxs-lookup"><span data-stu-id="4ad69-127">-Scope</span></span>
<span data-ttu-id="4ad69-128">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad69-129">-구독</span><span class="sxs-lookup"><span data-stu-id="4ad69-129">-Subscription</span></span>
<span data-ttu-id="4ad69-130">컨텍스트를 설정 해야 하는 구독의 이름 또는 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="4ad69-131">이 매개 변수에는-SubscriptionName 및-SubscriptionId에 대 한 별칭이 있으므로 명확 하 게 하기 위해 각각 이름 및 id를 지정 하는 대신 구독을 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad69-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="4ad69-132">-SubscriptionObject</span></span>
<span data-ttu-id="4ad69-133">구독 개체</span><span class="sxs-lookup"><span data-stu-id="4ad69-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad69-134">-테 넌 트</span><span class="sxs-lookup"><span data-stu-id="4ad69-134">-Tenant</span></span>
<span data-ttu-id="4ad69-135">테 넌 트 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="4ad69-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad69-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="4ad69-136">-TenantObject</span></span>
<span data-ttu-id="4ad69-137">테 넌 트 개체</span><span class="sxs-lookup"><span data-stu-id="4ad69-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ad69-138">-확인</span><span class="sxs-lookup"><span data-stu-id="4ad69-138">-Confirm</span></span>
<span data-ttu-id="4ad69-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad69-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad69-140">-WhatIf</span></span>
<span data-ttu-id="4ad69-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ad69-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad69-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad69-143">CommonParameters</span></span>
<span data-ttu-id="4ad69-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad69-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad69-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad69-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad69-146">입력</span><span class="sxs-lookup"><span data-stu-id="4ad69-146">INPUTS</span></span>

### <span data-ttu-id="4ad69-147">Microsoft. Azure. a PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="4ad69-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="4ad69-148">PSAzureTenant (. \*)</span><span class="sxs-lookup"><span data-stu-id="4ad69-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="4ad69-149">PSAzureSubscription (. \*)</span><span class="sxs-lookup"><span data-stu-id="4ad69-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="4ad69-150">출력</span><span class="sxs-lookup"><span data-stu-id="4ad69-150">OUTPUTS</span></span>

### <span data-ttu-id="4ad69-151">Microsoft. Azure. a PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="4ad69-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="4ad69-152">상속자</span><span class="sxs-lookup"><span data-stu-id="4ad69-152">NOTES</span></span>

## <span data-ttu-id="4ad69-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ad69-153">RELATED LINKS</span></span>

[<span data-ttu-id="4ad69-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="4ad69-154">Get-AzContext</span></span>](./Get-AzContext.md)

