---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 5d3f9212fcaf55d6506723b6c29ed1da0d676bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529155"
---
# <span data-ttu-id="83074-101">Get-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="83074-101">Get-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="83074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83074-102">SYNOPSIS</span></span>
<span data-ttu-id="83074-103">지정 된 Service Bus 큐에 대해 지정한 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83074-103">Gets the description of a specified authorization rule for a given Service Bus queue.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83074-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83074-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83074-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83074-105">DESCRIPTION</span></span>
<span data-ttu-id="83074-106">**AzureRmServiceBusQueueAuthorizationRule** cmdlet은 지정 된 Service Bus 큐에 대해 지정한 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83074-106">The **Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet gets the description of a specified authorization rule on the given Service Bus queue.</span></span>

## <span data-ttu-id="83074-107">예제의</span><span class="sxs-lookup"><span data-stu-id="83074-107">EXAMPLES</span></span>

### <span data-ttu-id="83074-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="83074-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="83074-109">지정 된 Service Bus 큐에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="83074-109">Returns the specified authorization rule description for a given Service Bus queue.</span></span>

## <span data-ttu-id="83074-110">변수</span><span class="sxs-lookup"><span data-stu-id="83074-110">PARAMETERS</span></span>

### <span data-ttu-id="83074-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="83074-111">-ResourceGroup</span></span>
<span data-ttu-id="83074-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83074-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="83074-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83074-113">-DefaultProfile</span></span>
<span data-ttu-id="83074-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83074-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83074-115">-이름</span><span class="sxs-lookup"><span data-stu-id="83074-115">-Name</span></span>
<span data-ttu-id="83074-116">EventHub AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83074-116">EventHub AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83074-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="83074-117">-Namespace</span></span>
<span data-ttu-id="83074-118">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83074-118">Namespace Name.</span></span>

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

### <span data-ttu-id="83074-119">-큐</span><span class="sxs-lookup"><span data-stu-id="83074-119">-Queue</span></span>
<span data-ttu-id="83074-120">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83074-120">Queue Name.</span></span>

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

### <span data-ttu-id="83074-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83074-121">CommonParameters</span></span>
<span data-ttu-id="83074-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83074-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83074-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83074-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83074-124">입력</span><span class="sxs-lookup"><span data-stu-id="83074-124">INPUTS</span></span>

### <span data-ttu-id="83074-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="83074-125">-ResourceGroup</span></span>
 <span data-ttu-id="83074-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="83074-126">System.String</span></span>
 

### <span data-ttu-id="83074-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="83074-127">-NamespaceName</span></span>
 <span data-ttu-id="83074-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="83074-128">System.String</span></span>
 

### <span data-ttu-id="83074-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="83074-129">-QueueName</span></span>
 <span data-ttu-id="83074-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="83074-130">System.String</span></span>
 

### <span data-ttu-id="83074-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="83074-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="83074-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="83074-132">System.String</span></span>

## <span data-ttu-id="83074-133">출력</span><span class="sxs-lookup"><span data-stu-id="83074-133">OUTPUTS</span></span>

### <span data-ttu-id="83074-134">System.webserver. List ' 1 [[ServiceBus]. ServiceBus, Version = 0.0.1.0, Culture = 중립, PublicKeyToken = null]). 목록 ' ' [[Microsoft Azure.]</span><span class="sxs-lookup"><span data-stu-id="83074-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="83074-135">Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules 이름: SBAuthoRule1 Location: 서쪽 US 태그: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="83074-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="83074-136">상속자</span><span class="sxs-lookup"><span data-stu-id="83074-136">NOTES</span></span>

## <span data-ttu-id="83074-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83074-137">RELATED LINKS</span></span>

