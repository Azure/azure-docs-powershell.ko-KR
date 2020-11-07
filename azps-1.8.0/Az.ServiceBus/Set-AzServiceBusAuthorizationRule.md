---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e9ab4d4d2fb2c60561d85582f2dda922ba9eaae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699153"
---
# <span data-ttu-id="f38ed-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f38ed-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="f38ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f38ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f38ed-103">지정 된 Service Bus 네임 스페이스 또는 큐 또는 항목에 대해 지정한 권한 부여 규칙 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="f38ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f38ed-104">SYNTAX</span></span>

### <span data-ttu-id="f38ed-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f38ed-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f38ed-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="f38ed-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f38ed-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f38ed-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f38ed-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f38ed-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f38ed-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f38ed-109">DESCRIPTION</span></span>
<span data-ttu-id="f38ed-110">**AzServiceBusAuthorizationRule** cmdlet은 지정 된 Service Bus 네임 스페이스 또는 큐 또는 항목에 있는 지정한 권한 부여 규칙에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="f38ed-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f38ed-111">EXAMPLES</span></span>

### <span data-ttu-id="f38ed-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f38ed-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="f38ed-113">네임 스페이스의 권한 부여 규칙에 대 한 액세스 권한에서 **관리** 를 제거 합니다 `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f38ed-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="f38ed-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f38ed-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="f38ed-115">큐에 있는 권한 부여 규칙의 액세스 권한에서 **관리** 를 제거 합니다 `AuthoRule1` `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="f38ed-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="f38ed-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="f38ed-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="f38ed-117">항목의 권한 부여 규칙에 대 한 액세스 권한에서 **관리** 를 제거 합니다 `AuthoRule1` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="f38ed-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="f38ed-118">변수</span><span class="sxs-lookup"><span data-stu-id="f38ed-118">PARAMETERS</span></span>

### <span data-ttu-id="f38ed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f38ed-119">-DefaultProfile</span></span>
<span data-ttu-id="f38ed-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f38ed-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f38ed-121">-InputObject</span></span>
<span data-ttu-id="f38ed-122">ServiceBus AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="f38ed-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f38ed-123">-이름</span><span class="sxs-lookup"><span data-stu-id="f38ed-123">-Name</span></span>
<span data-ttu-id="f38ed-124">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="f38ed-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f38ed-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f38ed-125">-Namespace</span></span>
<span data-ttu-id="f38ed-126">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="f38ed-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f38ed-127">-큐</span><span class="sxs-lookup"><span data-stu-id="f38ed-127">-Queue</span></span>
<span data-ttu-id="f38ed-128">큐 이름</span><span class="sxs-lookup"><span data-stu-id="f38ed-128">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f38ed-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f38ed-129">-ResourceGroupName</span></span>
<span data-ttu-id="f38ed-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f38ed-130">Resource Group Name</span></span>

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

### <span data-ttu-id="f38ed-131">-권한</span><span class="sxs-lookup"><span data-stu-id="f38ed-131">-Rights</span></span>
<span data-ttu-id="f38ed-132">권한 (예: @ ("듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="f38ed-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f38ed-133">-주제</span><span class="sxs-lookup"><span data-stu-id="f38ed-133">-Topic</span></span>
<span data-ttu-id="f38ed-134">주제 이름</span><span class="sxs-lookup"><span data-stu-id="f38ed-134">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f38ed-135">-확인</span><span class="sxs-lookup"><span data-stu-id="f38ed-135">-Confirm</span></span>
<span data-ttu-id="f38ed-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f38ed-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f38ed-137">-WhatIf</span></span>
<span data-ttu-id="f38ed-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f38ed-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f38ed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f38ed-140">CommonParameters</span></span>
<span data-ttu-id="f38ed-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f38ed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f38ed-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f38ed-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f38ed-143">입력</span><span class="sxs-lookup"><span data-stu-id="f38ed-143">INPUTS</span></span>

### <span data-ttu-id="f38ed-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f38ed-144">System.String</span></span>

### <span data-ttu-id="f38ed-145">ServiceBus. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f38ed-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="f38ed-146">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="f38ed-146">System.String[]</span></span>

## <span data-ttu-id="f38ed-147">출력</span><span class="sxs-lookup"><span data-stu-id="f38ed-147">OUTPUTS</span></span>

### <span data-ttu-id="f38ed-148">ServiceBus. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f38ed-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f38ed-149">상속자</span><span class="sxs-lookup"><span data-stu-id="f38ed-149">NOTES</span></span>

## <span data-ttu-id="f38ed-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f38ed-150">RELATED LINKS</span></span>
