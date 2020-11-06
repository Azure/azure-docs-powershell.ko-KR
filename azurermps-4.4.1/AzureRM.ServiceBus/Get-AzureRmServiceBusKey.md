---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 28abf3ff725f5a1b124f99c96b46d03458b42f8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527300"
---
# <span data-ttu-id="f9deb-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="f9deb-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="f9deb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9deb-102">SYNOPSIS</span></span>
<span data-ttu-id="f9deb-103">지정 된 네임 스페이스 또는 큐 또는 항목에 대 한 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9deb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9deb-104">SYNTAX</span></span>

### <span data-ttu-id="f9deb-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f9deb-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9deb-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="f9deb-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9deb-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f9deb-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9deb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f9deb-108">DESCRIPTION</span></span>
<span data-ttu-id="f9deb-109">**AzureRmServiceBusKey** cmdlet은 지정 된 네임 스페이스 또는 큐 또는 항목에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-109">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span> 

## <span data-ttu-id="f9deb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f9deb-110">EXAMPLES</span></span>

### <span data-ttu-id="f9deb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9deb-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="f9deb-112">지정 된 네임 스페이스에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-112">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="f9deb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f9deb-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="f9deb-114">지정 된 큐에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-114">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="f9deb-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="f9deb-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="f9deb-116">지정 된 항목에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-116">Primary and secondary connection string to the specified topic.</span></span>

## <span data-ttu-id="f9deb-117">변수</span><span class="sxs-lookup"><span data-stu-id="f9deb-117">PARAMETERS</span></span>

### <span data-ttu-id="f9deb-118">-이름</span><span class="sxs-lookup"><span data-stu-id="f9deb-118">-Name</span></span>
<span data-ttu-id="f9deb-119">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f9deb-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f9deb-120">-Namespace</span></span>
<span data-ttu-id="f9deb-121">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-121">Namespace Name.</span></span>

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

### <span data-ttu-id="f9deb-122">-큐</span><span class="sxs-lookup"><span data-stu-id="f9deb-122">-Queue</span></span>
<span data-ttu-id="f9deb-123">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-123">Queue Name.</span></span>

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

### <span data-ttu-id="f9deb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9deb-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9deb-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9deb-126">-주제</span><span class="sxs-lookup"><span data-stu-id="f9deb-126">-Topic</span></span>
<span data-ttu-id="f9deb-127">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-127">Topic Name.</span></span>

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

### <span data-ttu-id="f9deb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9deb-128">-DefaultProfile</span></span>
<span data-ttu-id="f9deb-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9deb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9deb-130">CommonParameters</span></span>
<span data-ttu-id="f9deb-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9deb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9deb-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9deb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9deb-133">입력</span><span class="sxs-lookup"><span data-stu-id="f9deb-133">INPUTS</span></span>

### <span data-ttu-id="f9deb-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f9deb-134">System.String</span></span>

## <span data-ttu-id="f9deb-135">출력</span><span class="sxs-lookup"><span data-stu-id="f9deb-135">OUTPUTS</span></span>

### <span data-ttu-id="f9deb-136">ServiceBus. ListKeysAttributes/.</span><span class="sxs-lookup"><span data-stu-id="f9deb-136">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="f9deb-137">상속자</span><span class="sxs-lookup"><span data-stu-id="f9deb-137">NOTES</span></span>

## <span data-ttu-id="f9deb-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9deb-138">RELATED LINKS</span></span>

