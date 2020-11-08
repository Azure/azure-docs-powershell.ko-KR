---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: 39bba687e355b1742210fb0c37fc8f1a65d957a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214694"
---
# <span data-ttu-id="b28ad-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b28ad-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="b28ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b28ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b28ad-103">지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b28ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b28ad-104">SYNTAX</span></span>

### <span data-ttu-id="b28ad-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b28ad-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b28ad-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b28ad-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b28ad-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b28ad-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b28ad-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b28ad-108">DESCRIPTION</span></span>
<span data-ttu-id="b28ad-109">**AzRelayAuthorizationRule** cmdlet은 지정 된 릴레이 엔터티 (Namespace/WcfRelay/HybridConnection)에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b28ad-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b28ad-110">EXAMPLES</span></span>

### <span data-ttu-id="b28ad-111">예제 1: 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="b28ad-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="b28ad-112">`AuthoRule1`네임 스페이스에 대 한 **듣기** 권한을 사용 하 여 만듭니다 `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b28ad-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="b28ad-113">예제 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b28ad-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="b28ad-114">`AuthoRule1`WcfRelay에 대 한 **듣기** 권한이 있는 권한 부여 규칙을 만듭니다 `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="b28ad-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="b28ad-115">예제 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b28ad-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="b28ad-116">`AuthoRule1`하이브리드 연결에 대 한 **듣기** 권한을 사용 하 여 만듭니다 `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="b28ad-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="b28ad-117">변수</span><span class="sxs-lookup"><span data-stu-id="b28ad-117">PARAMETERS</span></span>

### <span data-ttu-id="b28ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b28ad-118">-DefaultProfile</span></span>
<span data-ttu-id="b28ad-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b28ad-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b28ad-120">-HybridConnection</span></span>
<span data-ttu-id="b28ad-121">HybridConnection 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="b28ad-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b28ad-122">-Name</span></span>
<span data-ttu-id="b28ad-123">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b28ad-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b28ad-124">-Namespace</span></span>
<span data-ttu-id="b28ad-125">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-125">Namespace Name.</span></span>

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

### <span data-ttu-id="b28ad-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b28ad-126">-ResourceGroupName</span></span>
<span data-ttu-id="b28ad-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b28ad-128">-권한</span><span class="sxs-lookup"><span data-stu-id="b28ad-128">-Rights</span></span>
<span data-ttu-id="b28ad-129">권한 (예: "듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="b28ad-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="b28ad-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b28ad-130">-WcfRelay</span></span>
<span data-ttu-id="b28ad-131">WcfRelay 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="b28ad-132">-확인</span><span class="sxs-lookup"><span data-stu-id="b28ad-132">-Confirm</span></span>
<span data-ttu-id="b28ad-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b28ad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b28ad-134">-WhatIf</span></span>
<span data-ttu-id="b28ad-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b28ad-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b28ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28ad-137">CommonParameters</span></span>
<span data-ttu-id="b28ad-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b28ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28ad-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b28ad-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28ad-140">입력</span><span class="sxs-lookup"><span data-stu-id="b28ad-140">INPUTS</span></span>

### <span data-ttu-id="b28ad-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b28ad-141">System.String</span></span>

### <span data-ttu-id="b28ad-142">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="b28ad-142">System.String[]</span></span>

## <span data-ttu-id="b28ad-143">출력</span><span class="sxs-lookup"><span data-stu-id="b28ad-143">OUTPUTS</span></span>

### <span data-ttu-id="b28ad-144">Microsoft. m a m. 모델. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b28ad-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b28ad-145">상속자</span><span class="sxs-lookup"><span data-stu-id="b28ad-145">NOTES</span></span>

## <span data-ttu-id="b28ad-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b28ad-146">RELATED LINKS</span></span>
