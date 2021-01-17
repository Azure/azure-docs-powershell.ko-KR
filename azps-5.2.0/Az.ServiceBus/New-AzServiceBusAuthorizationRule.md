---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338846"
---
# <span data-ttu-id="020a9-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="020a9-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="020a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="020a9-102">SYNOPSIS</span></span>
<span data-ttu-id="020a9-103">지정된 Service Bus에 대해 지정된 네임스페이스 또는 큐 또는 토픽에 대한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="020a9-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="020a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="020a9-104">SYNTAX</span></span>

### <span data-ttu-id="020a9-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="020a9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="020a9-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="020a9-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="020a9-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="020a9-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="020a9-108">설명</span><span class="sxs-lookup"><span data-stu-id="020a9-108">DESCRIPTION</span></span>
<span data-ttu-id="020a9-109">**New-AzServiceBusAuthorizationRule** cmdlet은 지정된 Service Bus 네임스페이스 또는 큐 또는 토픽에 대한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="020a9-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="020a9-110">예제</span><span class="sxs-lookup"><span data-stu-id="020a9-110">EXAMPLES</span></span>

### <span data-ttu-id="020a9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="020a9-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="020a9-112">`AuthoRule1` **네임스페이스에 대한 수신** 및 **보내기** 권한으로 `SB-Example1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="020a9-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="020a9-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="020a9-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="020a9-114">큐에 `AuthoRule1` **대한 수신** 및 **보내기** 권한을 사용하여 `SBQueue` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="020a9-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="020a9-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="020a9-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="020a9-116">`AuthoRule1`토픽에 대한 수신 **및** **보내기** 권한으로 `SBTopic` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="020a9-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="020a9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="020a9-117">PARAMETERS</span></span>

### <span data-ttu-id="020a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020a9-118">-DefaultProfile</span></span>
<span data-ttu-id="020a9-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="020a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="020a9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="020a9-120">-Name</span></span>
<span data-ttu-id="020a9-121">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="020a9-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="020a9-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="020a9-122">-Namespace</span></span>
<span data-ttu-id="020a9-123">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="020a9-123">Namespace Name</span></span>

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

### <span data-ttu-id="020a9-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="020a9-124">-Queue</span></span>
<span data-ttu-id="020a9-125">큐 이름</span><span class="sxs-lookup"><span data-stu-id="020a9-125">Queue Name</span></span>

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

### <span data-ttu-id="020a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="020a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="020a9-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="020a9-127">Resource Group Name</span></span>

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

### <span data-ttu-id="020a9-128">-Rights</span><span class="sxs-lookup"><span data-stu-id="020a9-128">-Rights</span></span>
<span data-ttu-id="020a9-129">권한, 예: "수신", "보내기", "관리"</span><span class="sxs-lookup"><span data-stu-id="020a9-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="020a9-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="020a9-130">-Topic</span></span>
<span data-ttu-id="020a9-131">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="020a9-131">Topic Name</span></span>

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

### <span data-ttu-id="020a9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="020a9-132">-Confirm</span></span>
<span data-ttu-id="020a9-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="020a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="020a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="020a9-134">-WhatIf</span></span>
<span data-ttu-id="020a9-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="020a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="020a9-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="020a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="020a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020a9-137">CommonParameters</span></span>
<span data-ttu-id="020a9-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="020a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020a9-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="020a9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020a9-140">입력</span><span class="sxs-lookup"><span data-stu-id="020a9-140">INPUTS</span></span>

### <span data-ttu-id="020a9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="020a9-141">System.String</span></span>

### <span data-ttu-id="020a9-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="020a9-142">System.String[]</span></span>

## <span data-ttu-id="020a9-143">출력</span><span class="sxs-lookup"><span data-stu-id="020a9-143">OUTPUTS</span></span>

### <span data-ttu-id="020a9-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="020a9-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="020a9-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="020a9-145">NOTES</span></span>

## <span data-ttu-id="020a9-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="020a9-146">RELATED LINKS</span></span>
