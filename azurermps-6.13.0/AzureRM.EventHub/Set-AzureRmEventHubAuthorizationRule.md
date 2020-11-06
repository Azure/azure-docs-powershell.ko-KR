---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d77a0a31cdf9e7731346bd70a24533ce7a464c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530339"
---
# <span data-ttu-id="55527-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="55527-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="55527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55527-102">SYNOPSIS</span></span>
<span data-ttu-id="55527-103">이벤트 허브에서 지정 된 권한 부여 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="55527-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55527-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55527-104">SYNTAX</span></span>

### <span data-ttu-id="55527-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="55527-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55527-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="55527-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55527-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="55527-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55527-108">설명은</span><span class="sxs-lookup"><span data-stu-id="55527-108">DESCRIPTION</span></span>
<span data-ttu-id="55527-109">Set-AzureRmEventHubAuthorizationRule cmdlet은 지정 된 이벤트 허브에서 지정 된 권한 부여 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="55527-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="55527-110">예제의</span><span class="sxs-lookup"><span data-stu-id="55527-110">EXAMPLES</span></span>

### <span data-ttu-id="55527-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="55527-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="55527-112">\` \` \` \` 네임 스페이스 MyNamespaceName으로 범위가 지정 된 이벤트 허브 MyEventHubName에 대 한 관리 권한을 부여 하도록 권한 \` 부여 규칙 MyAuthRuleName를 업데이트 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="55527-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="55527-113">변수</span><span class="sxs-lookup"><span data-stu-id="55527-113">PARAMETERS</span></span>

### <span data-ttu-id="55527-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55527-114">-DefaultProfile</span></span>
<span data-ttu-id="55527-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55527-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55527-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="55527-116">-EventHub</span></span>
<span data-ttu-id="55527-117">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="55527-117">EventHub Name</span></span>

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

### <span data-ttu-id="55527-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55527-118">-InputObject</span></span>
<span data-ttu-id="55527-119">AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="55527-119">AuthorizationRule Object</span></span>

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

### <span data-ttu-id="55527-120">-이름</span><span class="sxs-lookup"><span data-stu-id="55527-120">-Name</span></span>
<span data-ttu-id="55527-121">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="55527-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="55527-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="55527-122">-Namespace</span></span>
<span data-ttu-id="55527-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="55527-123">Namespace Name</span></span>

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

### <span data-ttu-id="55527-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55527-124">-ResourceGroupName</span></span>
<span data-ttu-id="55527-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="55527-125">Resource Group Name</span></span>

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

### <span data-ttu-id="55527-126">-권한</span><span class="sxs-lookup"><span data-stu-id="55527-126">-Rights</span></span>
<span data-ttu-id="55527-127">권한 (예: @ ("듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="55527-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="55527-128">-확인</span><span class="sxs-lookup"><span data-stu-id="55527-128">-Confirm</span></span>
<span data-ttu-id="55527-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="55527-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55527-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55527-130">-WhatIf</span></span>
<span data-ttu-id="55527-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55527-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55527-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55527-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55527-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55527-133">CommonParameters</span></span>
<span data-ttu-id="55527-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55527-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55527-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55527-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55527-136">입력</span><span class="sxs-lookup"><span data-stu-id="55527-136">INPUTS</span></span>

### <span data-ttu-id="55527-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="55527-137">System.String</span></span>

### <span data-ttu-id="55527-138">Microsoft. ' EventHub. ' PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="55527-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="55527-139">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="55527-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="55527-140">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="55527-140">System.String[]</span></span>

## <span data-ttu-id="55527-141">출력</span><span class="sxs-lookup"><span data-stu-id="55527-141">OUTPUTS</span></span>

### <span data-ttu-id="55527-142">Microsoft. ' EventHub. ' PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="55527-142">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="55527-143">상속자</span><span class="sxs-lookup"><span data-stu-id="55527-143">NOTES</span></span>

## <span data-ttu-id="55527-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55527-144">RELATED LINKS</span></span>
