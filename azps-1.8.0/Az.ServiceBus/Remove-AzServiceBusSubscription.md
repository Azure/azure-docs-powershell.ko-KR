---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 0369d6bac19d2d2180c54f3c4244101df3a7bb42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699156"
---
# <span data-ttu-id="fb6a9-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="fb6a9-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="fb6a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6a9-103">지정 된 Service Bus 네임 스페이스에서 주제에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fb6a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb6a9-104">SYNTAX</span></span>

### <span data-ttu-id="fb6a9-105">구독 속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fb6a9-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb6a9-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fb6a9-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6a9-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fb6a9-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb6a9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fb6a9-108">DESCRIPTION</span></span>
<span data-ttu-id="fb6a9-109">**AzServiceBusSubscription** cmdlet은 지정 된 Service Bus 네임 스페이스의 주제에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fb6a9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fb6a9-110">EXAMPLES</span></span>

### <span data-ttu-id="fb6a9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb6a9-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="fb6a9-112">`SB-TopicSubscription-Example1` `SB-Topic_exampl1` 지정 된 Service Bus 네임 스페이스의 주제에 대 한 구독을 제거 `SB-Example1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="fb6a9-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="fb6a9-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="fb6a9-114">예제 2.2-InputObject-Using 파이핑:</span><span class="sxs-lookup"><span data-stu-id="fb6a9-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="fb6a9-115">예제 3.1-ResourceId-변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="fb6a9-116">예제 3.2-ResourceId-문자열 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="fb6a9-117">-ResourceId 매개 변수에 대 한 $resourceid/문자열에서 ARM Id를 통해 제공 된 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="fb6a9-118">변수</span><span class="sxs-lookup"><span data-stu-id="fb6a9-118">PARAMETERS</span></span>

### <span data-ttu-id="fb6a9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb6a9-119">-AsJob</span></span>
<span data-ttu-id="fb6a9-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fb6a9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb6a9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6a9-121">-DefaultProfile</span></span>
<span data-ttu-id="fb6a9-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb6a9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb6a9-123">-InputObject</span></span>
<span data-ttu-id="fb6a9-124">Service Bus 구독 개체</span><span class="sxs-lookup"><span data-stu-id="fb6a9-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="fb6a9-125">-이름</span><span class="sxs-lookup"><span data-stu-id="fb6a9-125">-Name</span></span>
<span data-ttu-id="fb6a9-126">구독 이름</span><span class="sxs-lookup"><span data-stu-id="fb6a9-126">Subscription Name</span></span>

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

### <span data-ttu-id="fb6a9-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fb6a9-127">-Namespace</span></span>
<span data-ttu-id="fb6a9-128">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="fb6a9-128">Namespace Name</span></span>

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

### <span data-ttu-id="fb6a9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb6a9-129">-PassThru</span></span>
<span data-ttu-id="fb6a9-130">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="fb6a9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6a9-131">-ResourceGroupName</span></span>
<span data-ttu-id="fb6a9-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-132">The name of the resource group</span></span>

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

### <span data-ttu-id="fb6a9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb6a9-133">-ResourceId</span></span>
<span data-ttu-id="fb6a9-134">Service Bus 구독 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="fb6a9-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="fb6a9-135">-주제</span><span class="sxs-lookup"><span data-stu-id="fb6a9-135">-Topic</span></span>
<span data-ttu-id="fb6a9-136">주제 이름</span><span class="sxs-lookup"><span data-stu-id="fb6a9-136">Topic Name</span></span>

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

### <span data-ttu-id="fb6a9-137">-확인</span><span class="sxs-lookup"><span data-stu-id="fb6a9-137">-Confirm</span></span>
<span data-ttu-id="fb6a9-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb6a9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6a9-139">-WhatIf</span></span>
<span data-ttu-id="fb6a9-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb6a9-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb6a9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6a9-142">CommonParameters</span></span>
<span data-ttu-id="fb6a9-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6a9-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb6a9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6a9-145">입력</span><span class="sxs-lookup"><span data-stu-id="fb6a9-145">INPUTS</span></span>

### <span data-ttu-id="fb6a9-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fb6a9-146">System.String</span></span>

### <span data-ttu-id="fb6a9-147">ServiceBus-PSSubscriptionAttributes.</span><span class="sxs-lookup"><span data-stu-id="fb6a9-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="fb6a9-148">출력</span><span class="sxs-lookup"><span data-stu-id="fb6a9-148">OUTPUTS</span></span>

### <span data-ttu-id="fb6a9-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fb6a9-149">System.Boolean</span></span>

## <span data-ttu-id="fb6a9-150">상속자</span><span class="sxs-lookup"><span data-stu-id="fb6a9-150">NOTES</span></span>

## <span data-ttu-id="fb6a9-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb6a9-151">RELATED LINKS</span></span>
