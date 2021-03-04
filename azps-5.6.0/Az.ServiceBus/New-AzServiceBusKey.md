---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: ac3b98089a3bbb710680269692685a32ef7adc03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950955"
---
# <span data-ttu-id="21fb4-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="21fb4-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="21fb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="21fb4-103">Service Bus 네임스페이스 또는 큐 또는 토픽에 대한 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="21fb4-104">구문</span><span class="sxs-lookup"><span data-stu-id="21fb4-104">SYNTAX</span></span>

### <span data-ttu-id="21fb4-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="21fb4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21fb4-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="21fb4-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21fb4-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="21fb4-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21fb4-108">설명</span><span class="sxs-lookup"><span data-stu-id="21fb4-108">DESCRIPTION</span></span>
<span data-ttu-id="21fb4-109">**New-AzServiceBusKey** cmdlet은 지정된 네임스페이스 또는 큐 또는 토픽 및 권한 부여 규칙에 대한 새 기본 또는 보조 연결 문자열을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="21fb4-110">예제</span><span class="sxs-lookup"><span data-stu-id="21fb4-110">EXAMPLES</span></span>

### <span data-ttu-id="21fb4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="21fb4-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="21fb4-112">네임스페이스에 대한 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="21fb4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="21fb4-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="21fb4-114">네임스페이스에 대해 제공된 키 값을 사용하여 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="21fb4-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="21fb4-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="21fb4-116">큐에 대한 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="21fb4-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="21fb4-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="21fb4-118">큐에 대해 제공된 키 값을 사용하여 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="21fb4-119">예제 5</span><span class="sxs-lookup"><span data-stu-id="21fb4-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="21fb4-120">토픽에 대한 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="21fb4-121">예제 6</span><span class="sxs-lookup"><span data-stu-id="21fb4-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="21fb4-122">토픽에 대해 제공된 키 값을 사용하여 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="21fb4-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="21fb4-123">PARAMETERS</span></span>

### <span data-ttu-id="21fb4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fb4-124">-DefaultProfile</span></span>
<span data-ttu-id="21fb4-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21fb4-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="21fb4-126">-KeyValue</span></span>
<span data-ttu-id="21fb4-127">SAS 토큰 서명 및 유효성을 검사하기 위한 base64-encoded 256비트 키입니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21fb4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="21fb4-128">-Name</span></span>
<span data-ttu-id="21fb4-129">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="21fb4-130">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="21fb4-130">-Namespace</span></span>
<span data-ttu-id="21fb4-131">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="21fb4-131">Namespace Name</span></span>

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

### <span data-ttu-id="21fb4-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="21fb4-132">-Queue</span></span>
<span data-ttu-id="21fb4-133">큐 이름</span><span class="sxs-lookup"><span data-stu-id="21fb4-133">Queue Name</span></span>

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

### <span data-ttu-id="21fb4-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="21fb4-134">-RegenerateKey</span></span>
<span data-ttu-id="21fb4-135">키 다시 생성 - 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="21fb4-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21fb4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21fb4-136">-ResourceGroupName</span></span>
<span data-ttu-id="21fb4-137">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="21fb4-137">Resource Group Name</span></span>

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

### <span data-ttu-id="21fb4-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="21fb4-138">-Topic</span></span>
<span data-ttu-id="21fb4-139">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="21fb4-139">Topic Name</span></span>

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

### <span data-ttu-id="21fb4-140">-확인</span><span class="sxs-lookup"><span data-stu-id="21fb4-140">-Confirm</span></span>
<span data-ttu-id="21fb4-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21fb4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21fb4-142">-WhatIf</span></span>
<span data-ttu-id="21fb4-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21fb4-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21fb4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21fb4-145">CommonParameters</span></span>
<span data-ttu-id="21fb4-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21fb4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21fb4-147">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="21fb4-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21fb4-148">입력</span><span class="sxs-lookup"><span data-stu-id="21fb4-148">INPUTS</span></span>

### <span data-ttu-id="21fb4-149">System.String</span><span class="sxs-lookup"><span data-stu-id="21fb4-149">System.String</span></span>

## <span data-ttu-id="21fb4-150">출력</span><span class="sxs-lookup"><span data-stu-id="21fb4-150">OUTPUTS</span></span>

### <span data-ttu-id="21fb4-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="21fb4-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="21fb4-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21fb4-152">NOTES</span></span>

## <span data-ttu-id="21fb4-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21fb4-153">RELATED LINKS</span></span>
