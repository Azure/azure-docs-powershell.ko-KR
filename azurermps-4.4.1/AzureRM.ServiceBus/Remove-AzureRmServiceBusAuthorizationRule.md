---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 7722ee1a84aee6ef16642a84ac9f72f259d9772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702408"
---
# <span data-ttu-id="c7a53-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c7a53-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="c7a53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a53-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a53-103">지정 된 리소스 그룹에서 Service Bus 네임 스페이스 또는 큐 또는 주제의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7a53-104">SYNTAX</span></span>

### <span data-ttu-id="c7a53-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c7a53-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c7a53-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="c7a53-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Queue] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c7a53-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c7a53-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Topic] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c7a53-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c7a53-108">DESCRIPTION</span></span>
<span data-ttu-id="c7a53-109">**AzureRmServiceBusAuthorizationRule** cmdlet은 지정 된 리소스 그룹에 대 한 Service Bus 네임 스페이스 또는 큐 또는 항목의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="c7a53-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c7a53-110">EXAMPLES</span></span>

### <span data-ttu-id="c7a53-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7a53-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```
<span data-ttu-id="c7a53-112">`SBAuthoRule1`지정 된 리소스 그룹에서 네임 스페이스의 권한 부여 규칙을 제거 `SB-Example1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="c7a53-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c7a53-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```
<span data-ttu-id="c7a53-114">`SBAuthoRule1`지정 된 리소스 그룹에서 큐의 권한 부여 규칙을 제거 `SBQueue` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="c7a53-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="c7a53-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```
<span data-ttu-id="c7a53-116">지정 된 리소스 그룹의 주제에 대 한 권한 부여 규칙을 제거 `SBAuthoRule1` `SBTopic` 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="c7a53-117">변수</span><span class="sxs-lookup"><span data-stu-id="c7a53-117">PARAMETERS</span></span>

### <span data-ttu-id="c7a53-118">-확인</span><span class="sxs-lookup"><span data-stu-id="c7a53-118">-Confirm</span></span>
<span data-ttu-id="c7a53-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a53-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c7a53-120">-Force</span></span>
<span data-ttu-id="c7a53-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a53-122">-이름</span><span class="sxs-lookup"><span data-stu-id="c7a53-122">-Name</span></span>
<span data-ttu-id="c7a53-123">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c7a53-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c7a53-124">-Namespace</span></span>
<span data-ttu-id="c7a53-125">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a53-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7a53-126">-PassThru</span></span>
<span data-ttu-id="c7a53-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="c7a53-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a53-128">-큐</span><span class="sxs-lookup"><span data-stu-id="c7a53-128">-Queue</span></span>
<span data-ttu-id="c7a53-129">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-129">Queue Name.</span></span>

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

### <span data-ttu-id="c7a53-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a53-130">-ResourceGroupName</span></span>
<span data-ttu-id="c7a53-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7a53-132">-주제</span><span class="sxs-lookup"><span data-stu-id="c7a53-132">-Topic</span></span>
<span data-ttu-id="c7a53-133">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-133">Topic Name.</span></span>

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

### <span data-ttu-id="c7a53-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a53-134">-WhatIf</span></span>
<span data-ttu-id="c7a53-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7a53-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7a53-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="c7a53-137">입력</span><span class="sxs-lookup"><span data-stu-id="c7a53-137">INPUTS</span></span>

### <span data-ttu-id="c7a53-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7a53-138">System.String</span></span>


## <span data-ttu-id="c7a53-139">출력</span><span class="sxs-lookup"><span data-stu-id="c7a53-139">OUTPUTS</span></span>

### <span data-ttu-id="c7a53-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c7a53-140">System.Boolean</span></span>


## <span data-ttu-id="c7a53-141">상속자</span><span class="sxs-lookup"><span data-stu-id="c7a53-141">NOTES</span></span>

## <span data-ttu-id="c7a53-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7a53-142">RELATED LINKS</span></span>

