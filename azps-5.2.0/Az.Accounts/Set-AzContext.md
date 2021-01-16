---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: f7d6c1fcfe4a74601a8a27e85bd1520912b26350
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331425"
---
# <span data-ttu-id="83274-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="83274-101">Set-AzContext</span></span>

## <span data-ttu-id="83274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83274-102">SYNOPSIS</span></span>
<span data-ttu-id="83274-103">cmdlet이 현재 세션에서 사용할 테넌트, 구독 및 환경을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="83274-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="83274-104">구문</span><span class="sxs-lookup"><span data-stu-id="83274-104">SYNTAX</span></span>

### <span data-ttu-id="83274-105">컨텍스트(기본값)</span><span class="sxs-lookup"><span data-stu-id="83274-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83274-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="83274-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83274-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="83274-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83274-108">구독</span><span class="sxs-lookup"><span data-stu-id="83274-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83274-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="83274-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83274-110">설명</span><span class="sxs-lookup"><span data-stu-id="83274-110">DESCRIPTION</span></span>
<span data-ttu-id="83274-111">이 Set-AzContext cmdlet은 현재 세션에서 실행되는 cmdlet에 대한 인증 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="83274-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="83274-112">컨텍스트에는 테넌트, 구독 및 환경 정보가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="83274-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="83274-113">예제</span><span class="sxs-lookup"><span data-stu-id="83274-113">EXAMPLES</span></span>

### <span data-ttu-id="83274-114">예제 1: 구독 컨텍스트 설정</span><span class="sxs-lookup"><span data-stu-id="83274-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="83274-115">이 명령은 지정된 구독을 사용할 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="83274-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="83274-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83274-116">PARAMETERS</span></span>

### <span data-ttu-id="83274-117">-Context</span><span class="sxs-lookup"><span data-stu-id="83274-117">-Context</span></span>
<span data-ttu-id="83274-118">현재 세션에 대한 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83274-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="83274-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83274-119">-DefaultProfile</span></span>
<span data-ttu-id="83274-120">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83274-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83274-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="83274-121">-ExtendedProperty</span></span>
<span data-ttu-id="83274-122">추가 컨텍스트 속성</span><span class="sxs-lookup"><span data-stu-id="83274-122">Additional context properties</span></span>

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

### <span data-ttu-id="83274-123">-Force</span><span class="sxs-lookup"><span data-stu-id="83274-123">-Force</span></span>
<span data-ttu-id="83274-124">기존 컨텍스트를 동일한 이름(있는 경우)으로 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="83274-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="83274-125">-Name</span><span class="sxs-lookup"><span data-stu-id="83274-125">-Name</span></span>
<span data-ttu-id="83274-126">컨텍스트의 이름</span><span class="sxs-lookup"><span data-stu-id="83274-126">Name of the context</span></span>

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

### <span data-ttu-id="83274-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="83274-127">-Scope</span></span>
<span data-ttu-id="83274-128">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="83274-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="83274-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="83274-129">-Subscription</span></span>
<span data-ttu-id="83274-130">컨텍스트를 설정해야 하는 구독의 이름 또는 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="83274-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="83274-131">이 매개 변수에는 -SubscriptionName 및 -SubscriptionId에 대한 별칭이 있으므로 명확성을 위해 각각 이름 및 ID를 지정할 때 -Subscription 대신 이러한 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83274-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="83274-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="83274-132">-SubscriptionObject</span></span>
<span data-ttu-id="83274-133">구독 개체</span><span class="sxs-lookup"><span data-stu-id="83274-133">A subscription object</span></span>

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

### <span data-ttu-id="83274-134">-Tenant</span><span class="sxs-lookup"><span data-stu-id="83274-134">-Tenant</span></span>
<span data-ttu-id="83274-135">테넌트 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="83274-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="83274-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="83274-136">-TenantObject</span></span>
<span data-ttu-id="83274-137">테넌트 개체</span><span class="sxs-lookup"><span data-stu-id="83274-137">A Tenant Object</span></span>

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

### <span data-ttu-id="83274-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83274-138">-Confirm</span></span>
<span data-ttu-id="83274-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="83274-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83274-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83274-140">-WhatIf</span></span>
<span data-ttu-id="83274-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="83274-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83274-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83274-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83274-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83274-143">CommonParameters</span></span>
<span data-ttu-id="83274-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83274-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83274-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="83274-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83274-146">입력</span><span class="sxs-lookup"><span data-stu-id="83274-146">INPUTS</span></span>

### <span data-ttu-id="83274-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="83274-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="83274-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="83274-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="83274-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="83274-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="83274-150">출력</span><span class="sxs-lookup"><span data-stu-id="83274-150">OUTPUTS</span></span>

### <span data-ttu-id="83274-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="83274-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="83274-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83274-152">NOTES</span></span>

## <span data-ttu-id="83274-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83274-153">RELATED LINKS</span></span>

[<span data-ttu-id="83274-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="83274-154">Get-AzContext</span></span>](./Get-AzContext.md)

