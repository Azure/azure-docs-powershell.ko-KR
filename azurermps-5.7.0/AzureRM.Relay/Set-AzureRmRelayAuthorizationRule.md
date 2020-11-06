---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 91f37ad2ed49b4c1bd39306be803776ddce9ecff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534724"
---
# <span data-ttu-id="c7854-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c7854-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="c7854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7854-102">SYNOPSIS</span></span>
<span data-ttu-id="c7854-103">지정 된 릴레이 엔터티 (네임 스페이스/WcfRelay/HybridConnection)에 대해 지정한 권한 부여 규칙 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7854-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7854-104">SYNTAX</span></span>

### <span data-ttu-id="c7854-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c7854-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7854-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c7854-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7854-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c7854-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>]
 [[-Rights] <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7854-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c7854-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7854-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="c7854-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7854-110">설명은</span><span class="sxs-lookup"><span data-stu-id="c7854-110">DESCRIPTION</span></span>
<span data-ttu-id="c7854-111">**AzureRmRelayAuthorizationRule** cmdlet은 지정 된 릴레이 엔티티의 지정 된 권한 부여 규칙에 대 한 설명을 업데이트 합니다 (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="c7854-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c7854-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c7854-112">EXAMPLES</span></span>

### <span data-ttu-id="c7854-113">예제 1.1-InputObject를 사용 하는 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="c7854-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="c7854-114">네임 스페이스의 권한 부여 규칙에 대 한 액세스 권한에서 **보내기를** 추가 `AuthoRule1` `TestNameSpace-Relay1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="c7854-115">예제 1.2-권한 매개 변수가 있는 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="c7854-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="c7854-116">네임 스페이스의 권한 부여 규칙에 대 한 액세스 권한에서 **보내기를** 추가 `AuthoRule1` `TestNameSpace-Relay1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="c7854-117">예제 2.1-InputObject with WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c7854-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="c7854-118">WcfRelay의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="c7854-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="c7854-119">예제 2.2-권한 매개 변수가 있는 WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c7854-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="c7854-120">WcfRelay의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="c7854-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="c7854-121">예제 3.1-InputObject with HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c7854-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="c7854-122">HybridConnection의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="c7854-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="c7854-123">예제 3.2-권한 매개 변수가 있는 HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c7854-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="c7854-124">HybridConnection의 권한 부여 규칙에 대 한 액세스 권한으로 **보내기를** 추가 합니다 `AuthoRule1` `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="c7854-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="c7854-125">변수</span><span class="sxs-lookup"><span data-stu-id="c7854-125">PARAMETERS</span></span>

### <span data-ttu-id="c7854-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7854-126">-DefaultProfile</span></span>
<span data-ttu-id="c7854-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c7854-128">-HybridConnection</span></span>
<span data-ttu-id="c7854-129">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-129">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7854-130">-InputObject</span></span>
<span data-ttu-id="c7854-131">릴레이 AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="c7854-131">Relay AuthorizationRule Object</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-132">-이름</span><span class="sxs-lookup"><span data-stu-id="c7854-132">-Name</span></span>
<span data-ttu-id="c7854-133">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-133">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c7854-134">-Namespace</span></span>
<span data-ttu-id="c7854-135">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-135">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7854-136">-ResourceGroupName</span></span>
<span data-ttu-id="c7854-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-138">-권한</span><span class="sxs-lookup"><span data-stu-id="c7854-138">-Rights</span></span>
<span data-ttu-id="c7854-139">권한 (예: @ ("듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="c7854-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c7854-140">-WcfRelay</span></span>
<span data-ttu-id="c7854-141">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-141">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-142">-확인</span><span class="sxs-lookup"><span data-stu-id="c7854-142">-Confirm</span></span>
<span data-ttu-id="c7854-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7854-144">-WhatIf</span></span>
<span data-ttu-id="c7854-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7854-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7854-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7854-147">CommonParameters</span></span>
<span data-ttu-id="c7854-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7854-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7854-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7854-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7854-150">입력</span><span class="sxs-lookup"><span data-stu-id="c7854-150">INPUTS</span></span>

### <span data-ttu-id="c7854-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7854-151">-ResourceGroupName</span></span>
 <span data-ttu-id="c7854-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7854-152">System.String</span></span> 

### <span data-ttu-id="c7854-153">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c7854-153">-Namespace</span></span>
 <span data-ttu-id="c7854-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7854-154">System.String</span></span> 
 

### <span data-ttu-id="c7854-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c7854-155">-WcfRelay</span></span>
 <span data-ttu-id="c7854-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7854-156">System.String</span></span> 

### <span data-ttu-id="c7854-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c7854-157">-HybridConnection</span></span>
 <span data-ttu-id="c7854-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7854-158">System.String</span></span> 
 

### <span data-ttu-id="c7854-159">-이름</span><span class="sxs-lookup"><span data-stu-id="c7854-159">-Name</span></span>
 <span data-ttu-id="c7854-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7854-160">System.String</span></span>

### <span data-ttu-id="c7854-161">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7854-161">-InputObject</span></span>
 <span data-ttu-id="c7854-162">Microsoft. i m. 모델. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c7854-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="c7854-163">-권한</span><span class="sxs-lookup"><span data-stu-id="c7854-163">-Rights</span></span>
 <span data-ttu-id="c7854-164">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="c7854-164">System.String []</span></span>

## <span data-ttu-id="c7854-165">출력</span><span class="sxs-lookup"><span data-stu-id="c7854-165">OUTPUTS</span></span>

### <span data-ttu-id="c7854-166">Microsoft. i m. 모델. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c7854-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="c7854-167">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="c7854-167">Example 1 - Namespace</span></span>
<span data-ttu-id="c7854-168">권한: {Listen, Send} 이름: AuthoRule1 Type: Microsoft. 릴레이/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="c7854-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="c7854-169">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c7854-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="c7854-170">권한: {Listen, Send} 이름: AuthoRule1 Type: Microsoft. 릴레이/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="c7854-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="c7854-171">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c7854-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="c7854-172">권한: {Listen, Send} 이름: AuthoRule1 Type: Microsoft. 릴레이/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="c7854-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="c7854-173">상속자</span><span class="sxs-lookup"><span data-stu-id="c7854-173">NOTES</span></span>

## <span data-ttu-id="c7854-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7854-174">RELATED LINKS</span></span>

