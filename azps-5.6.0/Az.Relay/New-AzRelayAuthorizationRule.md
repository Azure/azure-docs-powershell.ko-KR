---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: d0faea052141420db88f58fd6513c2d6822f56c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000571"
---
# <span data-ttu-id="9b052-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9b052-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="9b052-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b052-102">SYNOPSIS</span></span>
<span data-ttu-id="9b052-103">지정된 릴레이 엔터티(네임스페이스/WcfRelay/HybridConnection)에 대한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="9b052-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b052-104">SYNTAX</span></span>

### <span data-ttu-id="9b052-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9b052-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b052-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9b052-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b052-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9b052-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b052-108">설명</span><span class="sxs-lookup"><span data-stu-id="9b052-108">DESCRIPTION</span></span>
<span data-ttu-id="9b052-109">**New-AzRelayAuthorizationRule** cmdlet은 지정된 릴레이 엔터티(네임스페이스/WcfRelay/HybridConnection)에 대한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="9b052-110">예제</span><span class="sxs-lookup"><span data-stu-id="9b052-110">EXAMPLES</span></span>

### <span data-ttu-id="9b052-111">예제 1: 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="9b052-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="9b052-112">`AuthoRule1`네임스페이스에 **대한 Listen** 권한으로 `TestNameSpace-Relay1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="9b052-113">예제 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9b052-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="9b052-114">`AuthoRule1`WcfRelay에 **대한 수신** 권한으로 권한 부여 규칙을 `TestWCFRelay1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="9b052-115">예제 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9b052-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="9b052-116">하이브리드 `AuthoRule1` **연결에 대한 수신기** 권한으로 `TestHybridConnection` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="9b052-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9b052-117">PARAMETERS</span></span>

### <span data-ttu-id="9b052-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b052-118">-DefaultProfile</span></span>
<span data-ttu-id="9b052-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b052-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="9b052-120">-HybridConnection</span></span>
<span data-ttu-id="9b052-121">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="9b052-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9b052-122">-Name</span></span>
<span data-ttu-id="9b052-123">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9b052-124">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="9b052-124">-Namespace</span></span>
<span data-ttu-id="9b052-125">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-125">Namespace Name.</span></span>

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

### <span data-ttu-id="9b052-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b052-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b052-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="9b052-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="9b052-128">-Rights</span></span>
<span data-ttu-id="9b052-129">권한(예: "수신", "보내기", "관리"</span><span class="sxs-lookup"><span data-stu-id="9b052-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b052-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="9b052-130">-WcfRelay</span></span>
<span data-ttu-id="9b052-131">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="9b052-132">-확인</span><span class="sxs-lookup"><span data-stu-id="9b052-132">-Confirm</span></span>
<span data-ttu-id="9b052-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b052-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b052-134">-WhatIf</span></span>
<span data-ttu-id="9b052-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b052-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b052-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b052-137">CommonParameters</span></span>
<span data-ttu-id="9b052-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b052-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b052-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9b052-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b052-140">입력</span><span class="sxs-lookup"><span data-stu-id="9b052-140">INPUTS</span></span>

### <span data-ttu-id="9b052-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9b052-141">System.String</span></span>

### <span data-ttu-id="9b052-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="9b052-142">System.String[]</span></span>

## <span data-ttu-id="9b052-143">출력</span><span class="sxs-lookup"><span data-stu-id="9b052-143">OUTPUTS</span></span>

### <span data-ttu-id="9b052-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9b052-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9b052-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b052-145">NOTES</span></span>

## <span data-ttu-id="9b052-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b052-146">RELATED LINKS</span></span>
