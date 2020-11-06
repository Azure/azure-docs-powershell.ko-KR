---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa7224654581a5c71cb4daafa5dbb96100d63705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536963"
---
# <span data-ttu-id="87e1c-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="87e1c-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="87e1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="87e1c-103">특정 네임 스페이스 또는 큐 또는 항목에 대해 지정 된 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87e1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87e1c-104">SYNTAX</span></span>

### <span data-ttu-id="87e1c-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="87e1c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87e1c-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="87e1c-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87e1c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="87e1c-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87e1c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="87e1c-108">DESCRIPTION</span></span>
<span data-ttu-id="87e1c-109">**AzureRmServiceBusAuthorizationRule** cmdlet은 지정 된 네임 스페이스 또는 큐 또는 항목에서 지정한 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-109">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="87e1c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="87e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="87e1c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="87e1c-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="87e1c-112">지정 된 네임 스페이스에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="87e1c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="87e1c-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="87e1c-114">지정 된 큐에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-114">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="87e1c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="87e1c-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="87e1c-116">지정 된 항목에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-116">Returns the specified authorization rule description for a specified topic.</span></span>

## <span data-ttu-id="87e1c-117">변수</span><span class="sxs-lookup"><span data-stu-id="87e1c-117">PARAMETERS</span></span>

### <span data-ttu-id="87e1c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="87e1c-118">-Name</span></span>
<span data-ttu-id="87e1c-119">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e1c-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="87e1c-120">-Namespace</span></span>
<span data-ttu-id="87e1c-121">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-121">Namespace Name.</span></span>

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

### <span data-ttu-id="87e1c-122">-큐</span><span class="sxs-lookup"><span data-stu-id="87e1c-122">-Queue</span></span>
<span data-ttu-id="87e1c-123">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-123">Queue Name.</span></span>

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

### <span data-ttu-id="87e1c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e1c-124">-ResourceGroupName</span></span>
<span data-ttu-id="87e1c-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="87e1c-126">-주제</span><span class="sxs-lookup"><span data-stu-id="87e1c-126">-Topic</span></span>
<span data-ttu-id="87e1c-127">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-127">Topic Name.</span></span>

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

### <span data-ttu-id="87e1c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e1c-128">-DefaultProfile</span></span>
<span data-ttu-id="87e1c-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87e1c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e1c-130">CommonParameters</span></span>
<span data-ttu-id="87e1c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87e1c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e1c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87e1c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e1c-133">입력</span><span class="sxs-lookup"><span data-stu-id="87e1c-133">INPUTS</span></span>

### <span data-ttu-id="87e1c-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="87e1c-134">System.String</span></span>

## <span data-ttu-id="87e1c-135">출력</span><span class="sxs-lookup"><span data-stu-id="87e1c-135">OUTPUTS</span></span>

### <span data-ttu-id="87e1c-136">System.webserver. List ' 1 [[ServiceBus]. ServiceBus, Version = 0.4.2.0, Culture = 중립, PublicKeyToken = null]). 목록 ' ' [[Microsoft Azure.]</span><span class="sxs-lookup"><span data-stu-id="87e1c-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="87e1c-137">상속자</span><span class="sxs-lookup"><span data-stu-id="87e1c-137">NOTES</span></span>
## <span data-ttu-id="87e1c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87e1c-138">RELATED LINKS</span></span>

## <span data-ttu-id="87e1c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87e1c-139">RELATED LINKS</span></span>

