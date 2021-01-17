---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 4ca8156e80a827c9916def7ef749cfa9abb9389a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378043"
---
# <span data-ttu-id="d7eed-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d7eed-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="d7eed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7eed-102">SYNOPSIS</span></span>
<span data-ttu-id="d7eed-103">지정된 Relay 엔터티(네임스페이스/WcfRelay/HybridConnection)에 대해 지정된 권한 부여 규칙 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d7eed-104">구문</span><span class="sxs-lookup"><span data-stu-id="d7eed-104">SYNTAX</span></span>

### <span data-ttu-id="d7eed-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d7eed-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7eed-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7eed-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7eed-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7eed-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7eed-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d7eed-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7eed-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d7eed-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7eed-110">설명</span><span class="sxs-lookup"><span data-stu-id="d7eed-110">DESCRIPTION</span></span>
<span data-ttu-id="d7eed-111">**Set-AzRelayAuthorizationRule** cmdlet은 지정된 Relay 엔터티(네임스페이스/WcfRelay/HybridConnection)의 지정된 권한 부여 규칙에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d7eed-112">예제</span><span class="sxs-lookup"><span data-stu-id="d7eed-112">EXAMPLES</span></span>

### <span data-ttu-id="d7eed-113">예제 1.1 - InputObject가 있는 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="d7eed-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="d7eed-114">**네임스페이스에서** 권한 부여 규칙의 액세스 권한에서 `AuthoRule1` 보내기 `TestNameSpace-Relay1` 추가.</span><span class="sxs-lookup"><span data-stu-id="d7eed-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="d7eed-115">예제 1.2 - Rights 매개 변수가 있는 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="d7eed-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="d7eed-116">**네임스페이스에서** 권한 부여 규칙의 액세스 권한에서 `AuthoRule1` 보내기 `TestNameSpace-Relay1` 추가.</span><span class="sxs-lookup"><span data-stu-id="d7eed-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="d7eed-117">예제 2.1 - InputObject를 사용하여 WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d7eed-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="d7eed-118">WcfRelay의 권한 부여 규칙에 대한 액세스 권한에  `AuthoRule1` Send를 추가합니다. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="d7eed-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="d7eed-119">예제 2.2 - Rights 매개 변수가 있는 WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d7eed-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="d7eed-120">WcfRelay의 권한 부여 규칙에 대한 액세스 권한에  `AuthoRule1` Send를 추가합니다. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="d7eed-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="d7eed-121">예제 3.1 - InputObject를 사용하여 HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d7eed-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="d7eed-122">HybridConnection의 권한 부여 규칙에 대한 액세스 권한에  `AuthoRule1` Send를 추가합니다. `TestHybridConnection`</span><span class="sxs-lookup"><span data-stu-id="d7eed-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="d7eed-123">예제 3.2 - Rights 매개 변수를 사용하는 HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d7eed-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="d7eed-124">HybridConnection의 권한 부여 규칙에 대한 액세스 권한에  `AuthoRule1` Send를 추가합니다. `TestHybridConnection`</span><span class="sxs-lookup"><span data-stu-id="d7eed-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="d7eed-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7eed-125">PARAMETERS</span></span>

### <span data-ttu-id="d7eed-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7eed-126">-DefaultProfile</span></span>
<span data-ttu-id="d7eed-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7eed-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d7eed-128">-HybridConnection</span></span>
<span data-ttu-id="d7eed-129">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-129">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7eed-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7eed-130">-InputObject</span></span>
<span data-ttu-id="d7eed-131">Relay AuthorizationRule 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7eed-132">-Name</span><span class="sxs-lookup"><span data-stu-id="d7eed-132">-Name</span></span>
<span data-ttu-id="d7eed-133">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-133">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7eed-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d7eed-134">-Namespace</span></span>
<span data-ttu-id="d7eed-135">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-135">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7eed-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7eed-136">-ResourceGroupName</span></span>
<span data-ttu-id="d7eed-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7eed-138">-Rights</span><span class="sxs-lookup"><span data-stu-id="d7eed-138">-Rights</span></span>
<span data-ttu-id="d7eed-139">권한, 예: @("수신","보내기","관리")</span><span class="sxs-lookup"><span data-stu-id="d7eed-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7eed-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d7eed-140">-WcfRelay</span></span>
<span data-ttu-id="d7eed-141">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-141">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7eed-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7eed-142">-Confirm</span></span>
<span data-ttu-id="d7eed-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7eed-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7eed-144">-WhatIf</span></span>
<span data-ttu-id="d7eed-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d7eed-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7eed-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7eed-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7eed-147">CommonParameters</span></span>
<span data-ttu-id="d7eed-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d7eed-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7eed-149">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d7eed-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7eed-150">입력</span><span class="sxs-lookup"><span data-stu-id="d7eed-150">INPUTS</span></span>

### <span data-ttu-id="d7eed-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d7eed-151">System.String</span></span>

### <span data-ttu-id="d7eed-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d7eed-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="d7eed-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d7eed-153">System.String[]</span></span>

## <span data-ttu-id="d7eed-154">출력</span><span class="sxs-lookup"><span data-stu-id="d7eed-154">OUTPUTS</span></span>

### <span data-ttu-id="d7eed-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d7eed-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d7eed-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d7eed-156">NOTES</span></span>

## <span data-ttu-id="d7eed-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7eed-157">RELATED LINKS</span></span>
