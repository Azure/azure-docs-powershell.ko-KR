---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362188"
---
# <span data-ttu-id="1a320-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="1a320-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="1a320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a320-102">SYNOPSIS</span></span>
<span data-ttu-id="1a320-103">Service Bus 네임스페이스 또는 큐 또는 토픽에 대한 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="1a320-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a320-104">SYNTAX</span></span>

### <span data-ttu-id="1a320-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1a320-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a320-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1a320-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a320-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1a320-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a320-108">설명</span><span class="sxs-lookup"><span data-stu-id="1a320-108">DESCRIPTION</span></span>
<span data-ttu-id="1a320-109">**New-AzServiceBusKey** cmdlet은 지정된 네임스페이스 또는 큐 또는 토픽 및 권한 부여 규칙에 대한 새 기본 또는 보조 연결 문자열을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="1a320-110">예제</span><span class="sxs-lookup"><span data-stu-id="1a320-110">EXAMPLES</span></span>

### <span data-ttu-id="1a320-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a320-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="1a320-112">네임스페이스에 대한 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="1a320-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1a320-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="1a320-114">네임스페이스에 제공된 키 값을 사용하여 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="1a320-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="1a320-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="1a320-116">큐에 대한 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="1a320-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="1a320-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="1a320-118">큐에 제공된 키 값을 사용하여 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="1a320-119">예제 5</span><span class="sxs-lookup"><span data-stu-id="1a320-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="1a320-120">토픽에 대한 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="1a320-121">예제 6</span><span class="sxs-lookup"><span data-stu-id="1a320-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="1a320-122">토픽에 제공된 키 값을 사용하여 기본 또는 보조 연결 문자열을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="1a320-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a320-123">PARAMETERS</span></span>

### <span data-ttu-id="1a320-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a320-124">-DefaultProfile</span></span>
<span data-ttu-id="1a320-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a320-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="1a320-126">-KeyValue</span></span>
<span data-ttu-id="1a320-127">SAS 토큰 서명 및 유효성을 검사하기 위한 base64로 인코딩된 256비트 키입니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="1a320-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1a320-128">-Name</span></span>
<span data-ttu-id="1a320-129">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="1a320-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1a320-130">-Namespace</span></span>
<span data-ttu-id="1a320-131">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="1a320-131">Namespace Name</span></span>

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

### <span data-ttu-id="1a320-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="1a320-132">-Queue</span></span>
<span data-ttu-id="1a320-133">큐 이름</span><span class="sxs-lookup"><span data-stu-id="1a320-133">Queue Name</span></span>

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

### <span data-ttu-id="1a320-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="1a320-134">-RegenerateKey</span></span>
<span data-ttu-id="1a320-135">키 다시 생성 - 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="1a320-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="1a320-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a320-136">-ResourceGroupName</span></span>
<span data-ttu-id="1a320-137">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1a320-137">Resource Group Name</span></span>

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

### <span data-ttu-id="1a320-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="1a320-138">-Topic</span></span>
<span data-ttu-id="1a320-139">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="1a320-139">Topic Name</span></span>

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

### <span data-ttu-id="1a320-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a320-140">-Confirm</span></span>
<span data-ttu-id="1a320-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a320-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a320-142">-WhatIf</span></span>
<span data-ttu-id="1a320-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1a320-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a320-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a320-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a320-145">CommonParameters</span></span>
<span data-ttu-id="1a320-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a320-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a320-147">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1a320-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a320-148">입력</span><span class="sxs-lookup"><span data-stu-id="1a320-148">INPUTS</span></span>

### <span data-ttu-id="1a320-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1a320-149">System.String</span></span>

## <span data-ttu-id="1a320-150">출력</span><span class="sxs-lookup"><span data-stu-id="1a320-150">OUTPUTS</span></span>

### <span data-ttu-id="1a320-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="1a320-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="1a320-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a320-152">NOTES</span></span>

## <span data-ttu-id="1a320-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a320-153">RELATED LINKS</span></span>
