---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: fde71fed26c074efa705d0b1dc181dfb46bae44e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957152"
---
# <span data-ttu-id="e42a9-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e42a9-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="e42a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e42a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e42a9-103">네임스페이스 또는 eventhub에 대한 새 Event Hubs 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e42a9-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="e42a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="e42a9-104">SYNTAX</span></span>

### <span data-ttu-id="e42a9-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e42a9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e42a9-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e42a9-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e42a9-107">설명</span><span class="sxs-lookup"><span data-stu-id="e42a9-107">DESCRIPTION</span></span>
<span data-ttu-id="e42a9-108">New-AzEventHubAuthorizationRule cmdlet은 새 Event Hubs 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e42a9-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="e42a9-109">예제</span><span class="sxs-lookup"><span data-stu-id="e42a9-109">EXAMPLES</span></span>

### <span data-ttu-id="e42a9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e42a9-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="e42a9-111">리소스 그룹 \` \` \` \` \` MyResourceGroupName이 있는 네임스페이스 MyNamespaceName에 수신 및 보내기 권한을 부여하는 권한 부여 규칙 MyAuthRuleName을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e42a9-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e42a9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e42a9-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="e42a9-113">리소스 그룹 \` \` \` \` \` \` \` MyResourceGroupName이 있는 네임스페이스 MyNamespaceName에서 Event Hub MyEventHubName에 수신 및 보내기 권한을 부여하는 권한 부여 규칙 MyAuthRuleName을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e42a9-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e42a9-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e42a9-114">PARAMETERS</span></span>

### <span data-ttu-id="e42a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42a9-115">-DefaultProfile</span></span>
<span data-ttu-id="e42a9-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e42a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e42a9-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e42a9-117">-EventHub</span></span>
<span data-ttu-id="e42a9-118">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="e42a9-118">EventHub Name</span></span>

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

### <span data-ttu-id="e42a9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e42a9-119">-Name</span></span>
<span data-ttu-id="e42a9-120">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="e42a9-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="e42a9-121">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="e42a9-121">-Namespace</span></span>
<span data-ttu-id="e42a9-122">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="e42a9-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e42a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="e42a9-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e42a9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e42a9-125">-Rights</span><span class="sxs-lookup"><span data-stu-id="e42a9-125">-Rights</span></span>
<span data-ttu-id="e42a9-126">권한(예: "수신", "보내기", "관리"</span><span class="sxs-lookup"><span data-stu-id="e42a9-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="e42a9-127">-확인</span><span class="sxs-lookup"><span data-stu-id="e42a9-127">-Confirm</span></span>
<span data-ttu-id="e42a9-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e42a9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e42a9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e42a9-129">-WhatIf</span></span>
<span data-ttu-id="e42a9-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e42a9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e42a9-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e42a9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e42a9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42a9-132">CommonParameters</span></span>
<span data-ttu-id="e42a9-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e42a9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42a9-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e42a9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42a9-135">입력</span><span class="sxs-lookup"><span data-stu-id="e42a9-135">INPUTS</span></span>

### <span data-ttu-id="e42a9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e42a9-136">System.String</span></span>

### <span data-ttu-id="e42a9-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e42a9-137">System.String[]</span></span>

## <span data-ttu-id="e42a9-138">출력</span><span class="sxs-lookup"><span data-stu-id="e42a9-138">OUTPUTS</span></span>

### <span data-ttu-id="e42a9-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e42a9-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e42a9-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e42a9-140">NOTES</span></span>

## <span data-ttu-id="e42a9-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e42a9-141">RELATED LINKS</span></span>
