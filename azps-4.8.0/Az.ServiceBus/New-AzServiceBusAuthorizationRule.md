---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213321"
---
# <span data-ttu-id="09e31-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="09e31-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="09e31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09e31-102">SYNOPSIS</span></span>
<span data-ttu-id="09e31-103">지정 된 서비스 버스 네임 스페이스 또는 큐 또는 항목에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09e31-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="09e31-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09e31-104">SYNTAX</span></span>

### <span data-ttu-id="09e31-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="09e31-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09e31-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="09e31-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09e31-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="09e31-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09e31-108">설명은</span><span class="sxs-lookup"><span data-stu-id="09e31-108">DESCRIPTION</span></span>
<span data-ttu-id="09e31-109">**AzServiceBusAuthorizationRule** cmdlet은 지정 된 Service Bus 네임 스페이스 또는 큐 또는 항목에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09e31-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="09e31-110">예제의</span><span class="sxs-lookup"><span data-stu-id="09e31-110">EXAMPLES</span></span>

### <span data-ttu-id="09e31-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="09e31-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="09e31-112">`AuthoRule1`네임 스페이스에 대 한 **수신** 및 **보내기** 권한을 사용 하 여 만듭니다 `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="09e31-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="09e31-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="09e31-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="09e31-114">`AuthoRule1`큐에 대 한 **수신 대기** 및 **보내기** 권한을 사용 하 여 만듭니다 `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="09e31-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="09e31-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="09e31-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="09e31-116">`AuthoRule1`항목에 대 한 **듣기** 및 **보내기** 권한을 사용 하 여 만듭니다 `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="09e31-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="09e31-117">변수</span><span class="sxs-lookup"><span data-stu-id="09e31-117">PARAMETERS</span></span>

### <span data-ttu-id="09e31-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e31-118">-DefaultProfile</span></span>
<span data-ttu-id="09e31-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09e31-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09e31-120">-이름</span><span class="sxs-lookup"><span data-stu-id="09e31-120">-Name</span></span>
<span data-ttu-id="09e31-121">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="09e31-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="09e31-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="09e31-122">-Namespace</span></span>
<span data-ttu-id="09e31-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="09e31-123">Namespace Name</span></span>

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

### <span data-ttu-id="09e31-124">-큐</span><span class="sxs-lookup"><span data-stu-id="09e31-124">-Queue</span></span>
<span data-ttu-id="09e31-125">큐 이름</span><span class="sxs-lookup"><span data-stu-id="09e31-125">Queue Name</span></span>

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

### <span data-ttu-id="09e31-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e31-126">-ResourceGroupName</span></span>
<span data-ttu-id="09e31-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="09e31-127">Resource Group Name</span></span>

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

### <span data-ttu-id="09e31-128">-권한</span><span class="sxs-lookup"><span data-stu-id="09e31-128">-Rights</span></span>
<span data-ttu-id="09e31-129">권한 (예: "듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="09e31-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="09e31-130">-주제</span><span class="sxs-lookup"><span data-stu-id="09e31-130">-Topic</span></span>
<span data-ttu-id="09e31-131">주제 이름</span><span class="sxs-lookup"><span data-stu-id="09e31-131">Topic Name</span></span>

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

### <span data-ttu-id="09e31-132">-확인</span><span class="sxs-lookup"><span data-stu-id="09e31-132">-Confirm</span></span>
<span data-ttu-id="09e31-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="09e31-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09e31-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09e31-134">-WhatIf</span></span>
<span data-ttu-id="09e31-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="09e31-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09e31-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09e31-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09e31-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e31-137">CommonParameters</span></span>
<span data-ttu-id="09e31-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09e31-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e31-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09e31-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e31-140">입력</span><span class="sxs-lookup"><span data-stu-id="09e31-140">INPUTS</span></span>

### <span data-ttu-id="09e31-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="09e31-141">System.String</span></span>

### <span data-ttu-id="09e31-142">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="09e31-142">System.String[]</span></span>

## <span data-ttu-id="09e31-143">출력</span><span class="sxs-lookup"><span data-stu-id="09e31-143">OUTPUTS</span></span>

### <span data-ttu-id="09e31-144">ServiceBus. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="09e31-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="09e31-145">상속자</span><span class="sxs-lookup"><span data-stu-id="09e31-145">NOTES</span></span>

## <span data-ttu-id="09e31-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09e31-146">RELATED LINKS</span></span>
