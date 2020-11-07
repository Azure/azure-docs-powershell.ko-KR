---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0483c60a1624374dc3e5b750439d905f19ceb2fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710948"
---
# <span data-ttu-id="042f1-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="042f1-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="042f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="042f1-102">SYNOPSIS</span></span>
<span data-ttu-id="042f1-103">Service Bus 네임 스페이스 또는 큐 또는 항목에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="042f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="042f1-104">SYNTAX</span></span>

### <span data-ttu-id="042f1-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="042f1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="042f1-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="042f1-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="042f1-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="042f1-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="042f1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="042f1-108">DESCRIPTION</span></span>
<span data-ttu-id="042f1-109">**AzureRmServiceBusKey** cmdlet은 지정 된 네임 스페이스 또는 큐 또는 항목 및 권한 부여 규칙에 대 한 새 기본 또는 보조 연결 문자열을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="042f1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="042f1-110">EXAMPLES</span></span>

### <span data-ttu-id="042f1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="042f1-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="042f1-112">네임 스페이스에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="042f1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="042f1-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="042f1-114">큐에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="042f1-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="042f1-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="042f1-116">주제에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="042f1-117">변수</span><span class="sxs-lookup"><span data-stu-id="042f1-117">PARAMETERS</span></span>

### <span data-ttu-id="042f1-118">-확인</span><span class="sxs-lookup"><span data-stu-id="042f1-118">-Confirm</span></span>
<span data-ttu-id="042f1-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="042f1-120">-이름</span><span class="sxs-lookup"><span data-stu-id="042f1-120">-Name</span></span>
<span data-ttu-id="042f1-121">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="042f1-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="042f1-122">-Namespace</span></span>
<span data-ttu-id="042f1-123">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-123">Namespace Name.</span></span>

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

### <span data-ttu-id="042f1-124">-큐</span><span class="sxs-lookup"><span data-stu-id="042f1-124">-Queue</span></span>
<span data-ttu-id="042f1-125">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-125">Queue Name.</span></span>

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

### <span data-ttu-id="042f1-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="042f1-126">-RegenerateKey</span></span>
<span data-ttu-id="042f1-127">' PrimaryKey '/' SecondaryKey ' 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="042f1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="042f1-128">-ResourceGroupName</span></span>
<span data-ttu-id="042f1-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="042f1-130">-주제</span><span class="sxs-lookup"><span data-stu-id="042f1-130">-Topic</span></span>
<span data-ttu-id="042f1-131">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-131">Topic Name.</span></span>

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

### <span data-ttu-id="042f1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="042f1-132">-WhatIf</span></span>
<span data-ttu-id="042f1-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="042f1-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="042f1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="042f1-135">-DefaultProfile</span></span>
<span data-ttu-id="042f1-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="042f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042f1-137">CommonParameters</span></span>
<span data-ttu-id="042f1-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="042f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="042f1-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="042f1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042f1-140">입력</span><span class="sxs-lookup"><span data-stu-id="042f1-140">INPUTS</span></span>

### <span data-ttu-id="042f1-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="042f1-141">System.String</span></span>

## <span data-ttu-id="042f1-142">출력</span><span class="sxs-lookup"><span data-stu-id="042f1-142">OUTPUTS</span></span>

### <span data-ttu-id="042f1-143">ServiceBus. ListKeysAttributes/.</span><span class="sxs-lookup"><span data-stu-id="042f1-143">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="042f1-144">상속자</span><span class="sxs-lookup"><span data-stu-id="042f1-144">NOTES</span></span>

## <span data-ttu-id="042f1-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="042f1-145">RELATED LINKS</span></span>

