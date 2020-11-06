---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 64c839140907b10d62b4f71025afab985d5ba736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533008"
---
# <span data-ttu-id="e2df1-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2df1-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="e2df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2df1-102">SYNOPSIS</span></span>
<span data-ttu-id="e2df1-103">지정 된 릴레이 엔터티 (네임 스페이스/WcfRelay/HybridConnection)에 대해 지정한 권한 부여 규칙 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2df1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2df1-104">SYNTAX</span></span>

### <span data-ttu-id="e2df1-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2df1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2df1-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2df1-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2df1-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2df1-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-InputObject <AuthorizationRuleAttributes>]
 [-Rights <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2df1-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2df1-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 -InputObject <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2df1-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e2df1-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> -Rights <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2df1-110">설명은</span><span class="sxs-lookup"><span data-stu-id="e2df1-110">DESCRIPTION</span></span>
<span data-ttu-id="e2df1-111">**AzureRmRelayAuthorizationRule** cmdlet은 지정 된 릴레이 엔티티의 지정 된 권한 부여 규칙에 대 한 설명을 업데이트 합니다 (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="e2df1-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="e2df1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e2df1-112">EXAMPLES</span></span>

### <span data-ttu-id="e2df1-113">예제 1.1-InputObject를 사용 하는 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="e2df1-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="e2df1-114">네임 스페이스의 권한 부여 규칙에 대 한 액세스 권한에서 **보내기를** 추가 `AuthoRule1` `TestNameSpace-Relay1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="e2df1-115">예제 1.2-권한 매개 변수가 있는 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="e2df1-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="e2df1-116">네임 스페이스의 권한 부여 규칙에 대 한 액세스 권한에서 **보내기를** 추가 `AuthoRule1` `TestNameSpace-Relay1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="e2df1-117">예제 2.1-InputObject with WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e2df1-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="e2df1-118">WcfRelay의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="e2df1-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="e2df1-119">예제 2.2-권한 매개 변수가 있는 WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e2df1-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="e2df1-120">WcfRelay의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="e2df1-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="e2df1-121">예제 3.1-InputObject with HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e2df1-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="e2df1-122">HybridConnection의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="e2df1-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="e2df1-123">예제 3.2-권한 매개 변수가 있는 HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e2df1-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="e2df1-124">HybridConnection의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="e2df1-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="e2df1-125">변수</span><span class="sxs-lookup"><span data-stu-id="e2df1-125">PARAMETERS</span></span>

### <span data-ttu-id="e2df1-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e2df1-126">-Confirm</span></span>
<span data-ttu-id="e2df1-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2df1-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e2df1-128">-HybridConnection</span></span>
<span data-ttu-id="e2df1-129">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="e2df1-130">-이름</span><span class="sxs-lookup"><span data-stu-id="e2df1-130">-Name</span></span>
<span data-ttu-id="e2df1-131">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e2df1-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2df1-132">-Namespace</span></span>
<span data-ttu-id="e2df1-133">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-133">Namespace Name.</span></span>

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

### <span data-ttu-id="e2df1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2df1-134">-ResourceGroupName</span></span>
<span data-ttu-id="e2df1-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="e2df1-136">-권한</span><span class="sxs-lookup"><span data-stu-id="e2df1-136">-Rights</span></span>
<span data-ttu-id="e2df1-137">권한 (예: @ ("듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="e2df1-137">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2df1-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e2df1-138">-WcfRelay</span></span>
<span data-ttu-id="e2df1-139">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="e2df1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2df1-140">-WhatIf</span></span>
<span data-ttu-id="e2df1-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2df1-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2df1-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2df1-143">-DefaultProfile</span></span>
<span data-ttu-id="e2df1-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2df1-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2df1-145">-InputObject</span></span>
<span data-ttu-id="e2df1-146">{{Fill InputObject 설명}}</span><span class="sxs-lookup"><span data-stu-id="e2df1-146">{{Fill InputObject Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2df1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2df1-147">CommonParameters</span></span>
<span data-ttu-id="e2df1-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2df1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2df1-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2df1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2df1-150">입력</span><span class="sxs-lookup"><span data-stu-id="e2df1-150">INPUTS</span></span>

### <span data-ttu-id="e2df1-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2df1-151">-ResourceGroupName</span></span>
 <span data-ttu-id="e2df1-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2df1-152">System.String</span></span> 

### <span data-ttu-id="e2df1-153">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2df1-153">-Namespace</span></span>
 <span data-ttu-id="e2df1-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2df1-154">System.String</span></span> 
 

### <span data-ttu-id="e2df1-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e2df1-155">-WcfRelay</span></span>
 <span data-ttu-id="e2df1-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2df1-156">System.String</span></span> 

### <span data-ttu-id="e2df1-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e2df1-157">-HybridConnection</span></span>
 <span data-ttu-id="e2df1-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2df1-158">System.String</span></span> 
 

### <span data-ttu-id="e2df1-159">-이름</span><span class="sxs-lookup"><span data-stu-id="e2df1-159">-Name</span></span>
 <span data-ttu-id="e2df1-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2df1-160">System.String</span></span>

### <span data-ttu-id="e2df1-161">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2df1-161">-InputObject</span></span>
 <span data-ttu-id="e2df1-162">Microsoft. i m. 모델. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e2df1-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="e2df1-163">-권한</span><span class="sxs-lookup"><span data-stu-id="e2df1-163">-Rights</span></span>
 <span data-ttu-id="e2df1-164">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e2df1-164">System.String []</span></span>

## <span data-ttu-id="e2df1-165">출력</span><span class="sxs-lookup"><span data-stu-id="e2df1-165">OUTPUTS</span></span>

### <span data-ttu-id="e2df1-166">Microsoft. i m. 모델. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e2df1-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="e2df1-167">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="e2df1-167">Example 1 - Namespace</span></span>
<span data-ttu-id="e2df1-168">권한: {Listen, Send} 이름: AuthoRule1 Type: Microsoft. 릴레이/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="e2df1-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="e2df1-169">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e2df1-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="e2df1-170">권한: {Listen, Send} 이름: AuthoRule1 Type: Microsoft. 릴레이/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="e2df1-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="e2df1-171">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e2df1-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="e2df1-172">권한: {Listen, Send} 이름: AuthoRule1 Type: Microsoft. 릴레이/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="e2df1-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="e2df1-173">상속자</span><span class="sxs-lookup"><span data-stu-id="e2df1-173">NOTES</span></span>

## <span data-ttu-id="e2df1-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2df1-174">RELATED LINKS</span></span>

