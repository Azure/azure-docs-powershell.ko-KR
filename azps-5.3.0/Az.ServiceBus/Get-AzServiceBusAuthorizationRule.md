---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494897"
---
# <span data-ttu-id="0521a-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0521a-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="0521a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0521a-102">SYNOPSIS</span></span>
<span data-ttu-id="0521a-103">지정된 네임스페이스 또는 큐 또는 토픽 또는 별칭(GeoDR 구성)에 대해 지정된 권한 부여 규칙에 대한 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0521a-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="0521a-104">구문</span><span class="sxs-lookup"><span data-stu-id="0521a-104">SYNTAX</span></span>

### <span data-ttu-id="0521a-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0521a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0521a-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0521a-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0521a-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0521a-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0521a-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="0521a-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0521a-109">설명</span><span class="sxs-lookup"><span data-stu-id="0521a-109">DESCRIPTION</span></span>
<span data-ttu-id="0521a-110">**Get-AzServiceBusAuthorizationRule** cmdlet은 지정된 네임스페이스 또는 큐 또는 토픽 또는 별칭(GeoDR 구성)에서 지정된 권한 부여 규칙에 대한 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0521a-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="0521a-111">예제</span><span class="sxs-lookup"><span data-stu-id="0521a-111">EXAMPLES</span></span>

### <span data-ttu-id="0521a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0521a-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="0521a-113">지정된 네임스페이스에 대해 지정된 권한 부여 규칙 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0521a-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="0521a-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="0521a-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="0521a-115">지정된 큐에 대해 지정된 권한 부여 규칙 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0521a-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="0521a-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="0521a-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="0521a-117">지정된 토픽에 대해 지정된 권한 부여 규칙 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0521a-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="0521a-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="0521a-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="0521a-119">지정된 네임스페이스 및 별칭에 대해 지정된 권한 부여 규칙 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0521a-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="0521a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0521a-120">PARAMETERS</span></span>

### <span data-ttu-id="0521a-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="0521a-121">-AliasName</span></span>
<span data-ttu-id="0521a-122">GeoDR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="0521a-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="0521a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0521a-123">-DefaultProfile</span></span>
<span data-ttu-id="0521a-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0521a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0521a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0521a-125">-Name</span></span>
<span data-ttu-id="0521a-126">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="0521a-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="0521a-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0521a-127">-Namespace</span></span>
<span data-ttu-id="0521a-128">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="0521a-128">Namespace Name</span></span>

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

### <span data-ttu-id="0521a-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="0521a-129">-Queue</span></span>
<span data-ttu-id="0521a-130">큐 이름</span><span class="sxs-lookup"><span data-stu-id="0521a-130">Queue Name</span></span>

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

### <span data-ttu-id="0521a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0521a-131">-ResourceGroupName</span></span>
<span data-ttu-id="0521a-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0521a-132">Resource Group Name</span></span>

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

### <span data-ttu-id="0521a-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="0521a-133">-Topic</span></span>
<span data-ttu-id="0521a-134">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="0521a-134">Topic Name</span></span>

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

### <span data-ttu-id="0521a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0521a-135">CommonParameters</span></span>
<span data-ttu-id="0521a-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0521a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0521a-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0521a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0521a-138">입력</span><span class="sxs-lookup"><span data-stu-id="0521a-138">INPUTS</span></span>

### <span data-ttu-id="0521a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0521a-139">System.String</span></span>

## <span data-ttu-id="0521a-140">출력</span><span class="sxs-lookup"><span data-stu-id="0521a-140">OUTPUTS</span></span>

### <span data-ttu-id="0521a-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0521a-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0521a-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0521a-142">NOTES</span></span>

## <span data-ttu-id="0521a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0521a-143">RELATED LINKS</span></span>
