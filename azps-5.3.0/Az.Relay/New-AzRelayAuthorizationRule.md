---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: 39bba687e355b1742210fb0c37fc8f1a65d957a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378099"
---
# <span data-ttu-id="aef34-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="aef34-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="aef34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aef34-102">SYNOPSIS</span></span>
<span data-ttu-id="aef34-103">지정된 릴레이 엔터티(네임스페이스/WcfRelay/HybridConnection)에 대한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="aef34-104">구문</span><span class="sxs-lookup"><span data-stu-id="aef34-104">SYNTAX</span></span>

### <span data-ttu-id="aef34-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="aef34-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aef34-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="aef34-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aef34-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="aef34-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aef34-108">설명</span><span class="sxs-lookup"><span data-stu-id="aef34-108">DESCRIPTION</span></span>
<span data-ttu-id="aef34-109">**New-AzRelayAuthorizationRule** cmdlet은 지정된 릴레이 엔터티(네임스페이스/WcfRelay/HybridConnection)에 대한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="aef34-110">예제</span><span class="sxs-lookup"><span data-stu-id="aef34-110">EXAMPLES</span></span>

### <span data-ttu-id="aef34-111">예제 1: 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="aef34-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="aef34-112">`AuthoRule1` **네임스페이스에 대한 수신** 권한으로 `TestNameSpace-Relay1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="aef34-113">예제 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="aef34-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="aef34-114">`AuthoRule1`WcfRelay에 **대한 수신** 권한으로 권한 부여 규칙을 `TestWCFRelay1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="aef34-115">예제 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="aef34-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="aef34-116">하이브리드 `AuthoRule1` **연결에 대한 수신** 권한으로 `TestHybridConnection` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="aef34-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aef34-117">PARAMETERS</span></span>

### <span data-ttu-id="aef34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aef34-118">-DefaultProfile</span></span>
<span data-ttu-id="aef34-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aef34-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="aef34-120">-HybridConnection</span></span>
<span data-ttu-id="aef34-121">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="aef34-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aef34-122">-Name</span></span>
<span data-ttu-id="aef34-123">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="aef34-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aef34-124">-Namespace</span></span>
<span data-ttu-id="aef34-125">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-125">Namespace Name.</span></span>

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

### <span data-ttu-id="aef34-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aef34-126">-ResourceGroupName</span></span>
<span data-ttu-id="aef34-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="aef34-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="aef34-128">-Rights</span></span>
<span data-ttu-id="aef34-129">권한, 예: "수신", "보내기", "관리"</span><span class="sxs-lookup"><span data-stu-id="aef34-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="aef34-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="aef34-130">-WcfRelay</span></span>
<span data-ttu-id="aef34-131">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="aef34-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aef34-132">-Confirm</span></span>
<span data-ttu-id="aef34-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aef34-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aef34-134">-WhatIf</span></span>
<span data-ttu-id="aef34-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aef34-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aef34-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aef34-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef34-137">CommonParameters</span></span>
<span data-ttu-id="aef34-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aef34-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef34-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="aef34-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef34-140">입력</span><span class="sxs-lookup"><span data-stu-id="aef34-140">INPUTS</span></span>

### <span data-ttu-id="aef34-141">System.String</span><span class="sxs-lookup"><span data-stu-id="aef34-141">System.String</span></span>

### <span data-ttu-id="aef34-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="aef34-142">System.String[]</span></span>

## <span data-ttu-id="aef34-143">출력</span><span class="sxs-lookup"><span data-stu-id="aef34-143">OUTPUTS</span></span>

### <span data-ttu-id="aef34-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="aef34-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="aef34-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aef34-145">NOTES</span></span>

## <span data-ttu-id="aef34-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aef34-146">RELATED LINKS</span></span>
