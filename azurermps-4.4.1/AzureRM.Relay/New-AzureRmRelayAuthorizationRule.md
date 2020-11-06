---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 9e4eecad543346efa60dfb0b9a20e31c47a59036
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529177"
---
# <span data-ttu-id="301fb-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="301fb-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="301fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="301fb-102">SYNOPSIS</span></span>
<span data-ttu-id="301fb-103">지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="301fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="301fb-104">SYNTAX</span></span>

### <span data-ttu-id="301fb-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="301fb-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301fb-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="301fb-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="301fb-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="301fb-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="301fb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="301fb-108">DESCRIPTION</span></span>
<span data-ttu-id="301fb-109">**AzureRmRelayAuthorizationRule** cmdlet은 지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="301fb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="301fb-110">EXAMPLES</span></span>

### <span data-ttu-id="301fb-111">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="301fb-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="301fb-112">`AuthoRule1`네임 스페이스에 대 한 **듣기** 권한을 사용 하 여 만듭니다 `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="301fb-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="301fb-113">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="301fb-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="301fb-114">`AuthoRule1`WcfRelay에 대 한 **듣기** 권한이 있는 권한 부여 규칙을 만듭니다 `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="301fb-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="301fb-115">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="301fb-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="301fb-116">`AuthoRule1`네임 스페이스에 대 한 **듣기** 권한을 사용 하 여 만듭니다 `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="301fb-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="301fb-117">변수</span><span class="sxs-lookup"><span data-stu-id="301fb-117">PARAMETERS</span></span>

### <span data-ttu-id="301fb-118">-확인</span><span class="sxs-lookup"><span data-stu-id="301fb-118">-Confirm</span></span>
<span data-ttu-id="301fb-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301fb-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="301fb-120">-HybridConnection</span></span>
<span data-ttu-id="301fb-121">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="301fb-122">-이름</span><span class="sxs-lookup"><span data-stu-id="301fb-122">-Name</span></span>
<span data-ttu-id="301fb-123">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="301fb-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="301fb-124">-Namespace</span></span>
<span data-ttu-id="301fb-125">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-125">Namespace Name.</span></span>

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

### <span data-ttu-id="301fb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301fb-126">-ResourceGroupName</span></span>
<span data-ttu-id="301fb-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="301fb-128">-권한</span><span class="sxs-lookup"><span data-stu-id="301fb-128">-Rights</span></span>
<span data-ttu-id="301fb-129">권한 (예: "듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="301fb-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="301fb-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="301fb-130">-WcfRelay</span></span>
<span data-ttu-id="301fb-131">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="301fb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301fb-132">-WhatIf</span></span>
<span data-ttu-id="301fb-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301fb-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301fb-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301fb-135">-DefaultProfile</span></span>
<span data-ttu-id="301fb-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="301fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301fb-137">CommonParameters</span></span>
<span data-ttu-id="301fb-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="301fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301fb-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="301fb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301fb-140">입력</span><span class="sxs-lookup"><span data-stu-id="301fb-140">INPUTS</span></span>

### <span data-ttu-id="301fb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301fb-141">-ResourceGroupName</span></span>
 <span data-ttu-id="301fb-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="301fb-142">System.String</span></span> 

### <span data-ttu-id="301fb-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="301fb-143">-Namespace</span></span>
 <span data-ttu-id="301fb-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="301fb-144">System.String</span></span> 
 

### <span data-ttu-id="301fb-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="301fb-145">-WcfRelay</span></span>
 <span data-ttu-id="301fb-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="301fb-146">System.String</span></span> 

### <span data-ttu-id="301fb-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="301fb-147">-HybridConnection</span></span>
 <span data-ttu-id="301fb-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="301fb-148">System.String</span></span> 
 

### <span data-ttu-id="301fb-149">-이름</span><span class="sxs-lookup"><span data-stu-id="301fb-149">-Name</span></span>
 <span data-ttu-id="301fb-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="301fb-150">System.String</span></span>
 

### <span data-ttu-id="301fb-151">-권한</span><span class="sxs-lookup"><span data-stu-id="301fb-151">-Rights</span></span>
 <span data-ttu-id="301fb-152">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="301fb-152">System.String []</span></span>

## <span data-ttu-id="301fb-153">출력</span><span class="sxs-lookup"><span data-stu-id="301fb-153">OUTPUTS</span></span>

### <span data-ttu-id="301fb-154">Microsoft. i m. 모델. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="301fb-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="301fb-155">예제 1-네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="301fb-155">Example 1 - Namespace</span></span>
<span data-ttu-id="301fb-156">권한: {Listen} 이름: AuthoRule1 Type: Microsoft. 릴레이/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="301fb-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="301fb-157">예제 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="301fb-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="301fb-158">권한: {Listen} 이름: AuthoRule1 Type: Microsoft. 릴레이/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="301fb-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="301fb-159">예제 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="301fb-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="301fb-160">권한: {Listen} 이름: AuthoRule1 Type: Microsoft. 릴레이/AuthorizationRules Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="301fb-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="301fb-161">상속자</span><span class="sxs-lookup"><span data-stu-id="301fb-161">NOTES</span></span>

## <span data-ttu-id="301fb-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="301fb-162">RELATED LINKS</span></span>

