---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: 673e67b9611cfab468c1c6f83393515bd4997e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015899"
---
# <span data-ttu-id="1d7e7-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="1d7e7-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="1d7e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="1d7e7-103">지정된 구독의 지정된 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="1d7e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d7e7-104">SYNTAX</span></span>

### <span data-ttu-id="1d7e7-105">RulePropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1d7e7-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d7e7-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1d7e7-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d7e7-107">설명</span><span class="sxs-lookup"><span data-stu-id="1d7e7-107">DESCRIPTION</span></span>
<span data-ttu-id="1d7e7-108">**Remove-AzServiceBusRule** cmdlet은 주어진 토픽의 구독 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="1d7e7-109">예제</span><span class="sxs-lookup"><span data-stu-id="1d7e7-109">EXAMPLES</span></span>

### <span data-ttu-id="1d7e7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1d7e7-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="1d7e7-111">지정된 `SBRule` 토픽의 구독 `SBSubscription` 규칙을 `SBTopic` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="1d7e7-112">예제 2: InputObject - 변수 사용:</span><span class="sxs-lookup"><span data-stu-id="1d7e7-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="1d7e7-113">-InputObject 매개 변수에 대한 $inputobject 통해 제공된 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="1d7e7-114">예제 3: InputObject - 배관 사용:</span><span class="sxs-lookup"><span data-stu-id="1d7e7-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="1d7e7-115">예제 4: ResourceId - 변수 사용</span><span class="sxs-lookup"><span data-stu-id="1d7e7-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="1d7e7-116">예제 5: ResourceId - 문자열 값 사용</span><span class="sxs-lookup"><span data-stu-id="1d7e7-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="1d7e7-117">-ResourceId 매개 변수에 대한 ARM/string의 $resourceid ID를 통해 제공된 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="1d7e7-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1d7e7-118">PARAMETERS</span></span>

### <span data-ttu-id="1d7e7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d7e7-119">-AsJob</span></span>
<span data-ttu-id="1d7e7-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1d7e7-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d7e7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d7e7-121">-DefaultProfile</span></span>
<span data-ttu-id="1d7e7-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d7e7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1d7e7-123">-Force</span></span>
<span data-ttu-id="1d7e7-124">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1d7e7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d7e7-125">-InputObject</span></span>
<span data-ttu-id="1d7e7-126">Service Bus 규칙 개체</span><span class="sxs-lookup"><span data-stu-id="1d7e7-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7e7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="1d7e7-127">-Name</span></span>
<span data-ttu-id="1d7e7-128">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="1d7e7-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7e7-129">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="1d7e7-129">-Namespace</span></span>
<span data-ttu-id="1d7e7-130">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="1d7e7-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7e7-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d7e7-131">-PassThru</span></span>
<span data-ttu-id="1d7e7-132">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1d7e7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d7e7-133">-ResourceGroupName</span></span>
<span data-ttu-id="1d7e7-134">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="1d7e7-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7e7-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d7e7-135">-ResourceId</span></span>
<span data-ttu-id="1d7e7-136">Service Bus 규칙 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1d7e7-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7e7-137">-Subscription</span><span class="sxs-lookup"><span data-stu-id="1d7e7-137">-Subscription</span></span>
<span data-ttu-id="1d7e7-138">구독 이름</span><span class="sxs-lookup"><span data-stu-id="1d7e7-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7e7-139">-Topic</span><span class="sxs-lookup"><span data-stu-id="1d7e7-139">-Topic</span></span>
<span data-ttu-id="1d7e7-140">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="1d7e7-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7e7-141">-확인</span><span class="sxs-lookup"><span data-stu-id="1d7e7-141">-Confirm</span></span>
<span data-ttu-id="1d7e7-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d7e7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d7e7-143">-WhatIf</span></span>
<span data-ttu-id="1d7e7-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d7e7-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d7e7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d7e7-146">CommonParameters</span></span>
<span data-ttu-id="1d7e7-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d7e7-148">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d7e7-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d7e7-149">입력</span><span class="sxs-lookup"><span data-stu-id="1d7e7-149">INPUTS</span></span>

### <span data-ttu-id="1d7e7-150">System.String</span><span class="sxs-lookup"><span data-stu-id="1d7e7-150">System.String</span></span>

### <span data-ttu-id="1d7e7-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="1d7e7-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="1d7e7-152">출력</span><span class="sxs-lookup"><span data-stu-id="1d7e7-152">OUTPUTS</span></span>

### <span data-ttu-id="1d7e7-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d7e7-153">System.Boolean</span></span>

## <span data-ttu-id="1d7e7-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d7e7-154">NOTES</span></span>

## <span data-ttu-id="1d7e7-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d7e7-155">RELATED LINKS</span></span>
