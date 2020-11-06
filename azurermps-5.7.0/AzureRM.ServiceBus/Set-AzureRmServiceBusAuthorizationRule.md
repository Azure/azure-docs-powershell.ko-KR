---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 3d5c1b6b80ff4d2b046b8a4b23adf7407f680e6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532631"
---
# <span data-ttu-id="3d6cf-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d6cf-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="3d6cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6cf-103">지정 된 Service Bus 네임 스페이스 또는 큐 또는 항목에 대해 지정한 권한 부여 규칙 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d6cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d6cf-104">SYNTAX</span></span>

### <span data-ttu-id="3d6cf-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3d6cf-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6cf-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="3d6cf-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6cf-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d6cf-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d6cf-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3d6cf-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d6cf-109">설명은</span><span class="sxs-lookup"><span data-stu-id="3d6cf-109">DESCRIPTION</span></span>
<span data-ttu-id="3d6cf-110">**AzureRmServiceBusAuthorizationRule** cmdlet은 지정 된 Service Bus 네임 스페이스 또는 큐 또는 항목에 있는 지정한 권한 부여 규칙에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-110">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="3d6cf-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3d6cf-111">EXAMPLES</span></span>

### <span data-ttu-id="3d6cf-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3d6cf-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="3d6cf-113">네임 스페이스의 권한 부여 규칙에 대 한 액세스 권한에서 **관리** 를 제거 합니다 `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="3d6cf-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="3d6cf-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="3d6cf-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="3d6cf-115">큐에 있는 권한 부여 규칙의 액세스 권한에서 **관리** 를 제거 합니다 `AuthoRule1` `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="3d6cf-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="3d6cf-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="3d6cf-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="3d6cf-117">항목의 권한 부여 규칙에 대 한 액세스 권한에서 **관리** 를 제거 합니다 `AuthoRule1` `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="3d6cf-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="3d6cf-118">변수</span><span class="sxs-lookup"><span data-stu-id="3d6cf-118">PARAMETERS</span></span>

### <span data-ttu-id="3d6cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6cf-119">-DefaultProfile</span></span>
<span data-ttu-id="3d6cf-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d6cf-121">-InputObject</span></span>
<span data-ttu-id="3d6cf-122">ServiceBus AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="3d6cf-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cf-123">-이름</span><span class="sxs-lookup"><span data-stu-id="3d6cf-123">-Name</span></span>
<span data-ttu-id="3d6cf-124">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="3d6cf-124">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cf-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d6cf-125">-Namespace</span></span>
<span data-ttu-id="3d6cf-126">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="3d6cf-126">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cf-127">-큐</span><span class="sxs-lookup"><span data-stu-id="3d6cf-127">-Queue</span></span>
<span data-ttu-id="3d6cf-128">큐 이름</span><span class="sxs-lookup"><span data-stu-id="3d6cf-128">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6cf-129">-ResourceGroupName</span></span>
<span data-ttu-id="3d6cf-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3d6cf-130">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cf-131">-권한</span><span class="sxs-lookup"><span data-stu-id="3d6cf-131">-Rights</span></span>
<span data-ttu-id="3d6cf-132">권한 (예: @ ("듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="3d6cf-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cf-133">-주제</span><span class="sxs-lookup"><span data-stu-id="3d6cf-133">-Topic</span></span>
<span data-ttu-id="3d6cf-134">주제 이름</span><span class="sxs-lookup"><span data-stu-id="3d6cf-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cf-135">-확인</span><span class="sxs-lookup"><span data-stu-id="3d6cf-135">-Confirm</span></span>
<span data-ttu-id="3d6cf-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d6cf-137">-WhatIf</span></span>
<span data-ttu-id="3d6cf-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d6cf-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6cf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6cf-140">CommonParameters</span></span>
<span data-ttu-id="3d6cf-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6cf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3d6cf-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6cf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6cf-143">입력</span><span class="sxs-lookup"><span data-stu-id="3d6cf-143">INPUTS</span></span>

### <span data-ttu-id="3d6cf-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d6cf-144">System.String</span></span>
<span data-ttu-id="3d6cf-145">ServiceBus. PSSharedAccessAuthorizationRuleAttributes 시스템. String []</span><span class="sxs-lookup"><span data-stu-id="3d6cf-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="3d6cf-146">출력</span><span class="sxs-lookup"><span data-stu-id="3d6cf-146">OUTPUTS</span></span>

### <span data-ttu-id="3d6cf-147">ServiceBus. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3d6cf-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="3d6cf-148">상속자</span><span class="sxs-lookup"><span data-stu-id="3d6cf-148">NOTES</span></span>

## <span data-ttu-id="3d6cf-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d6cf-149">RELATED LINKS</span></span>
