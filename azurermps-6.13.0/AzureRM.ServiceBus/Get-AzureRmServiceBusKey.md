---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 96b95a4a6641e3bcfc2c1a18653da4231bee5c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526035"
---
# <span data-ttu-id="8682b-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="8682b-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="8682b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8682b-102">SYNOPSIS</span></span>
<span data-ttu-id="8682b-103">지정 된 네임 스페이스 또는 큐 또는 항목 또는 별칭 (GeoDR 구성)에 대 한 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8682b-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8682b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8682b-104">SYNTAX</span></span>

### <span data-ttu-id="8682b-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8682b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8682b-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="8682b-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8682b-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8682b-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8682b-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="8682b-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8682b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8682b-109">DESCRIPTION</span></span>
<span data-ttu-id="8682b-110">**AzureRmServiceBusKey** cmdlet은 지정 된 네임 스페이스 또는 큐 또는 항목 또는 별칭 (Geodr 구성)에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8682b-110">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="8682b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8682b-111">EXAMPLES</span></span>

### <span data-ttu-id="8682b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8682b-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="8682b-113">지정 된 네임 스페이스에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="8682b-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="8682b-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="8682b-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="8682b-115">지정 된 큐에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="8682b-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="8682b-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="8682b-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="8682b-117">지정 된 항목에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="8682b-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="8682b-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="8682b-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="8682b-119">지정 된 네임 스페이스 및 별칭에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="8682b-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="8682b-120">변수</span><span class="sxs-lookup"><span data-stu-id="8682b-120">PARAMETERS</span></span>

### <span data-ttu-id="8682b-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="8682b-121">-AliasName</span></span>
<span data-ttu-id="8682b-122">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="8682b-122">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8682b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8682b-123">-DefaultProfile</span></span>
<span data-ttu-id="8682b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8682b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8682b-125">-이름</span><span class="sxs-lookup"><span data-stu-id="8682b-125">-Name</span></span>
<span data-ttu-id="8682b-126">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="8682b-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="8682b-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8682b-127">-Namespace</span></span>
<span data-ttu-id="8682b-128">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="8682b-128">Namespace Name</span></span>

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

### <span data-ttu-id="8682b-129">-큐</span><span class="sxs-lookup"><span data-stu-id="8682b-129">-Queue</span></span>
<span data-ttu-id="8682b-130">큐 이름</span><span class="sxs-lookup"><span data-stu-id="8682b-130">Queue Name</span></span>

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

### <span data-ttu-id="8682b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8682b-131">-ResourceGroupName</span></span>
<span data-ttu-id="8682b-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8682b-132">Resource Group Name</span></span>

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

### <span data-ttu-id="8682b-133">-주제</span><span class="sxs-lookup"><span data-stu-id="8682b-133">-Topic</span></span>
<span data-ttu-id="8682b-134">주제 이름</span><span class="sxs-lookup"><span data-stu-id="8682b-134">Topic Name</span></span>

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

### <span data-ttu-id="8682b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8682b-135">CommonParameters</span></span>
<span data-ttu-id="8682b-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8682b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8682b-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8682b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8682b-138">입력</span><span class="sxs-lookup"><span data-stu-id="8682b-138">INPUTS</span></span>

### <span data-ttu-id="8682b-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8682b-139">System.String</span></span>

## <span data-ttu-id="8682b-140">출력</span><span class="sxs-lookup"><span data-stu-id="8682b-140">OUTPUTS</span></span>

### <span data-ttu-id="8682b-141">ServiceBus. PSListKeysAttributes/.</span><span class="sxs-lookup"><span data-stu-id="8682b-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="8682b-142">상속자</span><span class="sxs-lookup"><span data-stu-id="8682b-142">NOTES</span></span>

## <span data-ttu-id="8682b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8682b-143">RELATED LINKS</span></span>
