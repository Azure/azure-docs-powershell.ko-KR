---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 603eb1363e15b58a324f7131dd986a7c84371a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702409"
---
# <span data-ttu-id="7c1b1-101">New-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7c1b1-101">New-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="7c1b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1b1-103">지정 된 Service Bus 항목에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-103">Creates a new authorization rule for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c1b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c1b1-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c1b1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c1b1-105">DESCRIPTION</span></span>
<span data-ttu-id="7c1b1-106">**AzureRmServiceBusTopicAuthorizationRule** cmdlet은 지정 된 Service Bus 항목에 대 한 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-106">The **New-AzureRmServiceBusTopicAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus topic.</span></span>

## <span data-ttu-id="7c1b1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c1b1-107">EXAMPLES</span></span>

### <span data-ttu-id="7c1b1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c1b1-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="7c1b1-109">`SBTopicAuthoRule1`항목에 대 한 **듣기** 및 **보내기** 권한이 있는 권한 부여 규칙을 만듭니다 `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="7c1b1-109">Creates authorization rule `SBTopicAuthoRule1` with **Listen** and **Send** rights for the topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="7c1b1-110">변수</span><span class="sxs-lookup"><span data-stu-id="7c1b1-110">PARAMETERS</span></span>

### <span data-ttu-id="7c1b1-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7c1b1-111">-ResourceGroup</span></span>
<span data-ttu-id="7c1b1-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c1b1-113">-권한</span><span class="sxs-lookup"><span data-stu-id="7c1b1-113">-Rights</span></span>
<span data-ttu-id="7c1b1-114">권한을 부여 합니다. 예를 들어 @ ("수신", "보내기", "관리")</span><span class="sxs-lookup"><span data-stu-id="7c1b1-114">The rights; for example, @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="7c1b1-115">-확인</span><span class="sxs-lookup"><span data-stu-id="7c1b1-115">-Confirm</span></span>
<span data-ttu-id="7c1b1-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c1b1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c1b1-117">-WhatIf</span></span>
<span data-ttu-id="7c1b1-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c1b1-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c1b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c1b1-120">-DefaultProfile</span></span>
<span data-ttu-id="7c1b1-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c1b1-122">-이름</span><span class="sxs-lookup"><span data-stu-id="7c1b1-122">-Name</span></span>
<span data-ttu-id="7c1b1-123">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7c1b1-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7c1b1-124">-Namespace</span></span>
<span data-ttu-id="7c1b1-125">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-125">Namespace Name.</span></span>

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

### <span data-ttu-id="7c1b1-126">-주제</span><span class="sxs-lookup"><span data-stu-id="7c1b1-126">-Topic</span></span>
<span data-ttu-id="7c1b1-127">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-127">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c1b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1b1-128">CommonParameters</span></span>
<span data-ttu-id="7c1b1-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1b1-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c1b1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1b1-131">입력</span><span class="sxs-lookup"><span data-stu-id="7c1b1-131">INPUTS</span></span>

### <span data-ttu-id="7c1b1-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7c1b1-132">-ResourceGroup</span></span>
 <span data-ttu-id="7c1b1-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c1b1-133">System.String</span></span>
 

### <span data-ttu-id="7c1b1-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7c1b1-134">-NamespaceName</span></span>
 <span data-ttu-id="7c1b1-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c1b1-135">System.String</span></span>
 

### <span data-ttu-id="7c1b1-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7c1b1-136">-TopicName</span></span>
 <span data-ttu-id="7c1b1-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c1b1-137">System.String</span></span>
 

### <span data-ttu-id="7c1b1-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="7c1b1-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="7c1b1-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c1b1-139">System.String</span></span>

## <span data-ttu-id="7c1b1-140">출력</span><span class="sxs-lookup"><span data-stu-id="7c1b1-140">OUTPUTS</span></span>

### <span data-ttu-id="7c1b1-141">ServiceBus. SharedAccessAuthorizationRuleAttributes 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c1b1-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="7c1b1-142">Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules 이름: SBTopicAuthoRule1 Location: 서쪽 US 태그: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="7c1b1-142">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="7c1b1-143">상속자</span><span class="sxs-lookup"><span data-stu-id="7c1b1-143">NOTES</span></span>

## <span data-ttu-id="7c1b1-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c1b1-144">RELATED LINKS</span></span>

