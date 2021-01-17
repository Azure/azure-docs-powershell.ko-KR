---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: da981d38f0833adc276a114c42def5d19322e0d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494836"
---
# <span data-ttu-id="f8488-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f8488-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="f8488-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8488-102">SYNOPSIS</span></span>
<span data-ttu-id="f8488-103">지정된 Service Bus 네임스페이스 또는 큐 또는 토픽에 대해 지정된 권한 부여 규칙 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f8488-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="f8488-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8488-104">SYNTAX</span></span>

### <span data-ttu-id="f8488-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f8488-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8488-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8488-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8488-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8488-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8488-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f8488-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8488-109">설명</span><span class="sxs-lookup"><span data-stu-id="f8488-109">DESCRIPTION</span></span>
<span data-ttu-id="f8488-110">**Set-AzServiceBusAuthorizationRule** cmdlet은 지정된 Service Bus 네임스페이스 또는 큐 또는 토픽에서 지정된 권한 부여 규칙에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f8488-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="f8488-111">예제</span><span class="sxs-lookup"><span data-stu-id="f8488-111">EXAMPLES</span></span>

### <span data-ttu-id="f8488-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8488-112">Example 1</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="f8488-113">**네임스페이스에서** 권한 부여 규칙의 액세스 권한에서 `AuthoRule1` 관리를 `SB-Example1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f8488-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="f8488-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f8488-114">Example 2</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="f8488-115">큐에서 **권한** 부여 규칙의 액세스 권한에서 `AuthoRule1` 관리 `SBQueue` 제거.</span><span class="sxs-lookup"><span data-stu-id="f8488-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="f8488-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="f8488-116">Example 3</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="f8488-117">**토픽의** 권한 부여 규칙 액세스 권한에서 `AuthoRule1` 관리 `SBTopic` 제거.</span><span class="sxs-lookup"><span data-stu-id="f8488-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="f8488-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8488-118">PARAMETERS</span></span>

### <span data-ttu-id="f8488-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8488-119">-DefaultProfile</span></span>
<span data-ttu-id="f8488-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8488-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8488-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8488-121">-InputObject</span></span>
<span data-ttu-id="f8488-122">ServiceBus AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="f8488-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="f8488-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f8488-123">-Name</span></span>
<span data-ttu-id="f8488-124">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="f8488-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="f8488-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f8488-125">-Namespace</span></span>
<span data-ttu-id="f8488-126">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="f8488-126">Namespace Name</span></span>

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

### <span data-ttu-id="f8488-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="f8488-127">-Queue</span></span>
<span data-ttu-id="f8488-128">큐 이름</span><span class="sxs-lookup"><span data-stu-id="f8488-128">Queue Name</span></span>

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

### <span data-ttu-id="f8488-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8488-129">-ResourceGroupName</span></span>
<span data-ttu-id="f8488-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f8488-130">Resource Group Name</span></span>

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

### <span data-ttu-id="f8488-131">-Rights</span><span class="sxs-lookup"><span data-stu-id="f8488-131">-Rights</span></span>
<span data-ttu-id="f8488-132">권한, 예: @("수신","보내기","관리")</span><span class="sxs-lookup"><span data-stu-id="f8488-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="f8488-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="f8488-133">-Topic</span></span>
<span data-ttu-id="f8488-134">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="f8488-134">Topic Name</span></span>

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

### <span data-ttu-id="f8488-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8488-135">-Confirm</span></span>
<span data-ttu-id="f8488-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8488-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8488-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8488-137">-WhatIf</span></span>
<span data-ttu-id="f8488-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f8488-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8488-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8488-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8488-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8488-140">CommonParameters</span></span>
<span data-ttu-id="f8488-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8488-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8488-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f8488-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8488-143">입력</span><span class="sxs-lookup"><span data-stu-id="f8488-143">INPUTS</span></span>

### <span data-ttu-id="f8488-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f8488-144">System.String</span></span>

### <span data-ttu-id="f8488-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f8488-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="f8488-146">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f8488-146">System.String[]</span></span>

## <span data-ttu-id="f8488-147">출력</span><span class="sxs-lookup"><span data-stu-id="f8488-147">OUTPUTS</span></span>

### <span data-ttu-id="f8488-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f8488-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f8488-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8488-149">NOTES</span></span>

## <span data-ttu-id="f8488-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8488-150">RELATED LINKS</span></span>
