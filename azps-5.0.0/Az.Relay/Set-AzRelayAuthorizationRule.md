---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 4ca8156e80a827c9916def7ef749cfa9abb9389a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309974"
---
# <span data-ttu-id="11981-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="11981-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="11981-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11981-102">SYNOPSIS</span></span>
<span data-ttu-id="11981-103">지정 된 릴레이 엔터티 (네임 스페이스/WcfRelay/HybridConnection)에 대해 지정한 권한 부여 규칙 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="11981-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="11981-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11981-104">SYNTAX</span></span>

### <span data-ttu-id="11981-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="11981-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11981-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="11981-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11981-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="11981-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11981-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11981-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11981-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="11981-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11981-110">설명은</span><span class="sxs-lookup"><span data-stu-id="11981-110">DESCRIPTION</span></span>
<span data-ttu-id="11981-111">**AzRelayAuthorizationRule** cmdlet은 지정 된 릴레이 엔티티의 지정 된 권한 부여 규칙에 대 한 설명을 업데이트 합니다 (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="11981-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="11981-112">예제의</span><span class="sxs-lookup"><span data-stu-id="11981-112">EXAMPLES</span></span>

### <span data-ttu-id="11981-113">예제 1.1-InputObject를 사용 하는 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="11981-113">Example 1.1 - Namespace with InputObject</span></span>
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

<span data-ttu-id="11981-114">네임 스페이스의 권한 부여 규칙에 대 한 액세스 권한에서 **보내기를** 추가 `AuthoRule1` `TestNameSpace-Relay1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="11981-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="11981-115">예제 1.2-권한 매개 변수가 있는 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="11981-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="11981-116">네임 스페이스의 권한 부여 규칙에 대 한 액세스 권한에서 **보내기를** 추가 `AuthoRule1` `TestNameSpace-Relay1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="11981-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="11981-117">예제 2.1-InputObject with WcfRelay</span><span class="sxs-lookup"><span data-stu-id="11981-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="11981-118">WcfRelay의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="11981-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="11981-119">예제 2.2-권한 매개 변수가 있는 WcfRelay</span><span class="sxs-lookup"><span data-stu-id="11981-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="11981-120">WcfRelay의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="11981-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="11981-121">예제 3.1-InputObject with HybridConnection</span><span class="sxs-lookup"><span data-stu-id="11981-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="11981-122">HybridConnection의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="11981-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="11981-123">예제 3.2-권한 매개 변수가 있는 HybridConnection</span><span class="sxs-lookup"><span data-stu-id="11981-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="11981-124">HybridConnection의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="11981-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="11981-125">변수</span><span class="sxs-lookup"><span data-stu-id="11981-125">PARAMETERS</span></span>

### <span data-ttu-id="11981-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11981-126">-DefaultProfile</span></span>
<span data-ttu-id="11981-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11981-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11981-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="11981-128">-HybridConnection</span></span>
<span data-ttu-id="11981-129">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11981-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="11981-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11981-130">-InputObject</span></span>
<span data-ttu-id="11981-131">릴레이 AuthorizationRule 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="11981-131">Relay AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="11981-132">-이름</span><span class="sxs-lookup"><span data-stu-id="11981-132">-Name</span></span>
<span data-ttu-id="11981-133">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11981-133">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="11981-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="11981-134">-Namespace</span></span>
<span data-ttu-id="11981-135">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11981-135">Namespace Name.</span></span>

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

### <span data-ttu-id="11981-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11981-136">-ResourceGroupName</span></span>
<span data-ttu-id="11981-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11981-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="11981-138">-권한</span><span class="sxs-lookup"><span data-stu-id="11981-138">-Rights</span></span>
<span data-ttu-id="11981-139">권한 (예: @ ("듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="11981-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="11981-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="11981-140">-WcfRelay</span></span>
<span data-ttu-id="11981-141">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11981-141">WcfRelay Name.</span></span>

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

### <span data-ttu-id="11981-142">-확인</span><span class="sxs-lookup"><span data-stu-id="11981-142">-Confirm</span></span>
<span data-ttu-id="11981-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11981-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11981-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11981-144">-WhatIf</span></span>
<span data-ttu-id="11981-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11981-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11981-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11981-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11981-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11981-147">CommonParameters</span></span>
<span data-ttu-id="11981-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11981-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11981-149">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11981-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11981-150">입력</span><span class="sxs-lookup"><span data-stu-id="11981-150">INPUTS</span></span>

### <span data-ttu-id="11981-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11981-151">System.String</span></span>

### <span data-ttu-id="11981-152">Microsoft. m a m. 모델. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="11981-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="11981-153">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="11981-153">System.String[]</span></span>

## <span data-ttu-id="11981-154">출력</span><span class="sxs-lookup"><span data-stu-id="11981-154">OUTPUTS</span></span>

### <span data-ttu-id="11981-155">Microsoft. m a m. 모델. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="11981-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="11981-156">상속자</span><span class="sxs-lookup"><span data-stu-id="11981-156">NOTES</span></span>

## <span data-ttu-id="11981-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11981-157">RELATED LINKS</span></span>
