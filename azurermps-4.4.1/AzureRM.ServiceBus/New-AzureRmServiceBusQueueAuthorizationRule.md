---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 098c61be4eaf405d3c3a031601b48f20de1e234a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527279"
---
# <span data-ttu-id="c6a11-101">New-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c6a11-101">New-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="c6a11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6a11-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a11-103">지정 된 Service Bus 큐에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-103">Creates a new authorization rule for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6a11-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6a11-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6a11-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c6a11-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a11-106">**AzureRmServiceBusQueueAuthorizationRule** cmdlet은 지정 된 Service Bus 큐에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-106">The **New-AzureRmServiceBusQueueAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus queue.</span></span>

## <span data-ttu-id="c6a11-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c6a11-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a11-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6a11-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="c6a11-109">`SBAuthoRule1`큐에 대 한 **듣기 및 보내기** 권한을 사용 하 여 권한 부여 규칙을 만듭니다 `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="c6a11-109">Creates authorization rule `SBAuthoRule1` with **Listen and Send** rights for the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="c6a11-110">변수</span><span class="sxs-lookup"><span data-stu-id="c6a11-110">PARAMETERS</span></span>

### <span data-ttu-id="c6a11-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6a11-111">-ResourceGroup</span></span>
<span data-ttu-id="c6a11-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6a11-113">-권한</span><span class="sxs-lookup"><span data-stu-id="c6a11-113">-Rights</span></span>
<span data-ttu-id="c6a11-114">권한을 지정 합니다. 예를 들어</span><span class="sxs-lookup"><span data-stu-id="c6a11-114">Specifies the rights; for example,</span></span>  
<span data-ttu-id="c6a11-115">@ ("듣기", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="c6a11-115">@("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a11-116">-확인</span><span class="sxs-lookup"><span data-stu-id="c6a11-116">-Confirm</span></span>
<span data-ttu-id="c6a11-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a11-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6a11-118">-WhatIf</span></span>
<span data-ttu-id="c6a11-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6a11-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a11-121">-DefaultProfile</span></span>
<span data-ttu-id="c6a11-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6a11-123">-이름</span><span class="sxs-lookup"><span data-stu-id="c6a11-123">-Name</span></span>
<span data-ttu-id="c6a11-124">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-124">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a11-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c6a11-125">-Namespace</span></span>
<span data-ttu-id="c6a11-126">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-126">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a11-127">-큐</span><span class="sxs-lookup"><span data-stu-id="c6a11-127">-Queue</span></span>
<span data-ttu-id="c6a11-128">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-128">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6a11-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a11-129">CommonParameters</span></span>
<span data-ttu-id="c6a11-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a11-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a11-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a11-132">입력</span><span class="sxs-lookup"><span data-stu-id="c6a11-132">INPUTS</span></span>

### <span data-ttu-id="c6a11-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c6a11-133">-ResourceGroup</span></span>
 <span data-ttu-id="c6a11-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6a11-134">System.String</span></span>
 

### <span data-ttu-id="c6a11-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c6a11-135">-NamespaceName</span></span>
 <span data-ttu-id="c6a11-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6a11-136">System.String</span></span>
 

### <span data-ttu-id="c6a11-137">-QueueName</span><span class="sxs-lookup"><span data-stu-id="c6a11-137">-QueueName</span></span>
 <span data-ttu-id="c6a11-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6a11-138">System.String</span></span>
 

### <span data-ttu-id="c6a11-139">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="c6a11-139">-AuthorizationRuleName</span></span>
 <span data-ttu-id="c6a11-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6a11-140">System.String</span></span>

## <span data-ttu-id="c6a11-141">출력</span><span class="sxs-lookup"><span data-stu-id="c6a11-141">OUTPUTS</span></span>

### <span data-ttu-id="c6a11-142">ServiceBus. SharedAccessAuthorizationRuleAttributes 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6a11-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="c6a11-143">Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules 이름: SBAuthoRule1 Location: 서쪽 US 태그: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="c6a11-143">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="c6a11-144">상속자</span><span class="sxs-lookup"><span data-stu-id="c6a11-144">NOTES</span></span>

## <span data-ttu-id="c6a11-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6a11-145">RELATED LINKS</span></span>

