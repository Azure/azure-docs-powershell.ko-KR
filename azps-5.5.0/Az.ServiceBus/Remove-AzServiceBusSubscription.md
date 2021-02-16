---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: dd0dfb633fd48f2f747d6f4c0eb3471745b40da1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201617"
---
# <span data-ttu-id="46a38-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="46a38-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="46a38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46a38-102">SYNOPSIS</span></span>
<span data-ttu-id="46a38-103">지정된 Service Bus 네임스페이스에서 토픽에 대한 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46a38-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="46a38-104">구문</span><span class="sxs-lookup"><span data-stu-id="46a38-104">SYNTAX</span></span>

### <span data-ttu-id="46a38-105">SubscriptionPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="46a38-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46a38-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="46a38-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46a38-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="46a38-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46a38-108">설명</span><span class="sxs-lookup"><span data-stu-id="46a38-108">DESCRIPTION</span></span>
<span data-ttu-id="46a38-109">**Remove-AzServiceBusSubscription** cmdlet은 지정된 Service Bus 네임스페이스에서 토픽에 대한 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46a38-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="46a38-110">예제</span><span class="sxs-lookup"><span data-stu-id="46a38-110">EXAMPLES</span></span>

### <span data-ttu-id="46a38-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="46a38-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="46a38-112">지정된 Service Bus 네임스페이스의 토픽에 대한 `SB-TopicSubscription-Example1` `SB-Topic_exampl1` 구독을 `SB-Example1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46a38-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="46a38-113">예제 2: InputObject - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="46a38-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="46a38-114">예제 3: InputObject - 파이핑 사용:</span><span class="sxs-lookup"><span data-stu-id="46a38-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="46a38-115">예제 4: ResourceId - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="46a38-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="46a38-116">예제 5: ResourceId - 문자열 값 사용:</span><span class="sxs-lookup"><span data-stu-id="46a38-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="46a38-117">-ResourceId 매개 변수에 대한 ARM/문자열의 $resourceid ID를 통해 제공된 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46a38-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="46a38-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46a38-118">PARAMETERS</span></span>

### <span data-ttu-id="46a38-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46a38-119">-AsJob</span></span>
<span data-ttu-id="46a38-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="46a38-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a38-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a38-121">-DefaultProfile</span></span>
<span data-ttu-id="46a38-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46a38-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46a38-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46a38-123">-InputObject</span></span>
<span data-ttu-id="46a38-124">Service Bus 구독 개체</span><span class="sxs-lookup"><span data-stu-id="46a38-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46a38-125">-Name</span><span class="sxs-lookup"><span data-stu-id="46a38-125">-Name</span></span>
<span data-ttu-id="46a38-126">구독 이름</span><span class="sxs-lookup"><span data-stu-id="46a38-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a38-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="46a38-127">-Namespace</span></span>
<span data-ttu-id="46a38-128">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="46a38-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a38-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46a38-129">-PassThru</span></span>
<span data-ttu-id="46a38-130">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="46a38-130">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a38-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a38-131">-ResourceGroupName</span></span>
<span data-ttu-id="46a38-132">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="46a38-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a38-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46a38-133">-ResourceId</span></span>
<span data-ttu-id="46a38-134">Service Bus 구독 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="46a38-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a38-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="46a38-135">-Topic</span></span>
<span data-ttu-id="46a38-136">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="46a38-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a38-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46a38-137">-Confirm</span></span>
<span data-ttu-id="46a38-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="46a38-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a38-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a38-139">-WhatIf</span></span>
<span data-ttu-id="46a38-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="46a38-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46a38-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46a38-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a38-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a38-142">CommonParameters</span></span>
<span data-ttu-id="46a38-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46a38-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a38-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46a38-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a38-145">입력</span><span class="sxs-lookup"><span data-stu-id="46a38-145">INPUTS</span></span>

### <span data-ttu-id="46a38-146">System.String</span><span class="sxs-lookup"><span data-stu-id="46a38-146">System.String</span></span>

### <span data-ttu-id="46a38-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="46a38-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="46a38-148">출력</span><span class="sxs-lookup"><span data-stu-id="46a38-148">OUTPUTS</span></span>

### <span data-ttu-id="46a38-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46a38-149">System.Boolean</span></span>

## <span data-ttu-id="46a38-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46a38-150">NOTES</span></span>

## <span data-ttu-id="46a38-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46a38-151">RELATED LINKS</span></span>
