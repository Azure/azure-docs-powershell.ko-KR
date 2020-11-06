---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: e8bcb3688aec6d718c192e4dac4b6b4632eba059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535436"
---
# <span data-ttu-id="b163a-101">Get-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b163a-101">Get-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="b163a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b163a-102">SYNOPSIS</span></span>
<span data-ttu-id="b163a-103">주어진 주제에 대 한 지정 된 권한 부여 규칙 설명에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b163a-103">Returns the description of the specified authorization rule description for the given topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b163a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b163a-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b163a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b163a-105">DESCRIPTION</span></span>
<span data-ttu-id="b163a-106">**AzureRmServiceBusTopicAuthorizationRule** cmdlet은 지정 된 Service Bus 항목에 대해 지정한 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b163a-106">The **Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet gets the description of the specified authorization rule on the given Service Bus topic.</span></span>

## <span data-ttu-id="b163a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b163a-107">EXAMPLES</span></span>

### <span data-ttu-id="b163a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b163a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_example1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="b163a-109">주어진 주제에 대해 지정 된 권한 부여 규칙에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b163a-109">Returns the description of the specified authorization rule for the given topic.</span></span>

## <span data-ttu-id="b163a-110">변수</span><span class="sxs-lookup"><span data-stu-id="b163a-110">PARAMETERS</span></span>

### <span data-ttu-id="b163a-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b163a-111">-ResourceGroup</span></span>
<span data-ttu-id="b163a-112">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b163a-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="b163a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b163a-113">-DefaultProfile</span></span>
<span data-ttu-id="b163a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b163a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b163a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b163a-115">-Name</span></span>
<span data-ttu-id="b163a-116">주제 AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b163a-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b163a-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b163a-117">-Namespace</span></span>
<span data-ttu-id="b163a-118">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b163a-118">Namespace Name.</span></span>

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

### <span data-ttu-id="b163a-119">-주제</span><span class="sxs-lookup"><span data-stu-id="b163a-119">-Topic</span></span>
<span data-ttu-id="b163a-120">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b163a-120">Topic Name.</span></span>

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

### <span data-ttu-id="b163a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b163a-121">CommonParameters</span></span>
<span data-ttu-id="b163a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b163a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b163a-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b163a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b163a-124">입력</span><span class="sxs-lookup"><span data-stu-id="b163a-124">INPUTS</span></span>

### <span data-ttu-id="b163a-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b163a-125">-ResourceGroup</span></span>
 <span data-ttu-id="b163a-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b163a-126">System.String</span></span>
 

### <span data-ttu-id="b163a-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b163a-127">-NamespaceName</span></span>
 <span data-ttu-id="b163a-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b163a-128">System.String</span></span>
 

### <span data-ttu-id="b163a-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="b163a-129">-TopicName</span></span>
 <span data-ttu-id="b163a-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b163a-130">System.String</span></span>
 

### <span data-ttu-id="b163a-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b163a-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="b163a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b163a-132">System.String</span></span>

## <span data-ttu-id="b163a-133">출력</span><span class="sxs-lookup"><span data-stu-id="b163a-133">OUTPUTS</span></span>

### <span data-ttu-id="b163a-134">System.webserver. List ' 1 [[ServiceBus]. ServiceBus, Version = 0.0.1.0, Culture = 중립, PublicKeyToken = null]). 목록 ' ' [[Microsoft Azure.]</span><span class="sxs-lookup"><span data-stu-id="b163a-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b163a-135">Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules 이름: SBTopicAuthoRule1 Location: 서쪽 US 태그: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="b163a-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="b163a-136">상속자</span><span class="sxs-lookup"><span data-stu-id="b163a-136">NOTES</span></span>

## <span data-ttu-id="b163a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b163a-137">RELATED LINKS</span></span>

