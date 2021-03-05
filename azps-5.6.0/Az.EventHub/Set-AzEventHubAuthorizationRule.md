---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: ef71b8ce2f90fb6275c3bd658289f4e32579cd69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004155"
---
# <span data-ttu-id="7d991-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7d991-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="7d991-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d991-102">SYNOPSIS</span></span>
<span data-ttu-id="7d991-103">Event Hub에서 지정된 권한 부여 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7d991-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="7d991-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d991-104">SYNTAX</span></span>

### <span data-ttu-id="7d991-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d991-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d991-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d991-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d991-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7d991-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d991-108">설명</span><span class="sxs-lookup"><span data-stu-id="7d991-108">DESCRIPTION</span></span>
<span data-ttu-id="7d991-109">Set-AzEventHubAuthorizationRule cmdlet은 지정된 Event Hub에서 지정된 권한 부여 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7d991-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="7d991-110">예제</span><span class="sxs-lookup"><span data-stu-id="7d991-110">EXAMPLES</span></span>

### <span data-ttu-id="7d991-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d991-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="7d991-112">MyAuthRuleName 권한 부여 규칙을 업데이트하여 \` \` 네임스페이스 \` \` \` MyNamespaceName에서 범위가 지정한 Event Hub MyEventHubName에 \` 대한 관리 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="7d991-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="7d991-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d991-113">PARAMETERS</span></span>

### <span data-ttu-id="7d991-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d991-114">-DefaultProfile</span></span>
<span data-ttu-id="7d991-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d991-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d991-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7d991-116">-EventHub</span></span>
<span data-ttu-id="7d991-117">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="7d991-117">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d991-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d991-118">-InputObject</span></span>
<span data-ttu-id="7d991-119">AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="7d991-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d991-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7d991-120">-Name</span></span>
<span data-ttu-id="7d991-121">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="7d991-121">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d991-122">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="7d991-122">-Namespace</span></span>
<span data-ttu-id="7d991-123">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="7d991-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d991-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d991-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d991-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7d991-125">Resource Group Name</span></span>

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

### <span data-ttu-id="7d991-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="7d991-126">-Rights</span></span>
<span data-ttu-id="7d991-127">권한(예: @("수신","보내기","관리")</span><span class="sxs-lookup"><span data-stu-id="7d991-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d991-128">-확인</span><span class="sxs-lookup"><span data-stu-id="7d991-128">-Confirm</span></span>
<span data-ttu-id="7d991-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d991-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d991-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d991-130">-WhatIf</span></span>
<span data-ttu-id="7d991-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d991-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d991-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d991-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d991-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d991-133">CommonParameters</span></span>
<span data-ttu-id="7d991-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d991-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d991-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7d991-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d991-136">입력</span><span class="sxs-lookup"><span data-stu-id="7d991-136">INPUTS</span></span>

### <span data-ttu-id="7d991-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7d991-137">System.String</span></span>

### <span data-ttu-id="7d991-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7d991-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="7d991-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7d991-139">System.String[]</span></span>

## <span data-ttu-id="7d991-140">출력</span><span class="sxs-lookup"><span data-stu-id="7d991-140">OUTPUTS</span></span>

### <span data-ttu-id="7d991-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7d991-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7d991-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d991-142">NOTES</span></span>

## <span data-ttu-id="7d991-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d991-143">RELATED LINKS</span></span>
