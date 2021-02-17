---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 862b6f295a997b2027520a3f9c6a9f4f9cfb5ae9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200361"
---
# <span data-ttu-id="fa876-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fa876-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="fa876-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa876-102">SYNOPSIS</span></span>
<span data-ttu-id="fa876-103">이벤트 허브에서 지정된 권한 부여 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fa876-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="fa876-104">구문</span><span class="sxs-lookup"><span data-stu-id="fa876-104">SYNTAX</span></span>

### <span data-ttu-id="fa876-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fa876-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa876-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fa876-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa876-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fa876-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa876-108">설명</span><span class="sxs-lookup"><span data-stu-id="fa876-108">DESCRIPTION</span></span>
<span data-ttu-id="fa876-109">이 Set-AzEventHubAuthorizationRule cmdlet은 지정된 이벤트 허브에서 지정된 권한 부여 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fa876-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="fa876-110">예제</span><span class="sxs-lookup"><span data-stu-id="fa876-110">EXAMPLES</span></span>

### <span data-ttu-id="fa876-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fa876-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="fa876-112">MyAuthRuleName 권한 부여 규칙을 업데이트하여 MyNamespaceName 네임스페이스로 범위가 지정된 \` \` Event Hub \` MyEventHubName에 관리 권한을 \` \` \` 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="fa876-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="fa876-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa876-113">PARAMETERS</span></span>

### <span data-ttu-id="fa876-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa876-114">-DefaultProfile</span></span>
<span data-ttu-id="fa876-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa876-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa876-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="fa876-116">-EventHub</span></span>
<span data-ttu-id="fa876-117">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="fa876-117">EventHub Name</span></span>

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

### <span data-ttu-id="fa876-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa876-118">-InputObject</span></span>
<span data-ttu-id="fa876-119">AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="fa876-119">AuthorizationRule Object</span></span>

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

### <span data-ttu-id="fa876-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fa876-120">-Name</span></span>
<span data-ttu-id="fa876-121">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="fa876-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="fa876-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fa876-122">-Namespace</span></span>
<span data-ttu-id="fa876-123">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="fa876-123">Namespace Name</span></span>

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

### <span data-ttu-id="fa876-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa876-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa876-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fa876-125">Resource Group Name</span></span>

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

### <span data-ttu-id="fa876-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="fa876-126">-Rights</span></span>
<span data-ttu-id="fa876-127">권한, 예: @("수신","보내기","관리")</span><span class="sxs-lookup"><span data-stu-id="fa876-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="fa876-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa876-128">-Confirm</span></span>
<span data-ttu-id="fa876-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa876-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa876-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa876-130">-WhatIf</span></span>
<span data-ttu-id="fa876-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fa876-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa876-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa876-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa876-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa876-133">CommonParameters</span></span>
<span data-ttu-id="fa876-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fa876-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa876-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa876-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa876-136">입력</span><span class="sxs-lookup"><span data-stu-id="fa876-136">INPUTS</span></span>

### <span data-ttu-id="fa876-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fa876-137">System.String</span></span>

### <span data-ttu-id="fa876-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fa876-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="fa876-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="fa876-139">System.String[]</span></span>

## <span data-ttu-id="fa876-140">출력</span><span class="sxs-lookup"><span data-stu-id="fa876-140">OUTPUTS</span></span>

### <span data-ttu-id="fa876-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fa876-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="fa876-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fa876-142">NOTES</span></span>

## <span data-ttu-id="fa876-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa876-143">RELATED LINKS</span></span>
