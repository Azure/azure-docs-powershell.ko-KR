---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: 711213f7bb647d505d02b5492a9d9eb619959a5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699160"
---
# <span data-ttu-id="4b5c6-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="4b5c6-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="4b5c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5c6-103">지정 된 구독에 대 한 speficied 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-103">Removes the speficied rule of a given subscription .</span></span>

## <span data-ttu-id="4b5c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b5c6-104">SYNTAX</span></span>

### <span data-ttu-id="4b5c6-105">Rule속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4b5c6-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b5c6-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4b5c6-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b5c6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4b5c6-107">DESCRIPTION</span></span>
<span data-ttu-id="4b5c6-108">**AzServiceBusRule** cmdlet은 지정 된 항목의 구독에 대 한 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="4b5c6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4b5c6-109">EXAMPLES</span></span>

### <span data-ttu-id="4b5c6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b5c6-110">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="4b5c6-111">`SBRule`지정 된 항목의 구독에 대 한 규칙을 제거 `SBSubscription` `SBTopic` 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="4b5c6-112">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="4b5c6-112">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="4b5c6-113">-InputObject 매개 변수 $inputobject를 통해 제공 된 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="4b5c6-114">예제 2.2-InputObject-Using 파이핑:</span><span class="sxs-lookup"><span data-stu-id="4b5c6-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="4b5c6-115">예제 3.1-ResourceId-변수 사용</span><span class="sxs-lookup"><span data-stu-id="4b5c6-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="4b5c6-116">예제 3.1-ResourceId-문자열 값 사용</span><span class="sxs-lookup"><span data-stu-id="4b5c6-116">Example 3.1 - ResourceId - Using string value</span></span>
```
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="4b5c6-117">-ResourceId 매개 변수에 대 한 $resourceid/문자열에서 ARM Id를 통해 제공 된 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="4b5c6-118">변수</span><span class="sxs-lookup"><span data-stu-id="4b5c6-118">PARAMETERS</span></span>

### <span data-ttu-id="4b5c6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b5c6-119">-AsJob</span></span>
<span data-ttu-id="4b5c6-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4b5c6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b5c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5c6-121">-DefaultProfile</span></span>
<span data-ttu-id="4b5c6-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b5c6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4b5c6-123">-Force</span></span>
<span data-ttu-id="4b5c6-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4b5c6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b5c6-125">-InputObject</span></span>
<span data-ttu-id="4b5c6-126">Service Bus 규칙 개체</span><span class="sxs-lookup"><span data-stu-id="4b5c6-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="4b5c6-127">-이름</span><span class="sxs-lookup"><span data-stu-id="4b5c6-127">-Name</span></span>
<span data-ttu-id="4b5c6-128">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="4b5c6-128">Rule Name</span></span>

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

### <span data-ttu-id="4b5c6-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b5c6-129">-Namespace</span></span>
<span data-ttu-id="4b5c6-130">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="4b5c6-130">Namespace Name</span></span>

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

### <span data-ttu-id="4b5c6-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b5c6-131">-PassThru</span></span>
<span data-ttu-id="4b5c6-132">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4b5c6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5c6-133">-ResourceGroupName</span></span>
<span data-ttu-id="4b5c6-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-134">The name of the resource group</span></span>

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

### <span data-ttu-id="4b5c6-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b5c6-135">-ResourceId</span></span>
<span data-ttu-id="4b5c6-136">서비스 버스 규칙 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="4b5c6-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="4b5c6-137">-구독</span><span class="sxs-lookup"><span data-stu-id="4b5c6-137">-Subscription</span></span>
<span data-ttu-id="4b5c6-138">구독 이름</span><span class="sxs-lookup"><span data-stu-id="4b5c6-138">Subscription Name</span></span>

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

### <span data-ttu-id="4b5c6-139">-주제</span><span class="sxs-lookup"><span data-stu-id="4b5c6-139">-Topic</span></span>
<span data-ttu-id="4b5c6-140">주제 이름</span><span class="sxs-lookup"><span data-stu-id="4b5c6-140">Topic Name</span></span>

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

### <span data-ttu-id="4b5c6-141">-확인</span><span class="sxs-lookup"><span data-stu-id="4b5c6-141">-Confirm</span></span>
<span data-ttu-id="4b5c6-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b5c6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b5c6-143">-WhatIf</span></span>
<span data-ttu-id="4b5c6-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b5c6-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b5c6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5c6-146">CommonParameters</span></span>
<span data-ttu-id="4b5c6-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5c6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5c6-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b5c6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5c6-149">입력</span><span class="sxs-lookup"><span data-stu-id="4b5c6-149">INPUTS</span></span>

### <span data-ttu-id="4b5c6-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4b5c6-150">System.String</span></span>

### <span data-ttu-id="4b5c6-151">ServiceBus. a. m/.Ppstop특성</span><span class="sxs-lookup"><span data-stu-id="4b5c6-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="4b5c6-152">출력</span><span class="sxs-lookup"><span data-stu-id="4b5c6-152">OUTPUTS</span></span>

### <span data-ttu-id="4b5c6-153">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4b5c6-153">System.Boolean</span></span>

## <span data-ttu-id="4b5c6-154">상속자</span><span class="sxs-lookup"><span data-stu-id="4b5c6-154">NOTES</span></span>

## <span data-ttu-id="4b5c6-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b5c6-155">RELATED LINKS</span></span>
