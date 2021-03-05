---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 1423c0c0c67b12b1cb2fcb6bf682d3ed60aae9c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993356"
---
# <span data-ttu-id="bce30-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="bce30-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="bce30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bce30-102">SYNOPSIS</span></span>
<span data-ttu-id="bce30-103">지정된 Service Bus 네임스페이스에서 토픽에 대한 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bce30-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bce30-104">구문</span><span class="sxs-lookup"><span data-stu-id="bce30-104">SYNTAX</span></span>

### <span data-ttu-id="bce30-105">SubscriptionPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bce30-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bce30-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bce30-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce30-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bce30-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bce30-108">설명</span><span class="sxs-lookup"><span data-stu-id="bce30-108">DESCRIPTION</span></span>
<span data-ttu-id="bce30-109">**Remove-AzServiceBusSubscription** cmdlet은 지정된 Service Bus 네임스페이스에서 토픽에 대한 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bce30-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bce30-110">예제</span><span class="sxs-lookup"><span data-stu-id="bce30-110">EXAMPLES</span></span>

### <span data-ttu-id="bce30-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bce30-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="bce30-112">지정된 Service Bus 네임스페이스의 `SB-TopicSubscription-Example1` 토픽에 대한 `SB-Topic_exampl1` 구독을 `SB-Example1` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bce30-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="bce30-113">예제 2: InputObject - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="bce30-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="bce30-114">예제 3: InputObject - 배관 사용:</span><span class="sxs-lookup"><span data-stu-id="bce30-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="bce30-115">예제 4: ResourceId - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="bce30-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="bce30-116">예제 5: ResourceId - 문자열 값 사용:</span><span class="sxs-lookup"><span data-stu-id="bce30-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="bce30-117">-ResourceId 매개 변수에 대한 ARM/string의 $resourceid ID를 통해 제공된 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bce30-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="bce30-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bce30-118">PARAMETERS</span></span>

### <span data-ttu-id="bce30-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bce30-119">-AsJob</span></span>
<span data-ttu-id="bce30-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bce30-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bce30-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce30-121">-DefaultProfile</span></span>
<span data-ttu-id="bce30-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bce30-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce30-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bce30-123">-InputObject</span></span>
<span data-ttu-id="bce30-124">Service Bus 구독 개체</span><span class="sxs-lookup"><span data-stu-id="bce30-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="bce30-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bce30-125">-Name</span></span>
<span data-ttu-id="bce30-126">구독 이름</span><span class="sxs-lookup"><span data-stu-id="bce30-126">Subscription Name</span></span>

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

### <span data-ttu-id="bce30-127">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="bce30-127">-Namespace</span></span>
<span data-ttu-id="bce30-128">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="bce30-128">Namespace Name</span></span>

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

### <span data-ttu-id="bce30-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bce30-129">-PassThru</span></span>
<span data-ttu-id="bce30-130">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="bce30-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="bce30-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce30-131">-ResourceGroupName</span></span>
<span data-ttu-id="bce30-132">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="bce30-132">The name of the resource group</span></span>

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

### <span data-ttu-id="bce30-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bce30-133">-ResourceId</span></span>
<span data-ttu-id="bce30-134">Service Bus 구독 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bce30-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="bce30-135">-Topic</span><span class="sxs-lookup"><span data-stu-id="bce30-135">-Topic</span></span>
<span data-ttu-id="bce30-136">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="bce30-136">Topic Name</span></span>

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

### <span data-ttu-id="bce30-137">-확인</span><span class="sxs-lookup"><span data-stu-id="bce30-137">-Confirm</span></span>
<span data-ttu-id="bce30-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bce30-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce30-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce30-139">-WhatIf</span></span>
<span data-ttu-id="bce30-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bce30-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bce30-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bce30-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce30-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce30-142">CommonParameters</span></span>
<span data-ttu-id="bce30-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bce30-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce30-144">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bce30-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce30-145">입력</span><span class="sxs-lookup"><span data-stu-id="bce30-145">INPUTS</span></span>

### <span data-ttu-id="bce30-146">System.String</span><span class="sxs-lookup"><span data-stu-id="bce30-146">System.String</span></span>

### <span data-ttu-id="bce30-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="bce30-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="bce30-148">출력</span><span class="sxs-lookup"><span data-stu-id="bce30-148">OUTPUTS</span></span>

### <span data-ttu-id="bce30-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bce30-149">System.Boolean</span></span>

## <span data-ttu-id="bce30-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bce30-150">NOTES</span></span>

## <span data-ttu-id="bce30-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bce30-151">RELATED LINKS</span></span>
