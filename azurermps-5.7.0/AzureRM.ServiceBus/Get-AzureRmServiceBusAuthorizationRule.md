---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: e5a4886eef132f0e48c146fa70889dfa283489b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528809"
---
# <span data-ttu-id="e0568-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e0568-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="e0568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0568-102">SYNOPSIS</span></span>
<span data-ttu-id="e0568-103">지정 된 네임 스페이스 또는 큐 또는 항목 또는 별칭 (GeoDR 구성)에 대해 지정 된 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0568-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 


[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0568-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0568-104">SYNTAX</span></span>

### <span data-ttu-id="e0568-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e0568-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0568-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="e0568-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0568-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0568-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0568-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0568-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-AliasName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0568-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e0568-109">DESCRIPTION</span></span>
<span data-ttu-id="e0568-110">**AzureRmServiceBusAuthorizationRule** cmdlet은 지정 된 네임 스페이스 또는 큐 또는 항목 또는 별칭 (Geodr 구성)에서 지정한 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0568-110">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="e0568-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e0568-111">EXAMPLES</span></span>

### <span data-ttu-id="e0568-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e0568-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="e0568-113">지정 된 네임 스페이스에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0568-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="e0568-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="e0568-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="e0568-115">지정 된 큐에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0568-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="e0568-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="e0568-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="e0568-117">지정 된 항목에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0568-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="e0568-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="e0568-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="e0568-119">지정한 네임 스페이스 및 별칭에 대해 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0568-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="e0568-120">변수</span><span class="sxs-lookup"><span data-stu-id="e0568-120">PARAMETERS</span></span>

### <span data-ttu-id="e0568-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e0568-121">-AliasName</span></span>
<span data-ttu-id="e0568-122">GeoDR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="e0568-122">GeoDR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0568-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0568-123">-DefaultProfile</span></span>
<span data-ttu-id="e0568-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0568-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0568-125">-이름</span><span class="sxs-lookup"><span data-stu-id="e0568-125">-Name</span></span>
<span data-ttu-id="e0568-126">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="e0568-126">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0568-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e0568-127">-Namespace</span></span>
<span data-ttu-id="e0568-128">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="e0568-128">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0568-129">-큐</span><span class="sxs-lookup"><span data-stu-id="e0568-129">-Queue</span></span>
<span data-ttu-id="e0568-130">큐 이름</span><span class="sxs-lookup"><span data-stu-id="e0568-130">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0568-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0568-131">-ResourceGroupName</span></span>
<span data-ttu-id="e0568-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e0568-132">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0568-133">-주제</span><span class="sxs-lookup"><span data-stu-id="e0568-133">-Topic</span></span>
<span data-ttu-id="e0568-134">주제 이름</span><span class="sxs-lookup"><span data-stu-id="e0568-134">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0568-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0568-135">CommonParameters</span></span>
<span data-ttu-id="e0568-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0568-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e0568-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0568-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0568-138">입력</span><span class="sxs-lookup"><span data-stu-id="e0568-138">INPUTS</span></span>

### <span data-ttu-id="e0568-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e0568-139">System.String</span></span>


## <span data-ttu-id="e0568-140">출력</span><span class="sxs-lookup"><span data-stu-id="e0568-140">OUTPUTS</span></span>

### <span data-ttu-id="e0568-141">System.webserver. List ' 1 [[ServiceBus]. PSSharedAccessAuthorizationRuleAttributes, Microsoft Azure. ServiceBus, Version = 0.5.0.0, Culture = 중립, PublicKeyToken = null])</span><span class="sxs-lookup"><span data-stu-id="e0568-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="e0568-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e0568-142">NOTES</span></span>

## <span data-ttu-id="e0568-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0568-143">RELATED LINKS</span></span>
